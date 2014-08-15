Course Project of Getting and Cleaning Data course
--------------------------------------------------
In this document, the process of creating a tidy data set with the required fields as outlined in the project description is explained. The data was downloaded and unzipped in the working directory. The files used in the project are X train.txt, X test.txt, y test.txt, y train.txt, activity labels.txt, subject test.txt, subject train.txt. Readme.txt, features.txt, features info.txt, activity labels.txt were also used as reference. Below are the steps that were carried out:

1. Read in X train, X test, y train, y test, subject train, subject test files into R using read.table. 
2. Using cbind, merge subject train, y train, and x train data frames to get the training set data in place.
3. Using cbind, merge subject test, y test, and y train data frames to get the testing set data in place.
4. Using rbind combine the training and testing set data (10299 observations)- 1st requirement of the script as mentioned in the project description on the course website.
5. In the features.txt document, identified variables containing mean and standard deviation. Readme.txt and features_info.txt was used as a guide to faciliate identification of these variables. 76 variables were identified to be mean and standard deviation measurements.
6. Subsetting was used to extract only the variables containing mean and standard deviation measurements - 2nd requirement of the script as outlined in the project description on the course website.
7. Activities names from the activity labels.txt files were used in a 'for' loop in combination with 'if' statement to replace the numeric 'activity' values - 3rd requirement of the script as outlined in the project description on the course website.
8. Appropriate label names from features.txt (for the mean and standard deviation measurements) were used to provide descriptive names to the variable names - 4th requirement of the script as outlined in the project description on the course website.
9. Using the ddply function in the plyr package, average of each variable in the extracted data set was calculated for each subject and activity. This resulted in 180 observations for the 76 variables (mean and standard deviation measurements).
10. The tidy data set was stored in the tidydf data frame
11. The tidydf data frame was written out to a txt file using write.table command
