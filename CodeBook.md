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
  - Variable Position/Definition (as [Position] Definition)
  - Variable Length, Type (as Min Length to Max Length, Data Type)
  - List/Range of Values (as Min to Max, Range = Max-Min)

### Codebook

* Activity
  - [1] Activity description
  - test
  - test

* Subject
  - [2] Subject number
  - test
  - Integers 1-30

* TimeDomainBodyAccelerometerMeanXaxis
  - [3] Time domain signal: body accelerometer mean for the X axis measurement
  - 10 to 17, numeric
  - 0.22159824394 to 0.3014610196, Range = 0.07986277566

* TimeDomainBodyAccelerometerMeanYaxis
  - [4] Time domain signal: body accelerometer mean for the Y axis measurement
  - 14 to 20, numeric
  - -0.0405139534294 to -0.00130828765170213, Range = 0.0392056657776979

* TimeDomainBodyAccelerometerMeanZaxis
  - [5] Time domain signal: body accelerometer mean for the Z axis measurement
  - 13 to 19, numeric
  - -0.152513899520833 to -0.07537846886, Range = 0.077135430660833

* TimeDomainBodyAccelerometerStandardDeviationXaxis
  -
  - 11 to 20, numeric
  - -0.996068635384615 to 0.626917070512821, Range = 1.62298570589744

* TimeDomainBodyAccelerometerStandardDeviationYaxis
  -
  - 11 to 20, numeric

  - -0.990240946666667 to 0.616937015333333, Range = 1.607177962

* TimeDomainBodyAccelerometerStandardDeviationZaxis
  -
  - 12 to 20, numeric
  - -0.987658662307692 to 0.609017879074074, Range = 1.59667654138177

* TimeDomainGravityAccelerometerMeanXaxis
  -
  - 10 to 18, numeric
  - -0.680043155060241 to 0.974508732, Range = 1.65455188706024

* TimeDomainGravityAccelerometerMeanYaxis
  -
  - 10 to 19, numeric
  - -0.479894842941176 to 0.956593814210526, Range = 1.4364886571517

* TimeDomainGravityAccelerometerMeanZaxis
  -
  - 10 to 20, numeric
  - -0.49508872037037 to 0.9578730416, Range = 1.45296176197037

* TimeDomainGravityAccelerometerStandardDeviationXaxis
  -
  - 11 to 18, numeric
  - -0.996764227384615 to -0.829554947808219, Range = 0.167209279576396

* TimeDomainGravityAccelerometerStandardDeviationYaxis
  -
  - 11 to 18, numeric
  - -0.99424764884058 to -0.643578361424658, Range = 0.350669287415922

* TimeDomainGravityAccelerometerStandardDeviationZaxis
  -
  - 11 to 18, numeric
  - -0.990957249538462 to -0.610161166287671, Range = 0.380796083250791

* TimeDomainBodyAccelerometerJerkMeanXaxis
  -
  - 10 to 18, numeric
  - 0.0426880986186441 to 0.130193043809524, Range = 0.0875049451908799

* TimeDomainBodyAccelerometerJerkMeanYaxis
  -
  - 12 to 21, numeric
  - -0.0386872111282051 to 0.056818586275, Range = 0.0955057974032051

* TimeDomainBodyAccelerometerJerkMeanZaxis
  -
  - 11 to 21, numeric
  - -0.0674583919268293 to 0.0380533591627451, Range = 0.105511751089574

* TimeDomainBodyAccelerometerJerkStandardDeviationXaxis
  -
  - 11 to 20, numeric
  - -0.994604542264151 to 0.544273037307692, Range = 1.53887757957184

* TimeDomainBodyAccelerometerJerkStandardDeviationYaxis
  -
  - 10 to 19, numeric
  - -0.989513565652174 to 0.355306716915385, Range = 1.34482028256756

* TimeDomainBodyAccelerometerJerkStandardDeviationZaxis
  -
  - 10 to 19, numeric
  - -0.993288313333333 to 0.0310157077775926, Range = 1.02430402111093

* TimeDomainBodyGyroscopeMeanXaxis
  -
  - 11 to 20, numeric
  - -0.205775427307692 to 0.19270447595122, Range = 0.398479903258912

* TimeDomainBodyGyroscopeMeanYaxis
  -
  - 12 to 20, numeric
  - -0.204205356087805 to 0.0274707556666667, Range = 0.231676111754472

* TimeDomainBodyGyroscopeMeanZaxis
  -
  - 11 to 21, numeric
  - -0.0724546025804878 to 0.179102058245614, Range = 0.251556660826102

* TimeDomainBodyGyroscopeStandardDeviationXaxis
  -
  - 12 to 19, numeric
  - -0.994276591304348 to 0.267657219333333, Range = 1.26193381063768

* TimeDomainBodyGyroscopeStandardDeviationYaxis
  -
  - 11 to 19, numeric
  - -0.994210471914894 to 0.476518714444444, Range = 1.47072918635934

* TimeDomainBodyGyroscopeStandardDeviationZaxis
  -
  - 11 to 19, numeric
  - -0.985538363333333 to 0.564875818162963, Range = 1.5504141814963

* TimeDomainBodyGyroscopeJerkMeanXaxis
  -
  - 12 to 19, numeric
  - -0.157212539189362 to -0.0220916265065217, Range = 0.13512091268284

* TimeDomainBodyGyroscopeJerkMeanYaxis
  -
  - 12 to 19, numeric
  - -0.0768089915604167 to -0.0132022768074468, Range = 0.0636067147529699

* TimeDomainBodyGyroscopeJerkMeanZaxis
  -
  - 11 to 20, numeric
  - -0.0924998531372549 to -0.00694066389361702, Range = 0.0855591892436379

* TimeDomainBodyGyroscopeJerkStandardDeviationXaxis
  -
  - 12 to 18, numeric
  - -0.99654254057971 to 0.179148649684615, Range = 1.17569119026433

* TimeDomainBodyGyroscopeJerkStandardDeviationYaxis
  -
  - 11 to 19, numeric
  - -0.997081575652174 to 0.295945926186441, Range = 1.29302750183862

* TimeDomainBodyGyroscopeJerkStandardDeviationZaxis
  -
  - 11 to 19, numeric
  - -0.995380794637681 to 0.193206498960417, Range = 1.1885872935981

* TimeDomainBodyAccelerometerMagnitudeMean
  -
  - 11 to 21, numeric
  - -0.986493196666667 to 0.644604325128205, Range = 1.63109752179487

* TimeDomainBodyAccelerometerMagnitudeStandardDeviation
  -
  - 10 to 19, numeric
  - -0.986464542615385 to 0.428405922622222, Range = 1.41487046523761

* TimeDomainGravityAccelerometerMagnitudeMean
  -
  - 11 to 21, numeric
  - -0.986493196666667 to 0.644604325128205, Range = 1.63109752179487

* TimeDomainGravityAccelerometerMagnitudeStandardDeviation
  -
  - 10 to 19, numeric
  - -0.986464542615385 to 0.428405922622222, Range = 1.41487046523761

* TimeDomainBodyAccelerometerJerkMagnitudeMean
  -
  - 11 to 19, numeric
  - -0.99281471515625 to 0.434490400974359, Range = 1.42730511613061


* TimeDomainBodyAccelerometerJerkMagnitudeStandardDeviation
  -
  - 11 to 19, numeric
  - -0.994646916811594 to 0.450612065720513, Range = 1.44525898253211

* TimeDomainBodyGyroscopeMagnitudeMean
  -
  - 10 to 19, numeric
  - -0.980740846769231 to 0.418004608615385, Range = 1.39874545538462

* TimeDomainBodyGyroscopeMagnitudeStandardDeviation
  -
  - 12 to 19, numeric
  - -0.981372675614035 to 0.299975979851852, Range = 1.28134865546589

* TimeDomainBodyGyroscopeJerkMagnitudeMean
  -
  - 11 to 19, numeric
  - -0.997322526811594 to 0.0875816618205128, Range = 1.08490418863211

* TimeDomainBodyGyroscopeJerkMagnitudeStandardDeviation
  -
  - 11 to 19, numeric
  - -0.997666071594203 to 0.250173204117966, Range = 1.24783927571217

* FastFourierTransformBodyAccelerometerMeanXaxis
  -
  - 11 to 19, numeric
  - -0.995249932641509 to 0.537012022051282, Range = 1.53226195469279

* FastFourierTransformBodyAccelerometerMeanYaxis
  -
  - 10 to 20, numeric
  - -0.989034304057971 to 0.524187686888889, Range = 1.51322199094686

* FastFourierTransformBodyAccelerometerMeanZaxis
  -
  - 11 to 19, numeric
  - -0.989473926666667 to 0.280735952206667, Range = 1.27020987887333

* FastFourierTransformBodyAccelerometerStandardDeviationXaxis
  -
  - 11 to 20, numeric
  - -0.996604570307692 to 0.658506543333333, Range = 1.65511111364103

* FastFourierTransformBodyAccelerometerStandardDeviationYaxis
  -
  - 10 to 20, numeric
  - -0.990680395362319 to 0.560191344, Range = 1.55087173936232

* FastFourierTransformBodyAccelerometerStandardDeviationZaxis
  -
  - 11 to 19, numeric
  - -0.987224804307692 to 0.687124163703704, Range = 1.6743489680114

* FastFourierTransformBodyAccelerometerMeanFrequencyXaxis
  -
  - 12 to 21, numeric
  - -0.635913046346154 to 0.159123629063636, Range = 0.79503667540979

* FastFourierTransformBodyAccelerometerMeanFrequencyYaxis
  -
  - 12 to 20, numeric
  - -0.379518455061538 to 0.466528231788462, Range = 0.84604668685

* FastFourierTransformBodyAccelerometerMeanFrequencyZaxis
  -
  - 11 to 20, numeric
  - -0.520114793584906 to 0.402532553395833, Range = 0.922647346980739

* FastFourierTransformBodyAccelerometerJerkMeanXaxis
  -
  - 11 to 20, numeric
  - -0.994630797358491 to 0.474317256051282, Range = 1.46894805340977

* FastFourierTransformBodyAccelerometerJerkMeanYaxis
  -
  - 11 to 20, numeric
  - -0.989398823913043 to 0.276716853307692, Range = 1.26611567722074

* FastFourierTransformBodyAccelerometerJerkMeanZaxis
  -
  - 11 to 19, numeric
  - -0.992018447826087 to 0.157775692377778, Range = 1.14979414020386

* FastFourierTransformBodyAccelerometerJerkStandardDeviationXaxis
  -
  - 11 to 20, numeric
  - -0.995073759245283 to 0.476803887476923, Range = 1.47187764672221

* FastFourierTransformBodyAccelerometerJerkStandardDeviationYaxis
  -
  - 11 to 20, numeric
  - -0.990468082753623 to 0.349771285415897, Range = 1.34023936816952

* FastFourierTransformBodyAccelerometerJerkStandardDeviationZaxis
  -
  - 11 to 20, numeric
  - -0.993107759855072 to -0.00623647528983051, Range = 0.986871284565242

* FastFourierTransformBodyAccelerometerJerkMeanFrequencyXaxis
  -
  - 11 to 19, numeric
  - -0.576044001875 to 0.331449281481482, Range = 0.907493283356482

* FastFourierTransformBodyAccelerometerJerkMeanFrequencyYaxis
  -
  - 13 to 20, numeric
  - -0.601971415384615 to 0.195677336307692, Range = 0.797648751692307

* FastFourierTransformBodyAccelerometerJerkMeanFrequencyZaxis
  -
  - 11 to 20, numeric
  - -0.62755547372549 to 0.230107945944444, Range = 0.857663419669934

* FastFourierTransformBodyGyroscopeMeanXaxis
  -
  - 11 to 19, numeric
  - -0.99312260884058 to 0.474962448333333, Range = 1.46808505717391

* FastFourierTransformBodyGyroscopeMeanYaxis
  -
  - 11 to 19, numeric
  - -0.994025488297872 to 0.328817010088889, Range = 1.32284249838676

* FastFourierTransformBodyGyroscopeMeanZaxis
  -
  - 11 to 19, numeric
  - -0.985957788 to 0.492414379822222, Range = 1.47837216782222

* FastFourierTransformBodyGyroscopeStandardDeviationXaxis
  -
  - 11 to 18, numeric
  - -0.994652185217391 to 0.196613286661538, Range = 1.19126547187893

* FastFourierTransformBodyGyroscopeStandardDeviationYaxis
  -
  - 11 to 19, numeric
  - -0.994353086595745 to 0.646233637037037, Range = 1.64058672363278

* FastFourierTransformBodyGyroscopeStandardDeviationZaxis
  -
  - 10 to 19, numeric
  - -0.986725274871795 to 0.522454216314815, Range = 1.50917949118661

* FastFourierTransformBodyGyroscopeMeanFrequencyXaxis
  -
  - 12 to 20, numeric
  - -0.395770150677419 to 0.249209411510602, Range = 0.644979562188021

* FastFourierTransformBodyGyroscopeMeanFrequencyYaxis
  -
  - 12 to 20, numeric
  - -0.666814815306122 to 0.273141323315789, Range = 0.939956138621911

* FastFourierTransformBodyGyroscopeMeanFrequencyZaxis
  -
  - 11 to 20, numeric
  - -0.507490866734694 to 0.3770740968, Range = 0.884564963534694

* FastFourierTransformBodyAccelerometerMagnitudeMean
  -
  - 11 to 20, numeric
  - -0.986800645362319 to 0.586637550769231, Range = 1.57343819613155

* FastFourierTransformBodyAccelerometerMagnitudeStandardDeviation
  -
  - 11 to 20, numeric
  - -0.987648484461539 to 0.178684580868889, Range = 1.16633306533043

* FastFourierTransformBodyAccelerometerMagnitudeMeanFrequency
  -
  - 10 to 21, numeric
  - -0.312338030213846 to 0.435846931652174, Range = 0.74818496186602

* FastFourierTransformBodyBodyAccelerometerJerkMagnitudeMean
  -
  - 12 to 20, numeric
  - -0.993998275797101 to 0.538404846128205, Range = 1.53240312192531

* FastFourierTransformBodyBodyAccelerometerJerkMagnitudeStandardDeviation
  -
  - 11 to 19, numeric
  - -0.994366667681159 to 0.316346415348718, Range = 1.31071308302988

* FastFourierTransformBodyBodyAccelerometerJerkMagnitudeMeanFrequency
  -
  - 12 to 21, numeric
  - -0.125210388757581 to 0.488088499666667, Range = 0.613298888424248

* FastFourierTransformBodyBodyGyroscopeMagnitudeMean
  -
  - 9 to 20, numeric
  - -0.986535242105263 to 0.203979764835897, Range = 1.19051500694116

* FastFourierTransformBodyBodyGyroscopeMagnitudeStandardDeviation
  -
  - 9 to 18, numeric
  - -0.981468841692308 to 0.236659662496296, Range = 1.2181285041886

* FastFourierTransformBodyBodyGyroscopeMagnitudeMeanFrequency
  -
  - 13 to 21, numeric
  - -0.456638670923077 to 0.409521611525424, Range = 0.866160282448501

* FastFourierTransformBodyBodyGyroscopeJerkMagnitudeMean
  -
  - 11 to 19, numeric
  - -0.997617389275362 to 0.146618569064407, Range = 1.14423595833977

* FastFourierTransformBodyBodyGyroscopeJerkMagnitudeStandardDeviation
  -
  - 10 to 19, numeric
  - -0.99758523057971 to 0.287834616098305, Range = 1.28541984667802

* FastFourierTransformBodyBodyGyroscopeJerkMagnitudeMeanFrequency
  -
  - 11 to 21, numeric
  - -0.182923596577778 to 0.426301679855072, Range = 0.60922527643285

* TimeDomainAccelerometerMeanGravity
  -
  - 11 to 21, numeric
  - -0.163042575021277 to 0.129153963587755, Range = 0.292196538609032

* TimeDomainBodyAccelerometerJerkMean
  -
  - 11 to 21, numeric
  - -0.120553975717391 to 0.203259965863014, Range = 0.323813941580405

* TimeDomainBodyGyroscopeMeanGravityMean
  -
  - 11 to 21, numeric
  - -0.389305120341463 to 0.444101172307692, Range = 0.833406292649155

* TimeDomainGyroscopeJerkMeanGravityMean
  -
  - 12 to 21, numeric
  - -0.223672056052174 to 0.182384802705085, Range = 0.406056858757259

* XaxisGravityMean
  -
  - 11 to 18, numeric
  - -0.947116527659574 to 0.737784354819277, Range = 1.68490088247885

* YaxisGravityMean
  -
  - 10 to 21, numeric
  - -0.874567701929825 to 0.42476122745098, Range = 1.29932892938081

* ZaxisGravityMean
  -
  - 11 to 21, numeric
  - -0.873649367 to 0.390444368518519, Range = 1.26409373551852
