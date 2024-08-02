# Time Series Forecasting Project



## Introduction



In this project, I am tasked with building a time series forecasting model to predict the number of units sold for each item ID using dummy sales data from Amazon. The data includes various attributes such as date, Item ID, Item Name, anarix_id, ad_spend, units (target), orderedrevenueamount, and unit_price. My objective is to leverage this data to accurately forecast sales and to provide insights into the factors influencing these sales.



## Objectives



**Primary Task:** The primary goal is to develop a time series forecasting model that predicts the number of units sold for each item ID. I will use the Mean Squared Error (MSE) as the evaluation metric to assess the accuracy of the model. The dataset contains various features, and I aim to utilize these effectively to enhance the predictive performance.



**Bonus Task:** In the second task, I am required to predict unit sales without utilizing the ad_spend feature. This will help to understand the model's performance when deprived of advertising spend data, which could be crucial for decision-making in scenarios where ad spend information is unavailable or unreliable.



## Approach



My approach to this project involves the following key steps:



1. **Data Loading and Exploration**
   
   

   I start by loading the training and test datasets, ensuring that the date column is parsed correctly as a datetime object. This step is crucial because time series forecasting inherently depends on the chronological order of data.



   I then perform an initial inspection of the data to understand its structure, identify any missing values, and get an overview of the distribution of the features. This exploratory data analysis (EDA) helps me to identify patterns, outliers, and relationships between the features, which are essential for feature engineering and model building.



2. **Feature Engineering**
   
   

   Feature engineering is a critical step where I transform raw data into meaningful features that improve the model's performance. Here, I extract additional date-related features such as the year, month, day, and day of the week. These features help capture seasonality, trends, and other time-dependent patterns in the sales data.



   Additionally, I aggregate the data by Item ID and the newly created date features. This aggregation ensures that the data is appropriately structured for time series analysis and forecasting.



3. **Model Selection and Training**
   
   

   For model selection, I use XGBoost, a powerful gradient boosting algorithm that is well-suited for regression tasks. I split the data into training and validation sets to evaluate the model's performance and avoid overfitting. Feature scaling is also applied to ensure that the model can handle features with different scales effectively.



   After an initial round of training, I perform hyperparameter tuning using GridSearchCV to identify the best set of parameters for the model. This tuning helps in optimizing the model's performance by exploring various combinations of hyperparameters.



4. **Evaluation and Visualization**
   
   

   The model's performance is evaluated using the Mean Squared Error (MSE) on the validation set. Lower MSE values indicate better predictive accuracy. I also visualize the actual versus predicted units sold to gain insights into the model's effectiveness.



   For both the primary and bonus tasks, I create visualizations that compare the actual and predicted sales values. These plots help in understanding how well the model captures the underlying patterns in the data. I make sure to include my registration number "20MIC0057" in all the visualizations for identification purposes.



5. **Bonus Task: Predicting Without Ad Spend**
   
   

   In the bonus task, I drop the ad_spend feature and retrain the model. This step is essential for understanding how much the model relies on advertising spend to make accurate predictions. By comparing the MSE and visualizing the results, I can assess the model's robustness when deprived of this critical feature.



   Finally, I display the predictions directly in the notebook to ensure that they are correctly generated and ready for submission.



## Conclusion



Through this project, I aim to demonstrate my ability to handle time series data, perform feature engineering, and build robust forecasting models. The detailed exploration and visualization of results, coupled with model tuning, are expected to yield insights that could be valuable for decision-making in a real-world scenario.


