# M5_Forecasting_Accuracy_kaggle
It contains the code and data for M5 Forecasting - Accuracy competition on Kaggle.
The details and data for this competition can be found here: https://www.kaggle.com/c/m5-forecasting-accuracy/overview

## store_and_week_wise_lgbm_v1.ipynb
* In this solution, we have built different models for different (10) stores and different (4) weeks (1-7, 8-14, 15-21, 22-28), so we are building total __40__ models 
for each *train_train_day_x* (different validation periods for robust evaluation and hyper-parameter tuning).
* Features used are as following:
  * General base features
  * General price based features
  * General calendar and time based features
  * Lag and rolling mean/std features
  * Target encoding features for categorical variables
* __Lightgbm__ is used for modeling.
* The more implementation details can be found here: https://www.kaggle.com/c/m5-forecasting-accuracy/discussion/163216

# simple-lgbm-groupkfold-cv.ipynb

* This notebook explores how __GroupKFold__ CV strategy in __Sklearn__ can be used for hyper-parameter tuning for time-series data.
* In this notebook we haven't done any hyper-parameter tuning though, __GroupKFold__ CV has just been used for validating the model's performance but the same methodology can be used for hyper-parameter tuning.
* You can learn more about __GroupKFold__ CV and how it reduces the possibility of leakage with time-series CV from the __Markdown__ section of the notebook.
* Custom objective function and validation metric are used which works as a proxy for __WRMSSE__, competition' evaluation metric.
* The data for this notebook are available at:
   * https://www.kaggle.com/ragnar123/m5-reduce-data
   * https://www.kaggle.com/c/m5-forecasting-accuracy/data
