# Credit_Risk_Analysis

## Analysis Overview 

The goal of this credit card dataset analysis from LendingClub was to to apply machine learning to determine credit card risk. We oversampled the data provided using RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then, we used a combinational approach of over- and undersampling using the SMOTEEN algorithm. We then compared two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier to attempt to predict credit risk. We will now evaluate the performance of these models and make recommendations for which, if any, should be used to predict credit risk. 

## Results

**Oversampling algorithms:** 

**RandomOverSampler (Naïve Random Oversampling):** 
-	Balanced Accuracy score: 66.2%
-	Precision: 99%
-	Recall: 69%

**SMOTE:** 
-	Balanced Accuracy score: 66.2%
-	Precision: 99%
-	Recall: 69%

The oversampling algorithms balanced accuracy, precision, and recall scores are identical to each other. 

**Undersampling algorithms:** 

**ClusterCentroids Resampler:** 
-	Balanced Accuracy score: 54.4%
-	Precision: 99%
-	Recall: 42%

The undersampling algorithms are also very comparable to one another. 

**Combination (Over and Under) Sampling:** 

**SMOTEEN**
-	Balanced Accuracy score: 54.4%
-	Precision: 99%
-	Recall: 57%

**Ensemble Learning Algorithms:** 

**BalancedRandomForestClassifier:** 
-	Balanced Accuracy score: 82.1%
-	Precision: 99%
-	Recall: 89%

**EasyEnsembleClassifier:** 
-	Balanced Accuracy score: 92.5%
-	Precision: 99%
-	Recall: 89%

## Summary

The precision scores are the percentage of positive predictions that are correct, a measure of how reliable a positive classification is. Recall, also called sensitivity, is the percentage of actual positive results that are predicted correctly, or the “true positive rate.” While precision for each model was consistently found to be 99%, the recall percentage varied considerably. The oversampling algorithms were moderately successful with balanced accuracy and recall percentages. The undersampling algorithm had the lowest percentages or success at identifying the low-risk loans, with the combination (over and under) sampling model only proving to be moderately better. The ensemble learning algorithms had the highest balanced accuracy scores and recall scores. If a choice had to be made from these specific algorithms, the EasyEnsembleClassifier model might provide what the bank is looking for. However, I would be curious if there are other models available to use that provide a higher ability to identify high risk loans; the EasyEnsembleClassifier had a high risk recall of 75%, which seems low and might put the bank itself at risk for issuing loans to customers who may not ordinarily prove to be reliable loanees. 
