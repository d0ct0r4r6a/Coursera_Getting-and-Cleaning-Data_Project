#Code Book

This code book describes the steps taken for the analysis, the tidy data set, and other related information. One vital detail about the tidy data set is that it is a **NARROW TIDY DATA SET**.

## Analysis

Firstly, we begin with extracting the activity names and feature names from activity_labels.txt and features.txt respectively. Then we collect and combine the training and test data sets in the train and test directory. The combined data set contains a variable named 'observationPurpose' to distinguish training and test observations, but it is remove in subsequent steps to ease our analysis. We also swap the numerical labels for the activity with the activity name to improve clarity.

Next, the mean and standard deviation for each measurement is transferred (subsetted) to a new data frame. How do we select them? It is stated in features_info.txt that mean() describes Mean value & std() describes Standard deviation. So we only extract those variables with mean() and std() in their name.

In giving descriptive names for the features, we came up with a format to explain the measurement feature in the data set. The format is explained in the tidy data set section below.

Finally, the average of each feature for each subject and each activity is measured and put in the **average** column. The feature units are explained below. The resulting data frame is 'written' to a .txt file called tidy.txt in a tab-separated format.

## Tidy Data Set (tidy.txt)

The tidy dataset comprises a dataframe which dimensions are 11880 (observations) by 4 (variables). The number of observations are derived from getting the average of each feature for each subject and each activity i.e. 66 features x 30 subjects x 6 activities.

###Variables

**subjectID** (int) : identifier of the subject who carried out the experiment

**activityName** (factor, 6 levels) : activities performed by subjects

[1] "laying"
[2] "sitting"
[3] "standing"
[4] "walking"
[5] "walking_downstairs"
[6] "walking_upstairs" 

**feature** (factor, 66 levels) : measurement features containing mean() and std() in the original dataset

Format:

*t|f.FeatureName.(D-Axis).Mean|Std*

*|* means that it either takes the value to its left or right.

*t|f* specifies if the measurement is in the time or frequency domain, respectively.

*FeatureName* is the name of the measurement variable/feature

*(D-Axis)* denotes the direction of each measurement whenever appropriate.

*Mean|Std* denotes whether that is the mean or standard deviation of the feature, respectively.

 [1] t.BodyLinearAcceleration.X.Mean          
 [2] t.BodyLinearAcceleration.Y.Mean          
 [3] t.BodyLinearAcceleration.Z.Mean          
 [4] t.GravityLinearAcceleration.X.Mean       
 [5] t.GravityLinearAcceleration.Y.Mean       
 [6] t.GravityLinearAcceleration.Z.Mean       
 [7] t.BodyLinearJerk.X.Mean                  
 [8] t.BodyLinearJerk.Y.Mean                  
 [9] t.BodyLinearJerk.Z.Mean                  
[10] t.BodyAngularVelocity.X.Mean             
[11] t.BodyAngularVelocity.Y.Mean             
[12] t.BodyAngularVelocity.Z.Mean             
[13] t.BodyAngularJerk.X.Mean                 
[14] t.BodyAngularJerk.Y.Mean                 
[15] t.BodyAngularJerk.Z.Mean                 
[16] t.BodyLinearAccelerationMagnitude.Mean   
[17] t.GravityLinearAccelerationMagnitude.Mean
[18] t.BodyLinearJerkMagnitude.Mean           
[19] t.BodyAngularVelocityMagnitude.Mean      
[20] t.BodyAngularJerkMagnitude.Mean          
[21] f.BodyLinearAcceleration.X.Mean          
[22] f.BodyLinearAcceleration.Y.Mean          
[23] f.BodyLinearAcceleration.Z.Mean          
[24] f.BodyLinearJerk.X.Mean                  
[25] f.BodyLinearJerk.Y.Mean                  
[26] f.BodyLinearJerk.Z.Mean                  
[27] f.BodyAngularVelocity.X.Mean             
[28] f.BodyAngularVelocity.Y.Mean             
[29] f.BodyAngularVelocity.Z.Mean             
[30] f.BodyLinearAccelerationMagnitude.Mean   
[31] f.BodyLinearJerkMagnitude.Mean           
[32] f.BodyAngularVelocityMagnitude.Mean     
[33] f.BodyAngularJerkMagnitude.Mean          
[34] t.BodyLinearAcceleration.X.Std           
[35] t.BodyLinearAcceleration.Y.Std           
[36] t.BodyLinearAcceleration.Z.Std           
[37] t.GravityLinearAcceleration.X.Std        
[38] t.GravityLinearAcceleration.Y.Std        
[39] t.GravityLinearAcceleration.Z.Std        
[40] t.BodyLinearJerk.X.Std                   
[41] t.BodyLinearJerk.Y.Std                   
[42] t.BodyLinearJerk.Z.Std                   
[43] t.BodyAngularVelocity.X.Std              
[44] t.BodyAngularVelocity.Y.Std              
[45] t.BodyAngularVelocity.Z.Std              
[46] t.BodyAngularJerk.X.Std                  
[47] t.BodyAngularJerk.Y.Std                  
[48] t.BodyAngularJerk.Z.Std                  
[49] t.BodyLinearAccelerationMagnitude.Std    
[50] t.GravityLinearAccelerationMagnitude.Std 
[51] t.BodyLinearJerkMagnitude.Std            
[52] t.BodyAngularVelocityMagnitude.Std       
[53] t.BodyAngularJerkMagnitude.Std           
[54] f.BodyLinearAcceleration.X.Std           
[55] f.BodyLinearAcceleration.Y.Std           
[56] f.BodyLinearAcceleration.Z.Std           
[57] f.BodyLinearJerk.X.Std                   
[58] f.BodyLinearJerk.Y.Std                   
[59] f.BodyLinearJerk.Z.Std                   
[60] f.BodyAngularVelocity.X.Std              
[61] f.BodyAngularVelocity.Y.Std              
[62] f.BodyAngularVelocity.Z.Std              
[63] f.BodyLinearAccelerationMagnitude.Std    
[64] f.BodyLinearJerkMagnitude.Std            
[65] f.BodyAngularVelocityMagnitude.Std       
[66] f.BodyAngularJerkMagnitude.Std 

**average** (numeric) : average value of feature in each observation for each activity and for each subject.
The values are normalized and bounded within [-1,1].
Units (only applicable to those features starting with a 't'):
- feature with 'Acceleration' in its name is in standard gravity units 'g' 
- feature with 'AngularVelocity' in its name is in radians/second
- feature with 'LinearJerk' in its name is in 'g/second'
- feature with 'AngularJerk' in its name is in radians/(second^2)
