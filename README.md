# Running the run_analysis.R script

## Author:  Alexander McLin

This script was written for the Johns Hopkins Cleaning Data course taken in September 2015 on Coursera.org.

Version 1.0

## Disclaimer:

This script is provided without any warranty to the extent permitted by applicable law. You use it at your own risk.

## Purpose:

Merge and tidy up the dataset from UCI Machine Learning Repository located at <http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones>. A set of experiments performed using 30 volunteers using a Samsung Galaxy S II smartphone.

Each person performed 6 activities, WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING. Each activity was measured (by the Samsung smartphone) at a rate of 50Hz.

The signals were then sampled in fixed-width sliding windows resulting in 128 data points per window.

The 128 data points were then futher processed into a feature vector of 561 measurements. One feature vector per window.

The training and test datasets are comprised of the feature vectors derived from the windows generated by sampling the signals acquired during the experiments.

More information about the experimental setup and data collection can be found at the UCI Machine Learning Repository URL.

This R script merges all the training and test sets along with relevant labels into a single tidy dataset for futher analysis.

Using the tidy dataset, the script will extract the mean and standard deviation measurements. Label each value with a descriptive name, subject and activity identifiers will also be included.

Finally, the script will average all the extracted means and standard deviation values for each activity and subject and output the averages as a text file.

## Requirements:

The experimental dataset must be available as a directory labeled UCI HAR Dataset in the same working directory run_analysis.R script is located in.

The UCI HAR Dataset directory has a certain directory hierarchy which run_analysis.R is already familiar with.

## How to Run:

Simply invoke run_analyis.R using R - assuming it's in same directory as the UCI HAR Dataset, then it will generate a text file called run_analysis_tidydataset which contains the subject, activity identifiers, and the averages of the measured mean and standard deviation values.

You can run the script in two ways. Invoke R on the command-line then execute source("run_analysis.R") or invoke R --vanilla < run_analysis.R on the command-line.
