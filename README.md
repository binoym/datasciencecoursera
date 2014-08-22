1) Download run_analysis.R

2) Internal path to be set to "C:/Personal/Data Scientist/GettingAndCleaning Data/Week2/" in your local system

3)Files to be downloaded and 
"UCI HAR Dataset/train/X_train.txt
"UCI HAR Dataset/train/Y_train.txt
"UCI HAR Dataset/train/subject_train.txt"
"UCI HAR Dataset/test/X_test.txt
"UCI HAR Dataset/test/Y_test.txt"
"UCI HAR Dataset/test/subject_test.txt"
"UCI HAR Dataset/activity_labels.txt"

Detailed Steps
4) Read features and make the feature names better suited for R with some substitutions

features = read.csv("UCI HAR Dataset/features.txt", sep="", header=FALSE)
features[,2] = gsub('-mean', 'Mean', features[,2])
features[,2] = gsub('-std', 'Std', features[,2])
features[,2] = gsub('[-()]', '', features[,2])

5) Merge training and test sets together

6) Get only the data on mean and std. dev.

7) First reduce the features table to what we want

8) Add the last two columns (subject and activity)


9) Remove the unwanted columns from allData

10) Add the column names (features) to allData

11) Remove the subject and activity column, since a mean of those has no use

12 ) Write/create tidy.txt with tab delimited.
