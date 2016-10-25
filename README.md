# Getting and Cleaning Data Project

##Purpose
The purpose of this repository is to describe the process of cleaning the Human Activity Recognition Using Smartphones Dataset (full description of the dataset can be found [here](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones) and the data zipfile [here](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)). This repository also serves as a fulfillment toward Getting and Cleaning Data course offered by Johns Hopkins University on Coursera.

##Content
The content of this repository is:
* this readme file    : README.md
* 1(one) tidy dataset : tidy.txt
* 1(one) code book    : CodeBook.md
* 1(one) R script     : run_analysis.R

The tidy dataset contains the average of each variable for each activity and each subject.

The code book (CodeBook.md) explains the variables one by one.

The R script (run_analysis.R) can be run to reproduce the same tidy dataset in this repository. Explicitly, these are the things that the script does:

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Puts descriptive activity names to name the activities in the data set
4. Labels the data set with descriptive variable names.
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

##Getting the Data
In order for you to execute the analysis script, run the following to download the data.
```r
download.file("https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip","UCI HAR Dataset.zip", method = "curl")
unzip("UCI HAR Dataset.zip", exdir = ".")
setwd("UCI HAR Dataset/")
```
Afterward, you can execute run_analysis.R in the working directory.
```r
source("run_analysis.R") #make sure you put the script file in the UCI HAR Dataset directory
```

##Analysis Explanation

See CodeBook.md

##Acknowledgements

[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

[2] David Hood's helpful advice on the course in [his blog](https://thoughtfulbloke.wordpress.com/2015/09/09/getting-and-cleaning-the-assignment/)

[3] The mentors and the course community in the forum for providing guidance along the course
