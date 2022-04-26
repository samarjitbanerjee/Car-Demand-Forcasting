**Car Demand Forecasting Challenge**

Problem Statement
-	ABC is a car rental company based out of Bangalore. It rents cars for both in and out stations at affordable prices. The users can rent different types of cars like Sedans, Hatchbacks, SUVs and MUVs, Minivans and so on.
-	In recent times, the demand for cars is on the rise. As a result, the company would like to tackle the problem of supply and demand. The ultimate goal of the company is to strike the balance between the supply and demand in order to meet the user expectations. 
-	The company has collected the details of each rental. Based on the past data, the company would like to forecast the demand of car rentals on an hourly basis. 
Objective
-	The main objective of the problem is to develop the machine learning approach to forecast the demand of car rentals on an hourly basis.

Solution-
Approach 1: (Posing it as Time Series Forecasting): 
•	Data Preparation is based on taking lags of past 24 hours and prepare the data to fit in Stacked LSTM Model
•	During Forecasting on Test Data, we need to take past 24 hours data from Validation set and need to forecast the car demand for first record Test Data and once we forecast for second record, past 24 hours records include the first data from Test Record. This process continues until last record reached.
    
Approach 2: (Posing it as Regression Problem):
•	Data Preparation based on different features like, day of week, is weekend, month, year. One-Hot-Encoding on Month, year and hour.
o	During Model Training without providing these derived feature’s performance was degrading which boosted after adding to the data.
•	DNN Model with Drop-out layer used to train the model
•	Forecasted the car demand data based on model trained.

Final Model – DNN Model (Deep Neural Network with 16-8-1 layers). Relu activation function is used in the hidden layers. Linear Activation function is used in Last layer.
