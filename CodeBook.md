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
  - List/Range of Values

### Codebook

* Activity
  - test
  - test
  - test

* Subject
  - test
  - test
  - test

* TimeDomainBodyAccelerometerMeanXaxis
  -
  -
  - 0.22159824394 to 0.3014610196, Range = 0.07986277566

* TimeDomainBodyAccelerometerMeanYaxis
  -
  -
  - -0.0405139534294 to -0.00130828765170213, Range = 0.0392056657776979

* TimeDomainBodyAccelerometerMeanZaxis
  -
  -
  - -0.152513899520833 to -0.07537846886, Range = 0.077135430660833

* TimeDomainBodyAccelerometerStandardDeviationXaxis
  -
  -
  - -0.996068635384615 to 0.626917070512821, Range = 1.62298570589744

* TimeDomainBodyAccelerometerStandardDeviationYaxis
  -
  -
  - -0.990240946666667 to 0.616937015333333, Range = 1.607177962

* TimeDomainBodyAccelerometerStandardDeviationZaxis
  -
  -
  - -0.987658662307692 to 0.609017879074074, Range = 1.59667654138177

* TimeDomainGravityAccelerometerMeanXaxis
  -
  -
  - -0.680043155060241 to 0.974508732, Range = 1.65455188706024

* TimeDomainGravityAccelerometerMeanYaxis
  -
  -
  - -0.479894842941176 to 0.956593814210526, Range = 1.4364886571517

* TimeDomainGravityAccelerometerMeanZaxis
  -
  -
  - -0.49508872037037 to 0.9578730416, Range = 1.45296176197037

* TimeDomainGravityAccelerometerStandardDeviationXaxis
  -
  -
  - -0.996764227384615 to -0.829554947808219, Range = 0.167209279576396

* TimeDomainGravityAccelerometerStandardDeviationYaxis
  -
  -
  - -0.99424764884058 to -0.643578361424658, Range = 0.350669287415922

* TimeDomainGravityAccelerometerStandardDeviationZaxis
  -
  -
  - -0.990957249538462 to -0.610161166287671, Range = 0.380796083250791

* TimeDomainBodyAccelerometerJerkMeanXaxis
  -
  -
  - 0.0426880986186441 to 0.130193043809524, Range = 0.0875049451908799

* TimeDomainBodyAccelerometerJerkMeanYaxis
  -
  -
  - -0.0386872111282051 to 0.056818586275, Range = 0.0955057974032051

* TimeDomainBodyAccelerometerJerkMeanZaxis
  -
  -
  - -0.0674583919268293 to 0.0380533591627451, Range = 0.105511751089574

* TimeDomainBodyAccelerometerJerkStandardDeviationXaxis
  -
  -
  - -0.994604542264151 to 0.544273037307692, Range = 1.53887757957184

* TimeDomainBodyAccelerometerJerkStandardDeviationYaxis
  -
  -
  - -0.989513565652174 to 0.355306716915385, Range = 1.34482028256756

* TimeDomainBodyAccelerometerJerkStandardDeviationZaxis
  -
  -
  - -0.993288313333333 to 0.0310157077775926, Range = 1.02430402111093

* TimeDomainBodyGyroscopeMeanXaxis
  -
  -
  - -0.205775427307692 to 0.19270447595122, Range = 0.398479903258912

* TimeDomainBodyGyroscopeMeanYaxis
  -
  -
  - -0.204205356087805 to 0.0274707556666667, Range = 0.231676111754472

* TimeDomainBodyGyroscopeMeanZaxis
  -
  -
  - -0.0724546025804878 to 0.179102058245614, Range = 0.251556660826102

* TimeDomainBodyGyroscopeStandardDeviationXaxis
  -
  -
  - -0.994276591304348 to 0.267657219333333, Range = 1.26193381063768

* TimeDomainBodyGyroscopeStandardDeviationYaxis
  -
  -
  - -0.994210471914894 to 0.476518714444444, Range = 1.47072918635934

* TimeDomainBodyGyroscopeStandardDeviationZaxis
  -
  -
  - -0.985538363333333 to 0.564875818162963, Range = 1.5504141814963

* TimeDomainBodyGyroscopeJerkMeanXaxis
  -
  -
  - -0.157212539189362 to -0.0220916265065217, Range = 0.13512091268284

* TimeDomainBodyGyroscopeJerkMeanYaxis
  -
  -
  - -0.0768089915604167 to -0.0132022768074468, Range = 0.0636067147529699

* TimeDomainBodyGyroscopeJerkMeanZaxis
  -
  -
  - -0.0924998531372549 to -0.00694066389361702, Range = 0.0855591892436379

* TimeDomainBodyGyroscopeJerkStandardDeviationXaxis
  -
  -
  - -0.99654254057971 to 0.179148649684615, Range = 1.17569119026433

* TimeDomainBodyGyroscopeJerkStandardDeviationYaxis
  -
  -
  - -0.997081575652174 to 0.295945926186441, Range = 1.29302750183862

* TimeDomainBodyGyroscopeJerkStandardDeviationZaxis
  -
  -
  - -0.995380794637681 to 0.193206498960417, Range = 1.1885872935981

* TimeDomainBodyAccelerometerMagnitudeMean
  -
  -
  - -0.986493196666667 to 0.644604325128205, Range = 1.63109752179487

* TimeDomainBodyAccelerometerMagnitudeStandardDeviation
  -
  -
  - -0.986464542615385 to 0.428405922622222, Range = 1.41487046523761

* TimeDomainGravityAccelerometerMagnitudeMean
  -
  -
  - -0.986493196666667 to 0.644604325128205, Range = 1.63109752179487

* TimeDomainGravityAccelerometerMagnitudeStandardDeviation
  -
  -
  - -0.986464542615385 to 0.428405922622222, Range = 1.41487046523761

* TimeDomainBodyAccelerometerJerkMagnitudeMean
  -
  -
  - -0.99281471515625 to 0.434490400974359, Range = 1.42730511613061


* TimeDomainBodyAccelerometerJerkMagnitudeStandardDeviation
  -
  -
  - -0.994646916811594 to 0.450612065720513, Range = 1.44525898253211

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
