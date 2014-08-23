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

### Codebook Format

* Variable Name
  - Variable Length
  - Variable Definition
  - Range of Values

### Codebook

* Activity
  -
  -
  -

* Subject
  -
  -
  -

* TimeDomainBodyAccelerometerMeanXaxis
  -
  -
  -

* TimeDomainBodyAccelerometerMeanYaxis
  -
  -
  -

* TimeDomainBodyAccelerometerMeanZaxis
  -
  -
  -

* TimeDomainBodyAccelerometerStandardDeviationXaxis
  -
  -
  -

* TimeDomainBodyAccelerometerStandardDeviationYaxis
  -
  -
  -

* TimeDomainBodyAccelerometerStandardDeviationZaxis
  -
  -
  -

* TimeDomainGravityAccelerometerMeanXaxis
  -
  -
  -

* TimeDomainGravityAccelerometerMeanYaxis
  -
  -
  -

* TimeDomainGravityAccelerometerMeanZaxis
  -
  -
  -

* TimeDomainGravityAccelerometerStandardDeviationXaxis
  -
  -
  -

* TimeDomainGravityAccelerometerStandardDeviationYaxis
  -
  -
  -

* TimeDomainGravityAccelerometerStandardDeviationZaxis
  -
  -
  -

* TimeDomainBodyAccelerometerJerkMeanXaxis
  -
  -
  -

* TimeDomainBodyAccelerometerJerkMeanYaxis
  -
  -
  -

* TimeDomainBodyAccelerometerJerkMeanZaxis
  -
  -
  -

* TimeDomainBodyAccelerometerJerkStandardDeviationXaxis
  -
  -
  -

* TimeDomainBodyAccelerometerJerkStandardDeviationYaxis
  -
  -
  -

* TimeDomainBodyAccelerometerJerkStandardDeviationZaxis
  -
  -
  -

* TimeDomainBodyGyroscopeMeanXaxis
  -
  -
  -

* TimeDomainBodyGyroscopeMeanYaxis
  -
  -
  -

* TimeDomainBodyGyroscopeMeanZaxis
  -
  -
  -

* TimeDomainBodyGyroscopeStandardDeviationXaxis
  -
  -
  -

* TimeDomainBodyGyroscopeStandardDeviationYaxis
  -
  -
  -

* TimeDomainBodyGyroscopeStandardDeviationZaxis
  -
  -
  -

* TimeDomainBodyGyroscopeJerkMeanXaxis
  -
  -
  -

* TimeDomainBodyGyroscopeJerkMeanYaxis
  -
  -
  -

* TimeDomainBodyGyroscopeJerkMeanZaxis
  -
  -
  -

* TimeDomainBodyGyroscopeJerkStandardDeviationXaxis
  -
  -
  -

* TimeDomainBodyGyroscopeJerkStandardDeviationYaxis
  -
  -
  -

* TimeDomainBodyGyroscopeJerkStandardDeviationZaxis
  -
  -
  -

* TimeDomainBodyAccelerometerMagnitudeMean
  -
  -
  -

* TimeDomainBodyAccelerometerMagnitudeStandardDeviation
  -
  -
  -

* TimeDomainGravityAccelerometerMagnitudeMean
  -
  -
  -

* TimeDomainGravityAccelerometerMagnitudeStandardDeviation
  -
  -
  -

* TimeDomainBodyAccelerometerJerkMagnitudeMean
  -
  -
  -

* TimeDomainBodyAccelerometerJerkMagnitudeStandardDeviation
  -
  -
  -

* TimeDomainBodyGyroscopeMagnitudeMean
  -
  -
  -

* TimeDomainBodyGyroscopeMagnitudeStandardDeviation
  -
  -
  -

* TimeDomainBodyGyroscopeJerkMagnitudeMean
  -
  -
  -

* TimeDomainBodyGyroscopeJerkMagnitudeStandardDeviation
  -
  -
  -

* FastFourierTransformBodyAccelerometerMeanXaxis
  -
  -
  -

* FastFourierTransformBodyAccelerometerMeanYaxis
  -
  -
  -

* FastFourierTransformBodyAccelerometerMeanZaxis
  -
  -
  -

* FastFourierTransformBodyAccelerometerStandardDeviationXaxis
  -
  -
  -

* FastFourierTransformBodyAccelerometerStandardDeviationYaxis
  -
  -
  -

* FastFourierTransformBodyAccelerometerStandardDeviationZaxis
  -
  -
  -

* FastFourierTransformBodyAccelerometerMeanFrequencyXaxis
  -
  -
  -

* FastFourierTransformBodyAccelerometerMeanFrequencyYaxis
  -
  -
  -

* FastFourierTransformBodyAccelerometerMeanFrequencyZaxis
  -
  -
  -

* FastFourierTransformBodyAccelerometerJerkMeanXaxis
  -
  -
  -

* FastFourierTransformBodyAccelerometerJerkMeanYaxis
  -
  -
  -

* FastFourierTransformBodyAccelerometerJerkMeanZaxis
  -
  -
  -

* FastFourierTransformBodyAccelerometerJerkStandardDeviationXaxis
  -
  -
  -

* FastFourierTransformBodyAccelerometerJerkStandardDeviationYaxis
  -
  -
  -

* FastFourierTransformBodyAccelerometerJerkStandardDeviationZaxis
  -
  -
  -

* FastFourierTransformBodyAccelerometerJerkMeanFrequencyXaxis
  -
  -
  -

* FastFourierTransformBodyAccelerometerJerkMeanFrequencyYaxis
  -
  -
  -

* FastFourierTransformBodyAccelerometerJerkMeanFrequencyZaxis
  -
  -
  -

* FastFourierTransformBodyGyroscopeMeanXaxis
  -
  -
  -

* FastFourierTransformBodyGyroscopeMeanYaxis
  -
  -
  -

* FastFourierTransformBodyGyroscopeMeanZaxis
  -
  -
  -

* FastFourierTransformBodyGyroscopeStandardDeviationXaxis
  -
  -
  -

* FastFourierTransformBodyGyroscopeStandardDeviationYaxis
  -
  -
  -

* FastFourierTransformBodyGyroscopeStandardDeviationZaxis
  -
  -
  -

* FastFourierTransformBodyGyroscopeMeanFrequencyXaxis
  -
  -
  -

* FastFourierTransformBodyGyroscopeMeanFrequencyYaxis
  -
  -
  -

* FastFourierTransformBodyGyroscopeMeanFrequencyZaxis
  -
  -
  -

* FastFourierTransformBodyAccelerometerMagnitudeMean
  -
  -
  -

* FastFourierTransformBodyAccelerometerMagnitudeStandardDeviation
  -
  -
  -

* FastFourierTransformBodyAccelerometerMagnitudeMeanFrequency
  -
  -
  -

* FastFourierTransformBodyBodyAccelerometerJerkMagnitudeMean
  -
  -
  -

* FastFourierTransformBodyBodyAccelerometerJerkMagnitudeStandardDeviation
  -
  -
  -

* FastFourierTransformBodyBodyAccelerometerJerkMagnitudeMeanFrequency
  -
  -
  -

* FastFourierTransformBodyBodyGyroscopeMagnitudeMean
  -
  -
  -

* FastFourierTransformBodyBodyGyroscopeMagnitudeStandardDeviation
  -
  -
  -

* FastFourierTransformBodyBodyGyroscopeMagnitudeMeanFrequency
  -
  -
  -

* FastFourierTransformBodyBodyGyroscopeJerkMagnitudeMean
  -
  -
  -

* FastFourierTransformBodyBodyGyroscopeJerkMagnitudeStandardDeviation
  -
  -
  -

* FastFourierTransformBodyBodyGyroscopeJerkMagnitudeMeanFrequency
  -
  -
  -

* TimeDomainAccelerometerMeanGravity
  -
  -
  -

* TimeDomainBodyAccelerometerJerkMean
  -
  -
  -

* TimeDomainBodyGyroscopeMeanGravityMean
  -
  -
  -

* TimeDomainGyroscopeJerkMeanGravityMean
  -
  -
  -

* XaxisGravityMean
  -
  -
  -

* YaxisGravityMean
  -
  -
  -

* ZaxisGravityMean
  -
  -
  -
