# Time-Series-Analysis
This is a time series project that seeks to predict sales of the Favourita company.

# Steps
Business Understanding --> Data Understandin --> Data Preprocessing --> Modelling --> Model Evaluation
                                                                                           # Business Understanding
Favorita stores hold a significant presence in the Ecuadorian grocery retail market and are renowned for providing a wide range of products to customers across the country. With a strong commitment to delivering high-quality goods and exceptional customer service, Favorita has established itself as a trusted brand within the region. The stores are strategically located in various cities and states, catering to diverse customer preferences and demands. Each Favorita store is uniquely characterized by its location, size, and product assortment, ensuring that customers have easy access to a comprehensive selection of items for their daily needs.

With a customer-centric approach and a focus on continuous improvement, Favorita stores are dedicated to delivering value to their customers and building lasting relationships. By leveraging advanced data analytics and forecasting models, Favorita aims to optimize its inventory management, ensure product availability, and enhance the overall shopping experience.

Data Understanding
For the Store Sales Time Series Forecasting project, we have several datasets available:

train.csv: This dataset contains historical sales data, including store numbers, product families, onpromotion information, and the target variable ‘sales,’ representing the total sales for each product family at a specific store on a given date.
test.csv: Similar to the train dataset, this file contains the same features as the training data but does not include the ‘sales’ column. Our goal is to predict sales for the test data based on the trained model.
transaction.csv: This dataset provides information about transactions made on specific dates at different stores.
sample_submission.csv: A sample submission file in the correct format for the competition.
stores.csv: Store metadata, including city, state, type, and cluster information.
oil.csv: Daily oil prices, which include values during both the train and test data timeframes.
holidays_events.csv: Contains information about holidays and events, including metadata about transferred and bridge holidays.

Stationarity
Stationarity is a key part of time series analysis. Simply put, stationarity means that the manner in which time series data changes is constant. A stationary time series will not have any trends or seasonal patterns. You should check for stationarity because it not only makes modeling time series easier, but it is an underlying assumption in many time series models. Specifically, stationarity is assumed for a wide variety of time series forecasting methods including autoregressive moving average (ARMA), ARIMA and Seasonal ARIMA (SARIMA).

We will use the Dickey Fuller test and Kpss test to check for stationarity in our data. This test will generate critical values and a p-value, which will allow us to accept or reject the null hypothesis that there is no stationarity. If we reject the null hypothesis, that means we accept the alternative, which states that there is stationarity.

These values allow us to test the degree to which present values change with past values. If there is no stationarity in the data set, a change in present values will not cause a significant change in past values.

# Author 
Newton Kimathi

