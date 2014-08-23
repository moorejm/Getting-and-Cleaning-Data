## Coursera Getting and Cleaning Data Course Project ReadMe
### Introduction
The purpose of this ReadMe file is to describe the functionality of the run_analysis.R file found in this repo (https://github.com/moorejm/Getting-and-Cleaning-Data). The source of the data used for the run_analysis function can be found at the UCI Machine Learning Repository webpage, http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones, and the data set can be downloaded at https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip.

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
3. Uses the "merge" command to convert activities in the raw data sets (reported as numbers) into a readable format using the codebook included with the original data set
4. Uses the "gsub" command to remove extra characters and expand shorthand variable names to make it more readable for the user (UpperCamelCase was used instead of lowercase variable names to make it easier to read long variable names)
5. Uses the "aggregate" command to condense the data set into one mean per unique variable, activity, and subject combination.

### Description of run_analysis.R Functionality
**Note:** For run_analysis to work properly, download the data set from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip and extract the UCI HAR Dataset folder to your working directory. Additionally, to write the results as a text file to your working directory, uncomment the last line. By default, this line is commented out so that users don't accidentally write a file to their computer.

```
# write.table(clean_data2, "./run_analysis.txt", row.names=FALSE)
```

####1. Merges data from the "training" and "test" data set
Run.analysis.R combines the following files from UCI HAR "train" and "test" data sets (download link above):
* y_test (activity indicator for the test data set)
* y_train (activity indicator for the train data set)
* x_test (test data for all measured variables in "features")
* x_train (train data for all measured variables in "features")
* subject_test (subject number for the test data set)
* subject_train (subject number for the train data set)
* activity_labels (activity labels for numbers listed in "y_test" and "y_train")
* features (list of all measured variables)

The files are imported into R using the read.table() command and then equivalent files from the test and train data sets are combined using the rbind() command.

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

####2. Subsets the merged data set to only display mean and standard deviation measurements
