# Yes-Bank-Stock-Closing-Price-Prediction

## Problem Statement
Yes Bank is a well-known bank in the Indian financial domain. Since 2018, it has been in the news because of the fraud case involving Rana Kapoor. Owing to this fact, it was interesting to see how that impacted the stock prices of the company and whether Time series models or any other predictive models can do justice to such situations. This dataset has monthly stock prices of the bank since its inception and includes closing, starting, highest, and lowest stock prices of every month. The main objective is to predict the stock’s closing price of the month.
![image](https://user-images.githubusercontent.com/85817763/179193664-22721f34-db21-4647-a323-46be7acc561e.png)


## Project Approach
A stock (also known as equity) is a security that represents the ownership of a fraction of a corporation. This entitles the owner of the stock to a proportion of the corporation's assets and profits equal to how much stock they own. Units of stock are called "shares." The value of shares depends on the investors, whether more people are buying the stock or selling it, follows the simple supply – demand rule.

So, my aim was to apply different regression models on the given data to predict the closing price of the stock and then compare all the models to figure out the best one for this job. Following is the pathway followed during the whole process:
* Started off with data overview, just to understand what’s in the dataset and in order to inspect how clean the dataset is for working.
* Visualizations makes things easier so, performed exploratory data analysis and checked for data distribution.
* Used log transformation to make them normally distributed features as the features were a bit skewed.
* Checked for multicollinearity to check if the features are depedent or independent of each other.
* Splitted the dataset into training and testing data (70% of the data is used for training & 30% of the data is being used for testing).
* Created machine learning models using the following algorithms:
  1. Linear Regression
  2. Ridge Regession
  3. Lasso Regression
* Compared model performance using different evaluation metrics in order to get the best performing model.


## Variables Description
Date:- It contains 1st day of every month from year 2005

Open:- The open prices of yes bank Stock on that particular date

High:- The Highest price it reached on that day

Low:- The lowest price it reached on that day

close:- The Closing price of Yes bank stock on that particular date (Target Variable)

We can clearly see that our mean and much higher than our median in every feature so this distribution must be right skewed.

## Machine Learning Models

➡️ *Linear Regression*

Below is the perfomance graph of linear regression model based on predicted and actual output.

![image](https://user-images.githubusercontent.com/85817763/179197341-fd2ca425-0c99-4785-9573-77602e0affa3.png)


➡️ *Ridge Regression*

Below is the perfomance graph of ridge regression model based on predicted and actual output.

![image](https://user-images.githubusercontent.com/85817763/179198859-cc7983f1-e43d-4c1e-a981-80ab08a025b9.png)


➡️ *Lasso Regression*

Below is the perfomance graph of lasso regression model based on predicted and actual output.

![image](https://user-images.githubusercontent.com/85817763/179199192-3d1d0c27-b7ce-4b7e-b2e7-a9fe7770282a.png)



## Conclusions

* We load our data using Pandas

* we saw that our data in right skewed with the help of distplot

* then we saw the trends of our each features

* after that we have created a new feature that tells us about the monthly change

* percentage on the basis of our close price

* then we visualized average closing price of each year

* and we saw the histogram and trend of the new column

* and visualized our outliers using box plot

* then we got that our data need to be in uniform distribution so we applied log10 transformation on our data and set date column as index

* we have only one missing value in new created column which was filled by 0.03 value

* we split or data into 70-30 ratio of train and test

* now using Min Max Scaler we scaled our data

* and now we started our ML modelling

* we used Linear regression and evaluated its MSE RMSE MAE and R2 values and got best results

* then we used Lasso model and did Lasso Cross Validation with best alpha hyperparameter as 0.0001 and again we got almost same matrices

* and finally we used Ridge regression model and Ridge Cross Validation with best alpha hyperparameter as 0.0001 and got the same results

as our data is so limited and we dont have prices on per day basis so we can not perform time series analysis on the model so we will go with simple linear regression model as our best model for this regression prediction model.
