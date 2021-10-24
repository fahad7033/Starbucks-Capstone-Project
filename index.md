# Starbucks-Capstone-Project
<p align="center">
  <img  src="images/header.png">
</p>
## Project Overview

This is the capstone project of udacity data scientist nanodegree. In this project, the dataset of Starbucks customer behavior is investigated and analysed. Starbucks collects data about customers and how they react with the offers sent via mobile app. The offers might be a discount or buy one get one free (BOGO).

## Problem Statement
This project is about investigating the data of Starbucks customers and offers. Data is used for the following tasks:

1- Investigating some information about customers such as age, income, and joining.  <br>
2- Building a model to idenify customers who potentially will take an offer

## Data Exploration
The data is contained in three files: <br>
profile.json - demographic data for each customer <br>
portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.) <br>
transcript.json - records for transactions, offers received, offers viewed, and offers completed <br>


1- profile dataset
<p align="center">
  <img  src="images/profile.png">
</p>
<br>
2-portfolio dataset
<p align="center">
  <img  src="images/portfolio_dataset.png"> 
</p>

<br>
3-transcript dataset
<p align="center">
  <img  src="images/transcript.png"> 
</p>

## Data Preprocessing
It is clear from the data exploration that the data have some issues. In order to improve the qualit of the data, we implemented the following procedures:
<br>
For portfolio dataset:
1.Rename the column of id to be offer_id instead.
2.Encoding the column of channels
3.Create dummy variables for the column offer_type

<br>
For profile dataset:
1-Renaming the column of id to be customer_id.
2-The column became_member_on should be changed to be a readable date by separating years and months in separated columns
3-The culomn age contains the value 118 which refers to nan, so it should be changed to nan
4-Rows with nan values in the fields gender, income, or age are droped
5-Converting gender values to 0s for females and 1s for males

<br>
For transcript dataset:
1-Renaming the column of person to be customer_id.
2-Creating separated columns for amount, reward and offer_id from the column value
3-Dropping transaction rows whose customer_id is not in customer_id of proflie dataset
4-Converting time from hours to be in days
5-Create dummy variables for the column event

<br>


## Data Analysis
After analysing the data of registered customers, we found that most of customers have income in the range (60,000 and 80,000) and in the age of 50s. In addition, the majority of customers joined to app in 2017 and 2018. The distributions of income, age, and joining are presented in the following diagram:

<p align="center">
  <img  src="images/analysis1.png"> 
</p>
<br>
We also found that the number of joining customers every year has more males thans femals. Particularly, 2500 of femals joined in 2017 while 3000 of males joined in the same year. In 2018, the number of male customers was tow times the number of femal customers as it is clear in the below chart. 
<p align="center">
  <img  src="images/analysis2.png"> 
</p>

## Building a Model
I built a randomforest classifier to classify an offer wether it will sucsses with a specific customer or not. The model was trained and tested on 66501 instances (80% of the data used for training and 20% of the data used for testing). The model was evaluated in different matrices as followig:

Accuracy of the model on training data:  0.999962406015  <br>
Accuracy of the model on testing data:  0.916773174949
<br>
F1 score on training data:  0.999960197421   <br>
F1 score on testing data:  0.912538516236

From the rvaluation results, we can say that the model can assist in identifying customers who potentialy will take an offer with 91% rate of success.

#### Requirements
Python 3.8 <br>
numpy 1.16.4 <br>
pandas 0.22.0 <br>
matplotlib 2.1.2 <br>
<br>

## Conclusion
In this project, the dataset of Starbucks was investigated and analysed. We found that most of the customers in the age of 50s and have income beteen 60,000 and 80,000. Also, a model of randomforests was trained in the dataset to predict if an offer wehter be sucssess with a scpecific user or not. The model trained and tested and achieved a reasonable accuracy on the testing data. The compled code can be found in the notebook "Starbucks_Capstone_notebook_task". Finally, I would like to thank to Udacity www.udacity.com for offering such a great project.

