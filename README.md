# Yes-Bank-Stock-Closing-Price-Prediction

## Problem Statement
Yes Bank is a well-known bank in the Indian financial domain. Since 2018, it has been in the news because of the fraud case involving Rana Kapoor. Owing to this fact, it was interesting to see how that impacted the stock prices of the company and whether time series models or any other predictive models can do justice to such situations. This dataset has monthly stock prices of the bank since its inception and includes closing, starting, highest, and lowest stock prices of every month. The main objective is to predict the stock’s closing price of the month.

![image](https://user-images.githubusercontent.com/85817763/179193664-22721f34-db21-4647-a323-46be7acc561e.png)

## Project Approach
A stock (also known as equity) is a security that represents the ownership of a fraction of a corporation. This entitles the owner of the stock to a proportion of the corporation's assets and profits equal to how much stock they own. Units of stock are called "shares." The value of shares depends on the investors, whether more people are buying the stock or selling it, follows the simple supply – demand rule.

So, my aim was to apply different regression models on the given data to predict the closing price of the stock and then compare all the models to figure out the best one for this job. Following is the pathway followed during the whole process:
* Started off with data overview, just to understand what’s in the dataset and in order to inspect how clean the dataset is for working.
* Visualizations makes things easier so, performed exploratory data analysis and checked for data distribution.
* Used log transformation to make them normally distributed features as the features were a bit skewed.
* Checked for multicollinearity to check if the features are depedent or independent of each other.
* Splitted the dataset into training and testing data (80% of the data is used for training & 20% of the data is being used for testing).
* Created machine learning models using the following algorithms:
  1. Linear Regression
  2. Ridge Regession
  3. Lasso Regression
  4. K Nearest Neighbours (KNN)
* Compared model performance using different evaluation metrics in order to get the best performing model.

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


➡️ *KNN*

Below is the perfomance graph of KNN model based on predicted and actual output.

![image](https://user-images.githubusercontent.com/85817763/179199446-15012cae-12fb-4185-a938-3d63dfd5843d.png)


## Metrics Comparison

All the models are evaluated on the basis of following evaluation metrics.

![image](https://user-images.githubusercontent.com/85817763/183074627-4bd7e7c8-c6a5-4d17-9f57-c23c8aa11666.png)

## Conclusions

*  Independent variables(input variable) have a very high influence on dependent variable(target variable).
*   The accuracy for each model is more than 95%.
*  In this case, Linear Regression has given the best results with lowest MSE and RMSE and highest R square value scores out of all.
*  KNN performed the worst out of all.
*  As we know that, lasso regression automatically selects only those features that are useful and hence discarded some features when applied in this case, whereas in this case all the features were important for prediction purpose so it ended up giving poor results.
