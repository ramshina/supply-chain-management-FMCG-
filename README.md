# supply-chain-management-FMCG-
# FMCG Instant Noodles Supply Optimization Model

## Introduction

A Fast Moving Consumer Goods (FMCG) company entered into the instant noodles business two years back.
Their higher management has noticed that there is a mismatch in the demand and supply.
Where the demand is high, supply is pretty low and vice-versa which results in a loss in inventory cost and ultimately loss to the company.
Hence, the higher management wants to optimize the supply quantity in each and every warehouse in the entire country.

The objective of this exercise is to build a model, using historical data that will determine an optimum weight of the product to be shipped each time from the respective warehouse.

## Dataset

The dataset for this problem consists of various features such as warehouse ID, manager ID, zone, regional zone,
number of refill requests received by the warehouse in the last 3 months, 
number of transport issues for the warehouse in the last 1 year, number of competitors in the market,
number of retail shops who sell noodles produced by the warehouse, whether the warehouse is owned by the company or it is on rent,
number of distributors who work between warehouse and retail shops,whether the warehouse is in a flood impacted area or not,
whether the warehouse has proper electric supply along with some power backup, distance from the warehouse to production hub,
number of workers in the warehouse, warehouse establishment year, storage issues reported by the warehouse in the last 3 months, 
whether the warehouse has temperature regulating machine indicator or not,type of approval warehouse having been issued by government,
number of times the warehouse faces the breakdown in the last 3 months, product weight, etc.

## Data Science Process

The following data science process was employed to build the model:

1. Exploratory Data Analysis (EDA)
2. Data Processing
3. Model Building and Evaluation
4. Charts
5. Insights and Improvements

   ## Exploratory Data Analysis (EDA)

The EDA process was conducted to get a better understanding of the dataset and the relationships between the different variables. The following steps were performed:

- Importing the required libraries and loading the dataset into a Pandas DataFrame
- Viewing the top 5 rows of the dataset
- Determining the number of rows and columns in the dataset
- Obtaining a statistical summary of the dataset
- Getting information about the dataset such as the column data types and number of non-null values
- Creating a correlation matrix and heatmap to visualize the correlation between the different features

  From the heatmap, it was observed that the number of refill requests received by the warehouse in the last 3 months is strongly positively correlated with the product weight.

## Data Processing

The data processing step involved handling categorical variables using one-hot encoding, 
splitting the data into training and testing sets in an 80:20 ratio and scaling the data using StandardScaler.

## Model Building and Evaluation

Four models were built using the following machine learning algorithms:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor

The models were fitted to the training data and evaluated using the testing data.
The Gradient Boosting Regressor gave the highest R-squared value of 0.8084,
indicating that the model explains 80.84% of the variance in the target variable.

## Charts

To visualize the performance of the models, a scatter plot of the predicted values vs. true values was created for the Gradient Boosting Regressor. 
From the scatter plot, it was observed that the predicted values are close to the true values, indicating that our model is performing well.

## Insights and Improvements

The correlation heatmap showed that the number of refill requests received by the warehouse in the last 3 months is strongly positively correlated with the product weight.
This means that if a warehouse receives more refill requests, it is likely to ship more product weight.

One improvement that can be made to the model is to include more features that might affect the product weight such as the type of noodle being shipped,
the price of noodles, the seasonality of demand, etc.

Another improvement could be to use more advanced machine learning techniques such as neural networks or ensemble models to further improve the model’s performance.
