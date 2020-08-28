# Risky Business 

## Resampling Data:
1. Pull in DF data
2. Split the data into training and testing. 
    a. Create features and target(X df sans 'loan_status' column and Y as the target 'loan_status'). 
    b. Describe X data and check balance of target values to verify proper creation. 
    c. Split the data into training and testing by using sklearn's 'train_test_split'.
   
 Oversampling:
 1. Naive Random Oversampling
     2. Resample data with RandomOverSampler to randomly duplicate minority data to equal majority data. 
     3. Retrain the Logistic Regression model using the resampled data. 
     4. Print the confusion matrix, balanced accuracy score, and classification report. 
 2. SMOTE Oversampling
     3. SMOTE, Sythetic Minority Oversampling Technique, selects minority examples that are close in the feature space and draws a line between them and adds a new sample point. Picks 'k' nearest neighbors. 
     4. Resample the data with SMOTE and train the data. 
     5. Print the confusion matrix, balanced accuracy score, and classification report. 
     
Undersampling: 
 1. ClusterCentroids 
     2. Finds average groups of clustered features through KMeans algorithm. The closer to the centroid the more relevant the data point is considered to be. 
     3. Resample the data and train the logistic regression model. 
     4. Print the confusion matrix, balanced accuraacy score, and classification report. 
     

Combination Sampling:
 1. SMOTEENN: 
     2. Combination of SMOTE and Edited Nearest Neighbords to over and under sample. First oversamples by use of SMOTE, then cleans the data with ENN. 
     3. Resample the data and train the logistic regression model. 
     4. Print the confusion matrix, balanced accuracy score, and classification report. 

Questions:     
1. Best Balanced Accuracy Score: Naive Random Oversampling
2. Best Recall Score: SMOTE Oversampling
3. Best Geometric Mean Score: Naive Random Oversampling
     
     
## Ensemble Learning
1. read in and clean the data. 
2. split the data into training and testing. 

Balanced Random Forest Classifier: 
 1. Randomly under samples each bootstrap sample to balance. Uses values of y to automatrically adjust weights. Allows less chance for minority classes to be miss predicted in the random forest. 
 2. Resample the data. 
 3. Print the confusion matrix, balanced accuracy score, and imbalanced classification report. 
 4. List features sorted by importance for the Random Forest
 
Easy Ensemble AdaBoost Classifier: 
 1. Combines a series of low performing classifiers with the aim of creating an improved classifier. Combine serveral machine learning methods into a single predictive model to increase performance. Decrease variance through bagging, decrease bias through boosting, or improve predictions using stacking. 
 2. Train the classifier 
 3. Print the confusion matrix, balanced accuracy score, and imalanced classification report. 
 
Questions:
1. Best Balanced Accuracy Score: Easy Ensemble AdaBoost Classifier
2. Best Recall Score: Easy Ensemble AdaBoost Classifier
3. Best Geometric Mean Score: Easy ensemble AdaBoost Classifier

Top Three Features: 
1. total_rec_prncp
2. total_pymnt
3. total_pymnt_inv
