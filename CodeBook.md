## Getting and Cleaning Data Course Project Codebook

### Introduction
This codebook refers to the file run_analysis.R in the repository at 
https://github.com/moorejm/Getting-and-Cleaning-Data.

The data set used for this analysis is originally from the UCI Machine Learning Repository
at: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Source:
Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto.
Smartlab - Non Linear Complex Systems Laboratory
DITEN - UniversitÃ  degli Studi di Genova, Genoa I-16145, Italy.
activityrecognition '@' smartlab.ws
www.smartlab.ws 

Download link: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

The purpose of the run_analysis.R function is to merge and clean the "train" and "test" data from the 
UCI HAR Dataset by subsetting the mean and standard deviation variables in the data set, making the 
activities and variables more readable for the user, and aggregating the data set to find the average of 
each variable for each activity and subject. More information about run_analysis.R can be found in the 
README.md file in the repository at https://github.com/moorejm/Getting-and-Cleaning-Data and more information
about the data set used in the analysis can be found in the README.txt file included with the data set.

###Codebook Format
-Variable Name



```{r, echo=FALSE, message=FALSE}
# This R function is designed to merge and clean the UCI HAR Dataset
# (data: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)
# (original source: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)
# by combining the y_test, y_train, x_test, x_train, subject_test, subject_train, activity_labels, 
# and features files, subsetting just the mean and standard deviation variables in
# x_test and x_train, and making the activity labels and variable names more readable for
# the user (variable names are named using the UpperCamelCase format for improved readability). 
# Finally, the combined data set is condensed into a tidy data set by using the
# aggregate function to find the average of each variable for each subject and subject.
# Refer to README.md and CodeBook.md in the github repository at
# https://github.com/moorejm/Getting-and-Cleaning-Data for more information.


# Import data using the read.table command, all files are in a .txt format.
# Use rbind to combine y_test and y_train, subject_test and subject_train, and x_test and x_train,
# then use cbind to combine the x, y, and subject data sets.
data_y_test <- read.table("./UCI HAR Dataset/test/y_test.txt", header = FALSE)
data_y_train <- read.table("./UCI HAR Dataset/train/y_train.txt", header = FALSE)
bind_y <- rbind(data_y_test, data_y_train)
data_subj_test <- read.table("./UCI HAR Dataset/test/subject_test.txt", header = FALSE)
data_subj_train <- read.table("./UCI HAR Dataset/train/subject_train.txt", header = FALSE)
bind_subj <- rbind(data_subj_test, data_subj_train)
bind_y_subj <- cbind(bind_y, bind_subj)
data_x_test <- read.table("./UCI HAR Dataset/test/X_test.txt", sep = "", header = FALSE)
data_x_train <- read.table("./UCI HAR Dataset/train/X_train.txt", sep = "", header = FALSE)
bind_x <- rbind(data_x_test, data_x_train)
complete_data <- cbind(bind_y_subj, bind_x)


# Subset the mean and standard deviation columns in the combined dataset (complete_data)
mean_sd_data <- complete_data[,c(1,2,3,4,5,6,7,8,43,44,45,46,47,48,83,84,85,86,87,88,123,124,125,126,127,
                                 128,163,164,165,166,167,168,203,204,216,217,229,230,242,243,255,256,268,
                                 269,270,271,272,273,296,297,298,347,348,349,350,351,352,375,376,377,426,
                                 427,428,429,430,431,454,455,456,505,506,515,518,519,528,531,532,541,544,
                                 545,554,557,558,559,560,561,562,563)]

# Use the merge function to change the original activity names (1-6) into the more descriptive
# variable names found in activity_labels.txt
activity_labels <- read.table("./UCI HAR Dataset/activity_labels.txt", header= FALSE)
desc_activity <- merge(activity_labels, mean_sd_data, by.x = "V1", by.y = "V1")
desc_activity_clean <- desc_activity[,2:89]

# Import the file features.txt and subset the mean and standard deviation column headers.
# Append "Activity" and "Subject" to the beginning of the column header file, then
# use gsub to make the column headers more readable (using UpperCamelCase to improve readability).
# Finally, change the column names of the combined data set (desc_activity_clean)
data_features <- read.table("./UCI HAR Dataset/features.txt", header = FALSE)
trim_features <- data_features[c(1,2,3,4,5,6,41,42,43,44,45,46,81,82,83,84,85,86,121,122,123,124,125,126,
                                161,162,163,164,165,166,201,202,214,215,227,228,240,241,253,254,266,267,
                                268,269,270,271,294,295,296,345,346,347,348,349,350,373,374,375,424,425,
                                426,427,428,429,452,453,454,503,504,513,516,517,526,529,530,539,542,543,
                                552,555,556,557,558,559,560,561),2]
add_activity_subject <- c("Activity","Subject")
add_features <- append(add_activity_subject, as.character(trim_features))
add_features <- gsub("-|\\(),", "", add_features)
add_features <- gsub("^t", "TimeDomain", add_features)
add_features <- gsub("^f", "FastFourierTransform", add_features)
add_features <- gsub("Acc", "Accelerometer", add_features)
add_features <- gsub("Gyro", "Gyroscope", add_features)
add_features <- gsub("Mag", "Magnitude", add_features)
add_features <- gsub("Freq", "Frequency", add_features)
add_features <- gsub("mean", "Mean", add_features)
add_features <- gsub("std", "StandardDeviation", add_features)
add_features <- gsub("\\()X", "Xaxis", add_features)
add_features <- gsub("\\()Y", "Yaxis", add_features)
add_features <- gsub("\\()Z", "Zaxis", add_features)
add_features <- gsub("\\()$", "", add_features)
add_features <- gsub("angle\\(tBodyAccelerometerMean,gravity)", "TimeDomainAccelerometerMeanGravity", add_features)
add_features <- gsub("angle\\(tBodyAccelerometerJerkMean),gravityMean)", "TimeDomainBodyAccelerometerJerkMean", add_features)
add_features <- gsub("angle\\(tBodyGyroscopeMean,gravityMean)", "TimeDomainBodyGyroscopeMeanGravityMean", add_features)
add_features <- gsub("angle\\(tBodyGyroscopeJerkMean,gravityMean)", "TimeDomainGyroscopeJerkMeanGravityMean", add_features)
add_features <- gsub("angle\\(X,gravityMean)", "XaxisGravityMean", add_features)
add_features <- gsub("angle\\(Y,gravityMean)", "YaxisGravityMean", add_features)
add_features <- gsub("angle\\(Z,gravityMean)", "ZaxisGravityMean", add_features)
colnames(desc_activity_clean) <- add_features

# Use the aggregate function to create a tidy data set that displays the average of each variable
# for each activity and subject.
clean_data2 <- aggregate(desc_activity_clean[,c(3:88)], by=list(desc_activity_clean$Activity,desc_activity_clean$Subject), FUN=mean)
colnames(clean_data2) <- add_features
head(add_features)

# Uncomment the line below to write the data to a text file in your working directory, run_analysis.txt
# write.table(clean_data2, "./run_analysis.txt", row.names=FALSE)
```

You can also embed plots, for example:

```{r fig.width=7, fig.height=6}
plot(cars)
```

