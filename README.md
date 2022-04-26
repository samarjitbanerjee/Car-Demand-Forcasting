**Car Demand Forecasting Challenge**

Approach 1: (Posing it as Time Series Forecasting): 
•	Data Preparation is based on taking lags of past 24 hours and prepare the data to fit in Stacked LSTM Model
•	During Forecasting on Test Data, we need to take past 24 hours data from Validation set and need to forecast the car demand for first record Test Data and once we forecast for second record, past 24 hours records include the first data from Test Record. This process continues until last record reached.
    
Approach 2: (Posing it as Regression Problem):
•	Data Preparation based on different features like, day of week, is weekend, month, year. One-Hot-Encoding on Month, year and hour.
o	During Model Training without providing these derived feature’s performance was degrading which boosted after adding to the data.
•	DNN Model with Drop-out layer used to train the model
•	Forecasted the car demand data based on model trained.

Final Model – DNN Model (Deep Neural Network with 16-8-1 layers). Relu activation function is used in the hidden layers. Linear Activation function is used in Last layer.
