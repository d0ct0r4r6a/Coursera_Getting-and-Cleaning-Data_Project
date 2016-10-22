#Code Book

In the 2nd step, after merging the training and the test sets, the mean and standard deviation for each measurement is transferred (subsetted) to a new data frame. How do we select them? It is stated in features_info.txt that mean() describes Mean value & std() describes Standard deviation. So we only extract those variables with mean() and std() in their name.

Activity names are conveniently extracted from activity_labels.txt

## Tidy Data Set (tidy.txt)

###Variables
**subjectID** (int) [1-30]

Identifier of the subject who carried out the experiment

**activityName** (factor) 6 levels

"laying"
"sitting"
"standing"
"walking"
"walking_downstairs"
"walking_upstairs" 

Activities performed by subjects

**variable** (factor) 66 levels

Each variable will be written in this form:

**t|f.VariableName.(D-Axis).Mean|Std**

**|** means either it takes the value to its left or right.

**t|f** specifies if the measurement is in the time or frequency domain, respectively.

**VariableName** is the name of the measurement variable/feature

**(D-Axis)** denotes the direction of each measurement whenever appropriate.

**Mean|Std** denotes whether that is the mean or standard deviation of the variable, respectively.

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
