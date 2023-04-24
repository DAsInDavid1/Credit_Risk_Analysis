# Credit_Risk_Analysis
Using Machine Learning, imbalanced -learn and scikit-learn libraries to build and evaluate models using resampling. Will be using RandomOverSampler and SMOTE algorithms to oversample our data and evaluate the performace of these models to make a written recommendation on whether they should be used to predict credit risk.


## Overview
The purpose of this analysis was to use machine learning to solve the challenge of credit card risk. Using different unbalanced classification methods we tryto preditc credit risk and to evaluate the performance of 6 models to recomend wheather they should be used to predict credit risk.

## Results

### RandomOverSampler
<img src= "https://github.com/DAsInDavid1/Credit_Risk_Analysis/blob/main/Photos/RandomOverSampler.png" width=50% height=50%> 

<ins>Balanced score</ins> = 64% - Our accuracy shows that we are not very accurate at prediticting if the customer is a high risk or a low risk. It is only 14% better then the expected 50% chance you may have at guessing if a customer is high risk or low risk (assuming they are a balanced class)


<ins>precision</ins> = 99% - the precision score shows that we are incredibly accurate at predicting positive cases.

<ins>recall</ins> = 59% - our recall score shows that we are only about 1/2 right in predicting if the true positive actually is a true positive instead of a false negative.

### SMOTE
<img src= "https://github.com/DAsInDavid1/Credit_Risk_Analysis/blob/main/Photos/SMOTE.png" width=50% height=50%> 

<ins>Balanced score</ins> = 66% -  Our accuracy shows that we are not very accurate at prediticting if the customer is a high risk or a low risk. However it is better then the previous random over sampling.


<ins>precision</ins> = 99% - the precision score shows that we are incredibly accurate at predicting positive cases.

<ins>recall</ins> = 69% - Our recall rate is much better at around 70% and seems to be a major difference then random over sampling

### ClusterCentroids
<img src= "https://github.com/DAsInDavid1/Credit_Risk_Analysis/blob/main/Photos/ClusterCentroids.png" width=50% height=50%> 

<ins>Balanced score</ins> = 52% -  Our accuracy shows that we are not very accurate at prediticting if the customer is a high risk or a low risk. It is the worst method seen to predict credit score


<ins>precision</ins> = 99% - the precision score shows that we are incredibly accurate at predicting positive cases.

<ins>recall</ins> = 40% - Our recall rate is terrible at prediticing id the true positive actually is a true positive.

### SMOTEENN
<img src= "https://github.com/DAsInDavid1/Credit_Risk_Analysis/blob/main/Photos/SMOTEENN.png" width=50% height=50%> 

<ins>Balanced score</ins> = 64% -  Our accuracy shows that we are not very accurate at prediticting if the customer is a high risk or a low risk. It is higher then some. However, out of all the resampling methods it still is not the most accurate


<ins>precision</ins> = 99% - the precision score shows that we are incredibly accurate at predicting positive cases.

<ins>recall</ins> = 58% - Our recall rate is not up to par with what we would like, with only being accurate alittle bit more then 1/2 the time is not acceptable.

### BalancedRandomForestClassifier
<img src= "https://github.com/DAsInDavid1/Credit_Risk_Analysis/blob/main/Photos/BalancedRandomForestClassifier.png" width=50% height=50%> 

<ins>Balanced score</ins> = 78% - Our accuracy shows that we are getting more accurate at prediticting if the customer is a high risk or a low risk. This method 


<ins>precision</ins> = 99% - the precision score shows that we are incredibly accurate at predicting positive cases.

<ins>recall</ins> = 87% - our recall rate is much better at predicting if the true positive actually is a true positive instead of a false negative. With a 87% recall your credit risk will be much lower then the resampling methods

### EasyEnsembleClassifier
<img src= "https://github.com/DAsInDavid1/Credit_Risk_Analysis/blob/main/Photos/EasyEnsembleClassifier.png" width=50% height=50%> 

<ins>Balanced score</ins> = 93% - This accuracy has been the best by far, and if any method is to be used this should be the method.


<ins>precision</ins> = 99% - the precision score shows that we are incredibly accurate at predicting positive cases.

<ins>recall</ins> = 94% - our recall rate is much better at predicting if the true positive actually is a true positive instead of a false negative.

## Summary
Out of all the machine learning methods the EasyEnsembleClassifier method is by far the best. However, it is not good enough for a large firm. If you are having over 10,000 people apply for credit daily, and the model not getting the correct result 6% of the time (600 peopl) it would cause alot of work to fix that. for the ones deemded high risk but are actually not, you would need a help line to dispute their rejected credit. For the those deemed low risk, but actually high risk you would need a payables department with enough man power to try and recoup those funds from the high risk people.

If you are a smaller company only seeing 100 people apply for credit a day this model would work for you. Most firms would easily have enough man power to deal with the 6-7% of incorrect assesments of the machine learning model. 

# Resources
https://stackoverflow.com/questions/40565444/balanced-random-forest-in-scikit-learn-python - Used for learning syntax and implementation of Balanced Random Forest Classifer

https://stackoverflow.com/questions/66709985/high-recall-low-precision-with-easyensembleclassifier - Used for learning syntax and implementation of Easy Ensemble Classifier
