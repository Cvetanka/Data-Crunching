# List of variables used in this script#

This document contains the names and types of the variables used in this script. The names of the files with raw data used as an input in the analysis as well as complete work-flow are given in README file. 


Activity_Labels  - List (Corresponds to activity_labels.txt. Names of the activities as described in README.md) dim(6 x 2)

Features – List (Corresponds to Features.txt. Gives the names of all variables) dim(561 x 2)

Test_SubjectTest – List (corresponds to subject_test. Denotes the subject who did paricular activity) dim(2947 x 1)

Test_XTest – List (corresponds to X_test. Measurement data) dim(2947 x 561) After extracting the values with mean and std dim(2947 x 79)

Test_yTest  - List (corresponds to y_test. Test labels, each number corresponds to some activity) dim(2947 x 1)

Test – List, created by merging all test data (Test_subjectTest, Test_yTest and  Test_XTest. Complete and processed test data sets with mean and std values) dim(2947 x 81)

Train_SubjectTrain – List (corresponds to subject_train. Denotes the subject who did paricular activity) dim(7352 x 1)

Train_XTrain  – List (corresponds to X_train. Measurement data) dim(7352 x 561) After extracting the values with mean and std dim(2947 x 79)

Train_yTrain  - List (corresponds to y_train. Test labels, each number corresponds to some activity) dim(7352 x 1)

Train – List, created by merging all train data (Train_SubjectTrain, Train_yTrain, Train_XTrain. Complete and processed train data with mean and std values) dim(7352 x 81)

Data  - Closure, obtained putting together Test and Train dim(10299 x 81)

Mean_Data – List, obtained after aggregating Mean_Data by Subject_ID and Activity, contains cleaned and fully processed data with average values/performations of all mean and std variables by subject and activity  dim(180 x 81)

Tidy – Output .txt file with the content of Mean_Data dim(180 x 81)







