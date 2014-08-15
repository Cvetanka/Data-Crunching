# List of variables used in this script#

Here are presented the names and types of the variables used in this script. The names of the files with raw data used as an input in the analysis as well as complete work-flow is given in README file. 


Activity_Labels  - List (Corresponds to activity_labels.txt) dim(6 x 2)

Features – List (Corresponds to Features.txt) dim(561 x 2)

Test_SubjectTest – List (corresponds to subject_test) dim(2947 x 1)

Test_XTest – List (corresponds to X_test) dim(2947 x 561)

Test_yTest  - List (corresponds to y_test) dim(2947 x 1)

Test – List, created by merging all test data (Test_subjectTest, Test_yTest and  Test_XTest) dim(2947 x 81)

Train_SubjectTrain – List (corresponds to subject_train) dim(7352 x 1)

Train_XTrain  – List (corresponds to X_train) dim(7352 x 561)

Train_yTrain  - List (corresponds to y_train) dim(7352 x 1)

Train – List, created by merging all train data (Train_SubjectTrain, Train_yTrain, Train_XTrain) dim(7352 x 81)

Data  - Closure, obtained putting together Test and Train dim(10299 x 81)

Mean_Data – List, obtained after aggregating Mean_Data by Subject_ID and Activity, contains cleaned, processed data dim(180 x 81)

Tidy – Output .txt file with processed data (content of Mean_Data) dim(180 x 81)







