# Getting and Cleaning Data Project

Course project for the Getting and Cleaning Data Coursera course.

## Project Summary
The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set
The purpose of this project is to demonstrate abilitiy to cleaning data with the help of R to analyze experimental results. 
Full description of data is available at the site where the data was obtained in [Human Activity Recognition Using Smartphones](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones) study.

The run_analysis.R script should be run on the [data](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) and it will complete the following steps to transform the data into something that we are able to glean information out of.

1. Download the dataset from web if it does not already exist in the working directory.
2. Merges the training and the test sets to create one dataset.
3. Extracts only the measurements on the mean and standard deviation for each measurement.
4. Uses descriptive activity names to name the activities in the dataset
5. Appropriately labels the dataset with descriptive variable names.
6. From the data set in step 5, creates a second, independent tidy dataset with the average of each variable for each activity and each subject.

## Information
This repository contains 3 main files:

* run_analysis.R - This script is used to perform the analysis.
* tidy.txt - This is the final output.  It contains a cleansed version of the sample data.
* CodeBook.md - Contains the definitions of each of the columns in our generated tidy.txt file.
