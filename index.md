# Starbucks-Capstone-Project
<p align="center">
![Image](images/header.png)
</p>
## Project Overview

This is the capstone project of udacity data scientist nanodegree. In this project, the dataset of Starbucks customer behavior is investigated and analysed. Starbucks collects data about customers and how they react with the offers sent via mobile app. The offers might be a discount or buy one get one free (BOGO).

## Problem Statement


## Data Exploration
The data is contained in three files: <br>
profile.json - demographic data for each customer <br>
portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.) <br>
transcript.json - records for transactions, offers received, offers viewed, and offers completed <br>


1- profile dataset
<p align="center">
![Image](images/profile.png)
</p>
<br>
2-portfolio dataset
<p align="center">
![Image](images/portfolio_dataset.png)
</p>

<br>
3-transcript dataset
<p align="center">
![Image](images/transcript.png)
</p>

## Data Preprocessing
It is clear from the data exploration that the data have some issues. In order to improve the qualit of the data, we implemented the following procedures:
<br>

## Data Analysis
After analysing the data of registered customers, we found that most of customers have income in the range (60,000 and 80,000) and in the age of 50s. In addition, the majority of customers joined to app in 2017 and 2018. The distributions of income, age, and joining are presented in the following diagram:

<p align="center">
![Image](images/analysis1.png)
</p>
<br>
We also found that the number of joining customers every year has more males thans femals. Particularly, 2500 of femals joined in 2017 while 3000 of males joined in the same year. In 2018, the number of male customers was tow times the number of femal customers as it is clear in the below chart. 
<p align="center">

![Image](images/analysis2.png)
</p>
## Building a Model
I built a randomforest classifier to classify an offer wether it will sucsses with a specific customer or not. The model was trained and tested on 66501 instances (80% of the data used for training and 20% of the data used for testing). The model was evaluated in different matrices as followig:

Accuracy of the model on training data:  0.999962406015  <br>
Accuracy of the model on testing data:  0.916773174949
<br>
F1 score on training data:  0.999960197421   <br>
F1 score on testing data:  0.912538516236


#### Requirements
Python 3.8 <br>
numpy 1.16.4 <br>
pandas 0.22.0 <br>
matplotlib 2.1.2 <br>
## Conclusion
In this project, the dataset of Starbucks was investigated and analysed. We found that most of the customers in the age of 50s and have income beteen 60,000 and 80,000. Also, a model of randomforests was trained in the dataset to predict if an offer wehter be sucssess with a scpecific user or not. The model trained and tested and achieved a reasonable accuracy on the testing data. The compled code can be found in the notebook "Starbucks_Capstone_notebook_task". Finally, I would like to thank to Udacity www.udacity.com for offering such a great project.

