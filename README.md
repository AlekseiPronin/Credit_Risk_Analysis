# Credit_Risk_Analysis

## Purpose

The purpose of this analysis was to use Python and Scikit-learn to build and evaluate several machine learning models to predict credit risk.

* The data set for the analysis was provided
* Training and test groups from a given data set were created
* Random Oversampling, SMOTE Oversampling, Cluster Centroid Undersamling, SMOTEENN and Ensemble Learners (Random Forest and Easy Ensemble AdaBoost) were used to create ML models
* Models were evaluated based on balanced accuracy score, precision and sensitivity (recall)


## Results

#### Random Oversampling

![randomOversampling](https://github.com/AlekseiPronin/Credit_Risk_Analysis/blob/main/Resources/RandomOversampling.png)

* the Balanced accuracy score for this model is 0.6601016876770167
* Precision for high risk credits is very low due to a large number of false positive results. For low risk credits precision is 1 which means the model can find all credits with low risk
* Recall for both types is around 0.66 and it means that the ammount of false negative credits is pretty big.


#### SMOTE Oversampling

![SMOTE_over](https://github.com/AlekseiPronin/Credit_Risk_Analysis/blob/main/Resources/SMOTE_over.png)

* The Balanced accuracy score for this model is 0.6463291312633204
* The overall results of this model are simmilar to Random Oversampling model above. Precision is low for high risk credits and high for low risk credits.
* Recall follows the same trend with Random Oversampling and makes 0.63 and 0.66 for high and low risk credits respectively


#### Cluster Centroid Oversampling

![oversampling](https://github.com/AlekseiPronin/Credit_Risk_Analysis/blob/main/Resources/undersampling.png)

* The Balanced accuracy score for this model is 0.6463291312633204
* Precision is unballanced, which is simillar to previous models. For high risk credits is very low due to a large number of false positive results. For low risk credits precision is 1 which means the model can identify all credits with low risk
* Recall for low risk credits is 0.45 which means that the number of false negative credits is bigger than in previous models.


#### SMOTEENN

![SMOTEENN](https://github.com/AlekseiPronin/Credit_Risk_Analysis/blob/main/Resources/SMOTEENN.png)

* The Balanced accuracy score for this model is 0.5293318990697431 which is the lowest result across all tested models
* Precision remained the same to previous models
* Recall for high risk credits is 0.70 which means that the number of false negatives decreased. For low risk recall is 0.59, which means there is still great number of false negatives.


#### Ballanced Random Forest Classifier

![brf](https://github.com/AlekseiPronin/Credit_Risk_Analysis/blob/main/Resources/brf.png)

* The Balanced accuracy score for this model is 0.7877672625306695
* Precision for high risk credits increased which tells us that the number of false positives slightly decreased. Precision for low risk is 1.
* Recall for low risk credits is 0.91 which is rather high and it means that the number of false negative results is rather low.


#### Easy Ensemble AdaBoost Classifier

![eec](https://github.com/AlekseiPronin/Credit_Risk_Analysis/blob/main/Resources/eec.png)

* The Balanced accuracy score for this model is 0.925427358175101. This is the best result across all tested models.
* Precision 0.07 for high risk credits is the biggest across all tested models. For low risk remained the simmilar to other models.
* Recall is ballanced for both high and low risk credits and makes 0.91 and 0.94 respectively, which means that the ammount of false negative results is rather low.



## Summary

All models show simmilar results for Precision for both types of credits across all models. Recall showed different results from one model to another.

The worst performing model based on Ballanced Accuracy Score is SMOTEENN model with only 52% of accuracy.

The best performing model is Easy Ensemble model with the resulf of 92% accuracy.

Based on this analysis I would recommend to use the last model, Easy Ensemble, because it showed best accuracy score, best precision and recall for both credit types. 
In this context, false positives are preferable to false negatives. It is better to rule out false positive credits than to miss clients who actually take risky credits.
