# CodeBook.md

# run_analysis.R 

* downloads required data from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
* unzips the file
* creates output folder
* loads 'features.txt' used for columns
* loads 'X_train.txt', 'y_train.txt', 'subject_train.txt' with read.table
* X_train contains the data using the feature data set as columns
* y_train contains the activity labels
* subject_train contains the ids
* loads and appends test dataset using 'X_test.txt', 'y_test.txt', 'subject_test.txt' with read.table
* X_test contains the data using the feature data set as columns
* y_test contains the activity labels
* subject_test contains the ids
* appends train and test data
* rearrange the data using id
* extracts only the measurements on the mean and standard deviation for each measurement 
* loads activity_labels.txt
* changes the data activity row to use the activity labels
* calculates the average of each variable for each activity and each subject using ddply from pkyr package
* writes the tidy dataset into 'tidy_dataset.txt' with write.table


# tidy_dataset.txt
  read with read.table

variables:
	
 [1] "id"
 [2] "activity"
 [3] "tBodyAcc.mean...X_mean"
 [4] "tBodyAcc.correlation...X.Z_mean"
 [5] "tBodyAcc.correlation...Y.Z_mean"
 [6] "tGravityAcc.mean...X_mean"
 [7] "tGravityAcc.correlation...X.Z_mean"
 [8] "tGravityAcc.correlation...Y.Z_mean"
 [9] "tBodyAccJerk.mean...X_mean"
[10] "tBodyAccJerk.correlation...X.Z_mean"
[11] "tBodyAccJerk.correlation...Y.Z_mean"
[12] "tBodyGyro.mean...X_mean"
[13] "tBodyGyro.correlation...X.Z_mean"
[14] "tBodyGyro.correlation...Y.Z_mean"
[15] "tBodyGyroJerk.mean...X_mean"
[16] "tBodyGyroJerk.correlation...X.Z_mean"
[17] "tBodyAccMag.arCoeff..3_mean"
[18] "tGravityAccMag.arCoeff..3_mean"
[19] "tBodyAccJerkMag.arCoeff..3_mean"
[20] "tBodyGyroMag.arCoeff..3_mean"
[21] "tBodyGyroJerkMag.arCoeff..3_mean"
[22] "tBodyGyroJerkMag.arCoeff..4_mean"
[23] "fBodyAcc.mean...X_mean"
[24] "fBodyAcc.bandsEnergy...1.24.2_mean"
[25] "fBodyAcc.bandsEnergy...25.48.2_mean"
[26] "fBodyAccJerk.mean...X_mean"
[27] "fBodyAccJerk.bandsEnergy...1.24.2_mean"
[28] "fBodyAccJerk.bandsEnergy...25.48.2_mean"
[29] "fBodyGyro.mean...X_mean"
[30] "fBodyGyro.bandsEnergy...1.24.2_mean"
[31] "fBodyAccMag.skewness.._mean"
[32] "fBodyBodyAccJerkMag.skewness.._mean"
[33] "fBodyBodyGyroMag.skewness.._mean"
