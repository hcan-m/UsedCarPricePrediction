# usedcarpriceprediction

autos.rar contains raw data\
large_ds_ml_project.ipynb --- all codes in Jupyter Notebook\
large_ds_ml_project.html --- html print of Jupyter Notebook


Used Car Price Prediction Analysis

In this project, we aim to find the best regression model for dataset in order to be able to predict used cars prices. 

We have used public dataset from Kaggle which was scraped with Scrapy by Orges Leka from Ebay-Kleinanzeigen. It contains more than 370000 cars and 20 features of each of them like price, power, model etc... 

Original dataset had plenty missing values, outliers and mistakes, to be able to work on it we had to clean, impute and change their format.

We select the features carefully and extract new features from  raw data.

In order to achieve this goal we used Linear Model, K Nearest Neighbor and Random Forest.

Summary

In this project we aimed to find the best regression model for used cars dataset to be able to predict used cars price.

Dataset was scraped with Scrapy from German eBay and there were some mistakes, duplications and outliers. As first step we removed them from the dataset and stayed with 79.9% of the original data.

There were 20 variables in the original dataset and we had to remove "dateCrawled", "postalCode", "abtest", "offerType", "nrOfPictures", and "seller" because they were not usefull for our purpose.
We created new features:

"daysBeforeSold" by using "dateCreated" and "lastSeen"
"namelen" by using "name"
"age" by using "yearOfRegistration"
After that we worked on missing values columnwise and impute what we could impute meaningfully and drop the rest. At the end we had 75.8% of the original data ready to use for price prediction.

We used log-transformation in price and powerPs and one hot encoding for categorical variables to be able to perform machine learning algorithms.

We used Linear Model, K Nearest Neighbor and Random Forest. The most successul one was Random Forest with 88.01% r2_score. Followed by KNN with 83.70% and the worst one was as expected Linear Regression with 78.67%.
