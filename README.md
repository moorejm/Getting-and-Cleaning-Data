## Coursera Getting and Cleaning Data Course Project ReadMe
### Introduction
The purpose of this ReadMe file is to describe the functionality of the run_analysis.R file found in the Getting-and-Cleaning-Data repo (https://github.com/moorejm/Getting-and-Cleaning-Data). The source of the data used for the run_analysis function can be found at the UCI Machine Learning Repository webpage, http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones, and the data set can be downloaded at https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip.

The data was collected by:

Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto.
Smartlab - Non Linear Complex Systems Laboratory
DITEN - UniversitÃ  degli Studi di Genova, Genoa I-16145, Italy.
activityrecognition '@' smartlab.ws
www.smartlab.ws 

### Purpose and Summary
The purpose of the run_analysis function is to practice data cleaning techniques taught in the Coursera course "Getting and Cleaning Data," taught by Dr. Jeff Leek at the Johns Hopkins Bloomberg School of Public Health. The R function performs the following tasks:

1. Merges data from the "training" and "test" data sets (downloaded from the link above)
2. Subsets the merged data set to only display mean and standard deviation measurements
3. Uses the merge() command to convert activities in the raw data sets (reported as numbers) into a readable format using activity_labels.txt
4. Uses the gsub() command to remove extra characters and expand shorthand variable names to make it more readable for the user (UpperCamelCase was used instead of lowercase variable names to make it easier to read long variable names)
5. Uses the aggregate() command to condense the data set into one mean per unique variable, activity, and subject combination.

For more information regarding study design and how the data was collected, refer to README.txt in the UCI HAR Dataset.

### Description of run_analysis.R Functionality
**Note:** For run_analysis to work properly, download the data set from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip and extract the UCI HAR Dataset folder to your working directory. Additionally, to write the results as a text file to your working directory, uncomment the last line. By default, this line is commented out so that users don't accidentally write the results table to their computer.

```
# write.table(clean_data2, "./run_analysis.txt", row.names=FALSE)
```

####1. Merge data from the "training" and "test" data set
Run.analysis.R combines the following files from UCI HAR "train" and "test" data sets (download link above):
* y_test.txt (activity indicator for the test data set)
* y_train.txt (activity indicator for the train data set)
* x_test.txt (test data for all measured variables in "features")
* x_train.txt (train data for all measured variables in "features")
* subject_test.txt (subject number for the test data set)
* subject_train.txt (subject number for the train data set)
* activity_labels.txt (activity labels for numbers listed in "y_test" and "y_train")
* features.txt (list of all measured variables)

The files are imported into R using the read.table() command and then the equivalent files from the test and train data sets (e.g., x_test and x_train) are combined using the rbind() command.

**Example:**
```
data_y_test <- read.table("./UCI HAR Dataset/test/y_test.txt", header = FALSE)
data_y_train <- read.table("./UCI HAR Dataset/train/y_train.txt", header = FALSE)
bind_y <- rbind(data_y_test, data_y_train)
```

Once the y_, x_, and subject_ files have been combined using rbind(), the three tables are combined using cbind(). Note that the combined data will not have a header until step 4.

**Example:**
```
complete_data <- cbind(bind_y_subj, bind_x)
```

####2. Subset the merged data set to only display mean and standard deviation measurements
After combining the data sets, run_analysis.R subsets the combined table to only include mean and standard deviation variables. This was decided to be variables listed in features.txt with the keywords "mean" or "std" (in addition to the "Subject" and "Activity" columns from the combined data set). This includes variables that compare the difference in the angle measurements of multiple means since it deals with mean data.

```
mean_sd_data <- complete_data[,c(1,2,3,4,5,6,7,8,43,44,45,46,47,48,83,84,85,86,87,88,123,124,125,126,127,
128,163,164,165,166,167,168,203,204,216,217,229,230,242,243,255,256,268,
269,270,271,272,273,296,297,298,347,348,349,350,351,352,375,376,377,426,
427,428,429,430,431,454,455,456,505,506,515,518,519,528,531,532,541,544,
545,554,557,558,559,560,561,562,563)]
```

####3. Use the merge() command to convert activities in the raw data sets (reported as numbers) into a readable format using activity_labels.txt
Once the data has been condensed to just include mean and standard deviation data, run_analysis.R uses the merge() command to replace the values found in y_test.txt and y_train.txt, representing the activity, with the actual activity name. The purpose of this is to make the data set more readable to the user instead of needing to look up the number (1-6) in a codebook. The numbered activity is used as the primary key between the files y_test.txt, y_train.txt (combined in the table "mean_sd_data"), and activity_labels.txt.

```
activity_labels <- read.table("./UCI HAR Dataset/activity_labels.txt", header= FALSE)
desc_activity <- merge(activity_labels, mean_sd_data, by.x = "V1", by.y = "V1")
desc_activity_clean <- desc_activity[,2:89]
```

####4. Use the gsub() command to remove extra characters and expand shorthand variable names to make it more readable for the user
Similar to step 3, the purpose of this step is to make the data set more readable. Run_analysis.R makes variable names (originally from features.txt) more readable by using the gsub() command to remove symbols (such as "-","(", and ")"), expand shorthand variables (such as "t" to "TimeDomain" or "Freq" to "Frequency"), and create a consistent naming convention.

**Example:**
```
add_features <- gsub("-|\\(),", "", add_features)
add_features <- gsub("^t", "TimeDomain", add_features)
add_features <- gsub("^f", "FastFourierTransform", add_features)
add_features <- gsub("Acc", "Accelerometer", add_features)
```

Although the lecture notes in the Getting and Cleaning Data course recommend using all lowercase characters for variable names, the UpperCamelCase format was used for variables in this project because it makes it easier for the user to read the long column headers found in the output table.

####5. Use the aggregate() command to condense the data set into one mean per unique variable, activity, and subject combination.
Using the aggregate() command, the data set is condensed into a table containing the mean for each unique combination of variable, activity, and subject. This reduces the size of the final table considerably. For example, all of the "WALKING" measurements recorded by Subject 1 for the variable "TimeDomainBodyAccelerometerMeanXaxis" are combined into one data point, the mean of the recorded measurements.

```
clean_data2 <- aggregate(desc_activity_clean[,c(3:88)], by=list(desc_activity_clean$Activity,desc_activity_clean$Subject), FUN=mean)
```

####Final Steps
After the tidy data set has been created, the final step is to apply the detailed column names to the data set and output the results. In order to prevent users from mistakenly writing the results to a text file on their computer, the write.table() command has been commented out. To write the results to a text file, simply uncomment the final line.

```
colnames(clean_data2) <- add_features
clean_data2
# Uncomment the line below to write the data to a text file in your working directory, run_analysis.txt
# write.table(clean_data2, "./run_analysis.txt", row.names=FALSE)
```
