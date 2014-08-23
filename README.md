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

## Description of run_analysis.R Functionality

**Note:** For run_analysis to work properly, download the data set from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip and extract the UCI HAR Dataset folder to your working directory. Additionally, to write the results as a text file to your working directory, uncomment the last line:

```
# write.table(clean_data2, "./run_analysis.txt", row.names=FALSE)
```

By default, this line is commented out so that users don't accidentally write a file to their computer.

