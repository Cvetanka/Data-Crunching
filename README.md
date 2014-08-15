Run-Analysis
============
This script is aimed to provide one clean, easy readable and workable data table out of raw data gathered in the experiment Human Activity Recognition Using Smartphones. The raw data consist of following files:

  *'features_info.txt': Shows information about the variables used on the feature vector. 
  
  *'features.txt': List of all features/variables. 
  
  *'activity_labels.txt': Links the class labels with their activity name (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING,        STANDING, LAYING) . 
  
  *'train/X_train.txt': Training set. 
  
  *'train/y_train.txt': Training labels. 
  
  *'test/X_test.txt': Test set. 
  
  *'test/y_test.txt': Test labels. 
  
  *'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from      1 to 30. 
  
  *'train/test/Inertial Signals/body_acc_x_train/test.txt': The body acceleration signal obtained by subtracting the gravity from       the total acceleration. 
  
  *'train/test/Inertial Signals/body_acc_x_train/test.txt': The body acceleration signal obtained by subtracting the gravity from       the total acceleration. 
  
  *'train/test/Inertial Signals/body_gyro_x_train/test.txt': The angular velocity vector measured by the gyroscope for each window        sample. The units are radians/second. 
  
  Note: The notation train/test means that files with same type of measurements exsist for both data sets.
  
  The following tasks have to be performed as stated in the assignment:
  
    Merges the training and the test sets to create one data set.
    
    Extracts only the measurements on the mean and standard deviation for each measurement. 
    
    Uses descriptive activity names to name the activities in the data set
    
    Appropriately labels the data set with descriptive variable names. 
    
    Creates a second, independent tidy data set with the average of each variable for each activity and each subject. 

The working procedure is as follows:

First data are downloaded and saved as a local copy. They are read in R with read.table() function. To get feeling about the structure of the data sets functions dim() and str() are used. The names of the variables provided by “features.txt” are assigned to the test and train variables (data frames X_train.txt and X_test.txt). Only the variables that contain information about mean values (the average value of some performance/measurement) and standard deviation (std) are of interest for this project and they are extracted with the function grepl(). 

Further all test data and train data (measurement data sets, training labels and subject_ID) are merged together in one big data frame. The functions used for that are cbind() and rbind().

The final goal is to average all data by subject and activity and write in the output one tidy data set. That is achieved with the function aggregate() and function write.table().

Final note: This script requires the packages: reshape, table and/or data.table.   

Note: It is recommended in the instruction, first to merge the data sets and than to extract mean and std values. However I found more convenient first to extract the desired values from the separate data sets and than to merge them in one big data frame. This deviation from recommended routine, by no means affects the final result. It was also in my understanding to extract all measurements that contain some mean value (like meanFreq) what has resulted in additional information and larger final (tidy) data table. 

