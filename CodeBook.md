Variable Selection 
=================

The variables selected come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

These signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

tBodyAcc-XYZ<br>
tGravityAcc-XYZ<br>
tBodyAccJerk-XYZ<br>
tBodyGyro-XYZ<br>
tBodyGyroJerk-XYZ<br>
tBodyAccMag<br>
tGravityAccMag<br>
tBodyAccJerkMag<br>
tBodyGyroMag<br>
tBodyGyroJerkMag<br>
fBodyAcc-XYZ<br>
fBodyAccJerk-XYZ<br>
fBodyGyro-XYZ<br>
fBodyAccMag<br>
fBodyAccJerkMag<br>
fBodyGyroMag<br>
fBodyGyroJerkMag<br>

The set of variables that were estimated from these signals are: 

mean(): Mean value<br>
std(): Standard deviation

Additional vectors obtained by averaging the signals in a signal window sample. These are used on the angle() variable:

gravityMean<br>
tBodyAccMean<br>
tBodyAccJerkMean<br>
tBodyGyroMean<br>
tBodyGyroJerkMean<br>

##Complete Variables list:
1   activity<br>
2   subject<br>
3   tBodyAcc-mean()-X<br>
4   tBodyAcc-mean()-Y<br>
5   tBodyAcc-mean()-Z<br>
6   tBodyAcc-std()-X<br>
7   tBodyAcc-std()-Y<br>
8   tBodyAcc-std()-Z<br>
9   tGravityAcc-mean()-X<br>
10  tGravityAcc-mean()-Y<br>
11  tGravityAcc-mean()-Z<br>
12  tGravityAcc-std()-X<br>
13  tGravityAcc-std()-Y<br>
14  tGravityAcc-std()-Z<br>
15  tBodyAccJerk-mean()-X<br>
16  tBodyAccJerk-mean()-Y<br>
17  tBodyAccJerk-mean()-Z<br>
18  tBodyAccJerk-std()-X<br>
19  tBodyAccJerk-std()-Y<br>
20  tBodyAccJerk-std()-Z<br>
21  tBodyGyro-mean()-X<br>
22  tBodyGyro-mean()-Y<br>
23  tBodyGyro-mean()-Z<br>
24  tBodyGyro-std()-X<br>
25  tBodyGyro-std()-Y<br>
26  tBodyGyro-std()-Z<br>
27  tBodyGyroJerk-mean()-X<br>
28  tBodyGyroJerk-mean()-Y<br>
29  tBodyGyroJerk-mean()-Z<br>
30  tBodyGyroJerk-std()-X<br>
31  tBodyGyroJerk-std()-Y<br>
32  tBodyGyroJerk-std()-Z<br>
33  tBodyAccMag-mean()<br>
34  tBodyAccMag-std()<br>
35  tGravityAccMag-mean()<br>
36  tGravityAccMag-std()<br>
37  tBodyAccJerkMag-mean()<br>
38  tBodyAccJerkMag-std()<br>
39  tBodyAccJerkMag-mad()<br>
40  tBodyGyroMag-mean()<br>
41  tBodyGyroMag-std()<br>
42  tBodyGyroJerkMag-mean()<br>
43  tBodyGyroJerkMag-std()<br>
44  fBodyAcc-mean()-X<br>
45  fBodyAcc-mean()-Y<br>
46  fBodyAcc-mean()-Z<br>
47  fBodyAcc-std()-X<br>
48  fBodyAcc-std()-Y<br>
49  fBodyAcc-std()-Z<br>
50  fBodyAccJerk-mean()-X<br>
51  fBodyAccJerk-mean()-Y<br>
52  fBodyAccJerk-mean()-Z<br>
53  fBodyAccJerk-std()-X<br>
54  fBodyAccJerk-std()-Y<br>
55  fBodyAccJerk-std()-Z<br>
56  fBodyGyro-mean()-X<br>
57  fBodyGyro-mean()-Y<br>
58  fBodyGyro-mean()-Z<br>
59  fBodyGyro-std()-X<br>
60  fBodyGyro-std()-Y<br>
61  fBodyGyro-std()-Z<br>
62  fBodyAccMag-mean()<br>
63  fBodyAccMag-std()<br>
64  fBodyBodyAccJerkMag-mean()<br>
65  fBodyBodyAccJerkMag-std()<br>
66  fBodyBodyGyroMag-mean()<br>
67  fBodyBodyGyroMag-std()<br>
68  fBodyBodyGyroJerkMag-mean()<br>
69  fBodyBodyGyroJerkMag-std()<br>  

##Transformations Done:

- Step 1: creating clean data file for the test data set
  * Create a clean dataset from the needed columns of the test dataset.
  * Create and merge the activity codes dataset with clean data set.
  * Create and Merge the subject dataset with clean dataset
  * Convert the activity column into a factor
- Step 2: creating clean data file for the train data set
  * Create a clean dataset from the needed columns of the train dataset
  * Create and merge the activity codes dataset with clean data set
  * Create and Merge the subject dataset with clean dataset
  * Convert the activity column into a factor
- Step 3:Merging the the two clean datasets obtained from Step 2 and Step 3
- Step 4: Obtaining average of each variable for each activity and each subject
- Step 5: Write the final tide data set to the file TideDataset.txt
