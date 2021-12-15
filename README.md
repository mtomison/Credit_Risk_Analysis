
# Credit Risk Analysis
## Overview
Credit risk is inherently unbalanced.  So, how can we use machine learning to evaluate that risk?  This analysis is applying several machine learning models to train and then predict risk. 
## Results
### Balanced Accuracy Scores
> Naive Random Oversampling: 0.62499
> SMOTE Oversampling: 0.65126
> ClusterCentroids: 0.65126
> SMOTEEN: 0.51030
> BalancedRandomForestClassifier: 0.56323
> AtaBoostClassifier: 0.99640

### Precision & Recall Scores

**Naive Random Oversampling:**
| Risk |Prec  | Recall | f1|
|--|--|--|--|
|High  | 0.01 | 0.60| 0.02|
|Low|1.00|0.65|0.79|

**SMOTE Oversampling:**
| Risk |Prec  | Recall | f1|
|--|--|--|--|
|High  | 0.01 | 0.64| 0.02|
|Low|1.00|0.66|0.79|

**ClusterCentroids:**
| Risk |Prec  | Recall | f1|
|--|--|--|--|
|High  | 0.01 | 0.59| 0.01|
|Low|1.00|0.43|0.60|

**SMOTEEN:**
| Risk |Prec  | Recall | f1|
|--|--|--|--|
|High  | 0.01 | 0.70| 0.02|
|Low|1.00|0.57|0.73|

**BalancedRandomForestClassifier:**
| Risk |Prec  | Recall | f1|
|--|--|--|--|
|High  | 0.04 | 0.67| 0.07|
|Low|1.00|0.91|0.95|

**AtaBoostClassifier:**
| Risk |Prec  | Recall | f1|
|--|--|--|--|
|High  | 0.77 | 0.41| 0.54|
|Low|1.00|1.00|1.00|

## Summary
### Machine Learning Models
Most of these Machine Learning Models had a poor precision value for the high risk borrowers with one exception; *AtaBoostClassifier* had a .77 value. All of the models had a 1.0 precision value for the low risk borrowers, which is perfect.  

When looking at the recall or sensitivity values for the high risk borrowers, the best Machine Learning Models were *SMOTEEN* and *BalancedRandomForestClassifier* which had values of 0.70 and 0.67, respectively.

Taking the f1 values for the high risk borrowers, they all ranked poorly with none of them exceeding 0.07 except for *AtaBoostClassifier*.  This model had an f1 value of 0.54.  On the other hand, they all had acceptable f1 values for the low risk borrowers at 0.60 or above. 
### Recommendation
I would recommend ***AtaBoostClassifier*** machine learning model based on the fact that the precision and f1 numbers were both above 50% and the recall/sensitivity was not far behind that at only 41%.  This model exhibited an all around more balanced outcome.
