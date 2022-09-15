# Getting and Cleaning Data - Course Project

This is the course project for the Getting and Cleaning Data Coursera course.

## Project Summary
The goal of this project is to create a tidy data data set with the help of R to analyze experimental results which were captured in the [Human Activity Recognition Using Smartphones](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones) study.

The run_analysis.R script should be run on the [data](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) and it will complete the following steps to transform the data into something that we are able to glean information out of.

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names.
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

## Repository Information
This repository contains 3 main files:


* run_analysis.R - This script is used to build up and perform the analysis on the required sample data.
* tidy.txt - This is the final output from the run_analysis.R script.  It contains a cleansed version of the sample data.
* CodeBook.md - Contains the definitions of each of the columns in our generated tidy.txt file.
