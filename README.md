# Time-Series-Analysis
This is a time series project that seeks to predict sales of the Favourita company.

# Steps
Business Understanding --> Data Understandin --> Data Preprocessing --> Modelling --> Model Evaluation

# Business Understanding
Favorita stores hold a significant presence in the Ecuadorian grocery retail market and are renowned for providing a wide range of products to customers across the country. With a strong commitment to delivering high-quality goods and exceptional customer service, Favorita has established itself as a trusted brand within the region. The stores are strategically located in various cities and states, catering to diverse customer preferences and demands. Each Favorita store is uniquely characterized by its location, size, and product assortment, ensuring that customers have easy access to a comprehensive selection of items for their daily needs.

With a customer-centric approach and a focus on continuous improvement, Favorita stores are dedicated to delivering value to their customers and building lasting relationships. By leveraging advanced data analytics and forecasting models, Favorita aims to optimize its inventory management, ensure product availability, and enhance the overall shopping experience.

# Data Understanding

For the Store Sales Time Series Forecasting project, we have several datasets available:

* train.csv: This dataset contains historical sales data, including store numbers, product families, onpromotion information, and the target variable ‘sales,’ representing the total sales for each product family at a specific store on a given date.
* test.csv: Similar to the train dataset, this file contains the same features as the training data but does not include the ‘sales’ column. Our goal is to predict sales for the test data based on the trained model.
* transaction.csv: This dataset provides information about transactions made on specific dates at different stores.
* stores.csv: Store metadata, including city, state, type, and cluster information.
* oil.csv: Daily oil prices, which include values during both the train and test data timeframes.
* holidays_events.csv: Contains information about holidays and events, including metadata about transferred and bridge holidays.

# Summary and Findings


In this project, we aimed to develop accurate time series forecasting models to predict store sales for a large Ecuadorian-based grocery retailer, Corporation Favorita. The dataset provided included historical sales data, store and product information, promotions, oil prices, holidays, and events. The primary goal was to optimize inventory management by forecasting product demand and improve operational efficiency.

The project followed a structured CRISP-DM framework, beginning with business understanding, data loading, and data understanding. We explored the data, identified missing values, and gained insights into sales trends, seasonality, and potential impacts of holidays and events on sales.

To prepare the data, we handled missing values, performed feature engineering, and transformed the sales data using the Box-Cox transformation to stabilize variance and achieve stationarity. We also created new features such as lagged sales, monthly sales, and sales growth rate to capture relevant patterns.

Afterwards, we trained and evaluated various regression models, including Linear Regression, Logistic Regression, Gradient Boosting Regression, Support Vector Regression, Random Forest, and Decision Tree Regression. The evaluation metrics used included RMSLE, RMSE, and MSE, focusing on RMSLE as it accounts for relative errors in forecasting.

The Random Forest and Decision Tree Regression models performed well, and we conducted hyperparameter tuning to optimize their performance. The final models were then used to make predictions on the evaluation dataset.

Key insights from the project included identifying seasonality in sales, with spikes towards the end of March and the start of October, potentially due to Easter and holiday seasons, respectively. Moreover, we observed that certain store clusters and locations exhibited higher sales activity.

In conclusion, the developed time series forecasting models provided accurate sales predictions, enabling Corporation Favorita to optimize inventory management, reduce stockouts, and enhance customer satisfaction. By leveraging machine learning techniques and analyzing historical sales data, the project contributed valuable insights to improve store sales forecasting and overall business performance.

# Stationarity 
Stationarity is a key part of time series analysis. Simply put, stationarity means that the manner in which time series data changes is constant. A stationary time series will not have any trends or seasonal patterns. You should check for stationarity because it not only makes modeling time series easier, but it is an underlying assumption in many time series models. Specifically, stationarity is assumed for a wide variety of time series forecasting methods including autoregressive moving average (ARMA), ARIMA and Seasonal ARIMA (SARIMA).
For this Project, the tests for Stationarity Used are KPSS and Dickey Fuller Test.

## To make non-stationary Series Stationary
Box-Cox transformation is a statistical technique used to stabilize the variance of a time series and make it more approximately normal. In time series analysis, stationarity is a desirable property that ensures the statistical properties of the series remain constant over time. Non-stationary time series often exhibit trends, seasonality, or changing variance, which can make it challenging to apply certain forecasting models that assume stationarity.
The Box-Cox transformation involves applying a power transformation to the data, which effectively reduces the variability and helps in making the series more stationary. The code below shows the steps of box-cox transformation

## Removing Trend Using Differencing Method
Differencing method was used to remove the trend from the data. Differencing involves subtracting the previous value from the current value to compute the difference between consecutive data points. This helps in removing the trend component, resulting in a stationary time series that is more amenable to forecasting.

The first step is to calculate the differenced data, which is obtained by subtracting each data point in the Box-Cox transformed data, data_boxcox, from its previous data point. We use the shift() function to shift the data one time step backward to perform the differencing operation.

# Model Evaluation
The final model, after Hyperparameter tuning  had a Root Mean squared Logarithmic Error of (RMSLE) of 0.045945

