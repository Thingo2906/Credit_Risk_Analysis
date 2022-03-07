# Credit_Risk_Analysis
## Overview of the analysis: 
- In this project, we'll look at how all of the variables in our loan stats csv may be used to forecast if someone is at low or high risk. Creating a model, then evaluating and training it is one way that data scientists employ to solve this sort of problem. We are utilizing the imbalanced-learn and scikit-learn libraries to create models and evaluate them using a resampling strategy in this project. In the first several models, I used the randomoversampler and smite algorithms to oversample the data and the clustercentroid method to undersample it. In the remaining models, I utilized smoteenn to over and undersample the data using a mixture technique. Finally, I compared balancedrandomforestclassifier and easyensembleclassifier, two machine learning models that reduce bias.
## Results: 
- Naive Random Oversampling results: Our balanced accuracy test it 66%, the precision for the high_risk has a very low positivity at 1% and the recall is 71%
<img width="785" alt="12" src="https://user-images.githubusercontent.com/93515126/156951543-d66f9c22-8635-4e2e-b009-1ce3813d39af.png">
- SMOTE oversampling results: the accuracy score is 66.2%, the precision for the high_risk loans has a low positvity again at 1% and recall is 69% overall.
<img width="1286" alt="13" src="https://user-images.githubusercontent.com/93515126/156951725-6ce1c35b-30d9-44f7-a2ae-ca5aa3cd9edf.png">
- Undersampling results: balanced accuracy score is 66.2% overall, the precision is at 99% and the recall is 40%
<img width="715" alt="14" src="https://user-images.githubusercontent.com/93515126/156951846-6755014a-d477-4f6f-855d-32a82c77274e.png">
- Combination(over and undersampling) results: balanced accuracy score is 54.7% the precision is 99% and the recall is 57% overall.
<img width="696" alt="15" src="https://user-images.githubusercontent.com/93515126/156951977-5647d8c3-6479-4a73-aa0a-9fd25f632958.png">
- Balanced Random Forest Classifier results: the accuracy score is 77.2% the precision is 99% and the recall is 89%.
<img width="805" alt="16" src="https://user-images.githubusercontent.com/93515126/156952444-f7fceeb0-cbed-4e27-a8ab-9a0d0a652f7c.png">
- Easy Ensemble AdaBoost Classifier results: the accuracy score is 91.7% the precision is 99% and the recall is 94%
<img width="776" alt="17" src="https://user-images.githubusercontent.com/93515126/156952534-a8a5aa96-355a-48c4-aa24-0436acb50677.png">

## Summary: 

- To evaluate which model is best at forecasting which loans are the most risky, we undersampled, oversampled, and combined both in the first four models. In the next two models, we used ensemble classifiers to resample the data and try to forecast whether loans are high or low risk. Our accuracy score in the first four models is lower than the ensemble classifiers, and the recall in the oversampling/undersampling/mixed models is also poor. Typically, you want a fair mix of recall and precision in your models, which is why I prefer ensemble classifiers over the first four models. Because of its high accuracy score and strong mix of precision and recall scores, the Easy Ensemble looks to have the finest balance of all the models.
