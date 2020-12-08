# M5_Forecasting_Accuracy_kaggle
It contains the code and data for M5 Forecasting - Accuracy competition on Kaggle.
The details and data for this competition can be found here: https://www.kaggle.com/c/m5-forecasting-accuracy/overview

## store_and_week_wise_lgbm_v1.ipynb
* In this solution, we have built different models for different (10) stores and different (4) weeks (1-7, 8-14, 15-21, 22-28), so we are building total 40 models 
for each train_train_day_x (different validation periods for robust evaluation and hyper-parameter tuning).
* Features used are as following:
  * General base features
  * General price based features
  * General calendar and time based features
  * Lag and rolling mean/std features
  * Target encoding features for categorical variables
* Lightgbm is used for modeling.
* The more implementation details can be found here: https://www.kaggle.com/c/m5-forecasting-accuracy/discussion/163216

