# Code Book

This code book describes the files and data used in the course project of Coursera's Getting and cleaning data course.

## Overview

The origin of the data used is from an experiment where 30 volunteers, wearing a smartphone on the waist, performed six diferent activities.

The original description of the data set, including how the experiment was carried out, can be found in http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
The dataset used in this project was obtained from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

## Files used

* activity_labels.txt: Names and IDs for each of the 6 activities.

* features.txt: Names of the 561 diferent measures.

* X_test.txt: Observations of the 561 features for testing.

* y_test.txt: A integer vector, denoting the ID of the activity related to the observations in X_test.txt.

* subject_test.txt: A integer vector, denoting the ID of the volunteer related to each of the observations in X_test.txt.

* X_train.txt: Observations of the 561 features for training.

* y_train.txt: A integer vector, denoting the ID of the activity related to the observations in X_train.txt.

* subject_train.txt: A integer vector, denoting the ID of the volunteer related to each of the observations in X_train.txt.

There are other files in the zip file that has not been use in this project.

## Design of the R script

1. Reading of all the data files needed in the script, and appropiate naming of the columns.
  1.2 Merge of all the test and train sets into one unique dataset.
2. Removal of all the measure columns that did not contain the exact string "mean()" or "std()".
3. The values of the activity IDs column are transform into their real names of the activity.
4. Creation of a tidy data set containing the mean of each feature for each subject and activity.
5. Writting of a txt file whith the tidy data set.
