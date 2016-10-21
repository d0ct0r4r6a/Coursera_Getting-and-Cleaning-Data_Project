All the .txt files mentioned in this section are those that are in the .zip file.

In the 2nd step, after merging the training and the test sets, the mean and standard deviation for each measurement is transferred (subsetted) to a new data frame. How do we select them? It is stated in features_info.txt that mean() describes Mean value & std() describes Standard deviation. So we only extract those variables with mean() and std() in their name.

Activity names are conveniently extracted from activity_labels.txt

In naming the variables, we extend the contracted form of the variables. They will have this form:

**t|f.VariableName.(D-Axis).Mean|Std**

**|** means either it takes the value to its left or right.

The first section **t|f** specifies if the measurement is in the time or frequency domain, respectively.

The section **(D-Axis)** denotes the direction of each measurement whenever appropriate.

The last section **Mean|Std** denotes whether that is the mean or standard deviation of the variable, respectively.
