# Code Book
The `run_analysis.R` script performs the data preparation and then followed by the steps required as described in the course project’s definition.

## Dataset download
Dataset downloaded and extracted under the folder called `UCI HAR Dataset`


## Assign each data to variables
* `features` <- `features.txt`: 561 rows, 2 variables
* `activities` <- `activity_labels.txt`: 6 rows, 2 variables
* `subject_test` <- `test/subject_test.txt`: 2947 rows, 1 variable
* `x_test` <- `test/X_test.txt`: 2947 rows, 561 variables
* `y_test` <- `test/y_test.txt` : 2947 rows, 1 variables
* `subject_train` <- `test/subject_train.txt`: 7352 rows, 1 variable
* `x_train` <- `test/X_train.txt` : 7352 rows, 561 variables
* `y_train` <- `test/y_train.txt`: 7352 rows, 1 variable

## Merges the training and the test sets to create a binding dataset
* `X` (10299 rows, 561 columns) is created by merging `x_train` and `x_test` using `rbind()` function
* `Y` (10299 rows, 1 column) is created by merging `y_train` and y_test using `rbind() function
* `Subject` (10299 rows, 1 column) is created by merging `subject_train` and `subject_test` using `rbind()` function
* `Merged_Data` (10299 rows, 563 column) is created by merging Subject, `Y` and `X` using `cbind()` function

## Extracts only the measurements on the mean and standard deviation for each measurement
`TidyData` (10299 rows, 88 columns) is created by subsetting `Merged_Data`, selecting only columns: subject, code and the measurements on the mean and standard deviation (std) for each measurement

## Uses descriptive activity names to name the activities in the data set
Entire numbers in code column of the `TidyData` replaced with corresponding activity taken from second column of the activities variable

## Appropriately labels the dataset with descriptive variable names
code column in `TidyData` renamed into activities
* All Acc in column’s name replaced by Accelerometer
* All Gyro in column’s name replaced by Gyroscope
* All BodyBody in column’s name replaced by Body
* All Mag in column’s name replaced by Magnitude
* All start with character f in column’s name replaced by Frequency
* All start with character t in column’s name replaced by Time

## From the dataset in step 4, creates a second, independent tidy dataset with the average of each variable for each activity and each subject
`FinalData` (180 rows, 88 variables) is created by sumarizing `TidyData` taking the means of each variable for each activity and each subject, after groupped by subject and activity.
Export `FinalData` into `FinalData.txt` file.
