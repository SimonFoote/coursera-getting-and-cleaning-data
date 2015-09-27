#Coursera Getting and Cleaning Data - Code Book

##Assignment Overview
The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a series of yes/no questions related to the project. You will be required to submit: 1) a tidy data set as described below, 2) a link to a Github repository with your script for performing the analysis, and 3) a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md. You should also include a README.md in the repo with your scripts. This repo explains how all of the scripts work and how they are connected.  

One of the most exciting areas in all of data science right now is wearable computing - see for example this article . Companies like Fitbit, Nike, and Jawbone Up are racing to develop the most advanced algorithms to attract new users. The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained: 

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 

Here are the data for the project: 

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

##Script Steps

###1. Merges the training and the test sets to create one data set.
First all the Train data files are read in and the column names are set.
Then they are merged into one data set.

Next all the Test data files are read in and the column names are also set.
Then these are merged into one data set.

Lastly the Train and Test data sets are merged into a final data set.

###2. Extracts only the measurements on the mean and standard deviation for each measurement.
By extracting the column names and filtering them to only the required names, a logical vector can be used to extract only the required columns from the data set.


###3. Uses descriptive activity names to name the activities in the data set
By merging the ActivityType data to the data set, activity names can be joined.

###4. Appropriately labels the data set with descriptive variable names.
Next, we loop through all columns and replace the abbreviated text names with full meaningful descriptions.

###5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
Lastly, a subset of the data is taken from the orignal and the values summarised fro each activity and subject.
Which is exported to a textfile in the working directory.