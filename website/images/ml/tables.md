# AITA

```raw
Random Forest Classification Report:
              precision    recall  f1-score   support

         YTA       0.72      0.52      0.60      7387
         NTA       0.59      0.84      0.69      7012
         ESH       0.00      0.00      0.00       383
         NAH       0.00      0.00      0.00       317
        INFO       0.00      0.00      0.00       253

    accuracy                           0.63     15352
   macro avg       0.26      0.27      0.26     15352
weighted avg       0.61      0.63      0.60     15352

XGBoost Classification Report:
              precision    recall  f1-score   support

         YTA       0.71      0.62      0.66      7387
         NTA       0.64      0.81      0.71      7012
         ESH       0.00      0.00      0.00       383
         NAH       0.00      0.00      0.00       317
        INFO       0.00      0.00      0.00       253

    accuracy                           0.67     15352
   macro avg       0.27      0.29      0.27     15352
weighted avg       0.63      0.67      0.64     15352


Random Forest Kappa Score: 0.3125477758880384
XGBoost Kappa Score: 0.37599140374591733
```

# AIO

```raw
Random Forest Classification Report:
                  precision    recall  f1-score   support

Not Overreacting       0.67      0.91      0.77       172
    Overreacting       0.78      0.43      0.55       134

        accuracy                           0.70       306
       macro avg       0.73      0.67      0.66       306
    weighted avg       0.72      0.70      0.67       306

XGBoost Classification Report:
                  precision    recall  f1-score   support

Not Overreacting       0.69      0.80      0.74       172
    Overreacting       0.68      0.54      0.60       134

        accuracy                           0.69       306
       macro avg       0.68      0.67      0.67       306
    weighted avg       0.69      0.69      0.68       306


Random Forest Kappa Score: 0.34994746219562345
XGBoost Kappa Score: 0.34766388346065025
```
