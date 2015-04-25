# Getting-and-cleaning-data
## Objective
The objective is to create a R script which will do the below mentioned processing

1. Merges the training and the test sets to create one data set
2. Extracts only the measurements on the mean and standard deviation for each measurement
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each      	activity and each subject


##Steps Involved in the R script
- Step 1: Install and load the package reshape2 <br>
          Install the package only if it is not present on your system. This is a one time operation.<br>
          Load the package every time you start a new session.<br>
- Step 2: get the clean data from test dataset<br>
    * A clean data set is created with the necessary columns from test data set.
    * 2 new columns are added containing the data of Activity and Subject data sets.   
- Step 3: get the clean data from train dataset
    * A clean data set is created with the necessary columns from train data set.
    * 2 new columns are added containing the data of Activity and Subject data sets.
- Step 4: Merge the two datasets to create one data set.
	* Datasets created in step 2 and 3 are merged together
- Step 5: Create a tidy data set with the average of each variable for each activity and each subject.
- Step 6: Write the tidy data set created in step 5 to a .txt file.

##Steps to run the Script:
- Step 1: download the R script run_analysis.R
- Step 2: Keep it at the same location where the folder containing the data is present.
- Step 3: Make sure the name of the folder containing the data is "UCI HAR Dataset"
- Step 4: Load the script using source("run_analysis.R")
- Step 5: Run the function run_analysis().
