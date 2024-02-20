Lead Score Case Study 

Problem statement 

X EduLcation gets a lot of leads there are a lot of columns which have high number of missing values. Clearly, these columns are not useful. Since, there are 9000 datapoints in our data frame, let's eliminate the columns having greater than 3000 missing values as they are of no use to us. CEO’s target for lead conversion rate is around 80%.
There are a few columns in which there is a level called 'Select' which basically means that the student had not selected the option for that column which is why it shows 'Select'. To get some useful data we must make compulsory selection. Likewise, Customer occupation, Specialization, etc.

Approach 

Columns with >40% nulls were dropped. Value counts within categorical columns were checked to decide appropriate action: if imputation causes skew, then column was dropped, created new category (others), impute high frequency value, drop columns that don’t add any value.
Numerical categorical data were imputed with mode and columns with only one unique response from customer were dropped.
Data imbalance checked- only 38.5% leads converted.
Created dummy features (one-hot encoded) for categorical variables
Used RFE to reduce variables from 48 to 15. This will make dataframe more manageable.
Confusion matrix was made and cut off point of 0.345 was selected based on accuracy, sensitivity and specificity plot. This cut off gave accuracy, specificity and precision all around 80%. Whereas precision recall view gave less performance metrics around 75%.
Making Predictions on Test: Scaling and predicting using final model.
Lead score was assigned.
