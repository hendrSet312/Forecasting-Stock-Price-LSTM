# Forecasting-Stock-Price-LSTM

A case study analyzing and predicting AMD and Apple stock prices from Yahoo Finance data until April 1st 2020 with the LSTM model. 

## Used Library:
1. ETL & Data Manipulation : Numpy, pandas
2. Data Visualization : Seaborn, matplotlib
3. Machine Learning : Tensorflow, keras , optuna (for hyperparameter tuning) 

## Project Steps 
1. **Exploratory Data Analysis**
   - Exploring trends and anomalies on both AMD and Apple stock prices data
3. **Data Preprocessing**
   - Changing date columns datatype 
   - Splitting data into train (80%), validation (10%), test (10%)
   - Splitting data based on horizon (1) and windows (5)
4. **Modelling**
   - Build initial model :
      - 1 LSTM layer (50 units) with ReLu activation layer
      - 1 final layer with ADAM optimizer
   - Build hyperparameter tuned model :
     - Performed by Optuna framework
     - AMD timeseries model :
          - 4 LSTM layers (54, 74, 53 and 66 units)
          - dropout (%) : 0.003592374270444898
          - dense_layers: 1 (27 units)
     - Apple timeseries model :
         - 2 LSTM layers (44 and 11 units)
         - 3 Dense layers (94, 18, 5 units)
         - dropout (%) :  0.17625104440204847
5. **Model Evaluation**
   - Comparing model performance by MAE, RMSE and MAPE metrics
6. **Model Deployment**
   - Exporting built models into .keras format
