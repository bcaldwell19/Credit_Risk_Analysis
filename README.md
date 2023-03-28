# Credit_Risk_Analysis

> Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, you'll need to employ different techniques to train and evaluate models with unbalanced
> classes. Jill asks you to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

**Language**: Python

**Library**: Scikit-learn,imbalanced-learn

**Subject**: Supervised Learning (ML)

___________________________________________

## Analysis

It's important for the lender to understand the risk associated with accepting a request for a loan. Luickly, there is data available for lenders to understand the amount of risk they are willing to accept.  Supervised machine learning is a quick way to understand your data by various forms of analysis.  This analysis was performed to see how well different models will predict credit risk.    

## Results:

- RandomOverSampler (Figure 1)
    - Balanced accuracy score: 0.63
    - Precision (avg): 0.99
    - Recall (avg): 0.64
- SMOTE Oversampling (Figure 2)
    - Balanced accuracy score: 0.61
    - Precision (avg): 0.99
    - Recall (avg): 0.68
- Undersampling (Figure 3)
    - Balanced accuracy score: 0.51
    - Precision (avg): 0.99
    - Recall (avg): 0.46
- Combination (Over and Under) Sampling (Figure 4)
    - Balanced accuracy score: 0.64
    - Precision (avg): 0.99 
    - Recall (avg): 0.59
- BalancedRandomForestClassifier (Figure 5)
    - Balanced accuracy score: 0.91
    - Precision (avg): 0.99
    - Recall (avg): 0.91 
- EasyEnsembleClassifier (Figure 6)
    - Balanced accuracy score: 0.95
    - Precision (avg): 0.99
    - Recall (avg):  0.95

![Figure 1: Over Sample](/images/random_oversample.PNG)

Figure 1: Over Sample

![Figure 2: SMOTE](/images/smote.PNG)

Figure 2: SMOTE

![Figure 3: Clustered Centroids](/images/centroids.PNG)

Figure 3: Clustered Centroids

![Figure 4: SMOTEENN](/images/smoteenn.PNG)

Figure 4: SMOTEENN

![Figure 5: Balanced Random Forest](/images/random_trees.PNG)

Figure 5: Balanced Random Forest

![Figure 6: Easy Ensemble](/images/easy_ensemble.PNG)

Figure 6: Easy Ensemble

## Summary:

Credit risk was evaluated using multiple different machine learning models for the given dataset.  This allows us to better understand our dataset from different views.  A review of the average precision data shows that all models did a good job of reliably providing positive classification in the dataset. The models mostly varied in recall(sensitivity) and balanced accuracy score.  The Easy Ensemble Classifier scored the best of all the models for average recall.  This model was found to be the best at finding all the positive samples. 

In this study, we want to find all the positive samples to the best of our ability.  We want to flag only the accounts that will not pay back their credit.
My recommendation would be to use either the Balanced Random Forest or Easy Ensemble model to predict credit risk. I don't think it would be bad to be a little stringent on giving out credit, so Balanced Random Forest may be the better bet for a more conservative approach.  This can also depend on a lender's risk tolerance.  You want moost people to not have an issue, but the people on the bubble of good and bad credit history likely need further investigation.  
