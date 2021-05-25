# 🏅Loan-Approval-Analysis🏅

Based on the data provided by Kaggle, I have taken on a challenge to analyze and model the data, and then come up with an improved method to identify whether the customer will default on the loan, thus analyzing and predicting whether the accepted loan will be good or bad. The hope is that this project will provide some useful advice to identify risky loans, mitigate some potentially harmful lending practices or screen out a group of qualified lenders. It is also desirable to ensure that accepted loans conform to best lending practices, laws and regulations by verifying that the rates offered properly reflect the borrower's credit history and current creditworthiness.

## Dataset Information 
This dataset is from Kaggle with 2 files,  in the following https://tinyurl.com/wnrcn9x. This project is mainly focused on the one with accepted loans. And the target variable is loan_status. The accepted loan data has 2,260,701 rows. This is a dataset from 2007 to 2018 for LendingClub data, with US based financial information ranging from loan length to applicant credit score. 

## Skills used


## Requirements 
* Data Cleaning 
* Exploratory Data Analysis 
* Permutation testing
* Polynomial features
* Data Modeling
* Machine Learning Model Pipelines
* Hyperparameter Tuning

### Libraries are required as follows
```
from pydrive.auth import GoogleAuth
from pydrive.drive import GoogleDrive
from google.colab import auth
from oauth2client.client import GoogleCredentials
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import warnings
```
## Results
### Fit Models (using samples)
```
Logistic Regression: 
0.989107 (0.003430)
```
```
Random Forest Classifier: 
0.981786 (0.003174)
```
```
Gradient Boosting Classifier: 
0.981786 (0.004286)
```
```
Extra Trees Classifier: 
0.985179 (0.003997)
```
```
Decision Tree Classifier: 
0.964107 (0.007595)
```
```
SVC: 
0.977500 (0.003763)
```
```
Linear Discriminant Analysis: 
0.972143 (0.006298)
```
```
Gaussian NB:
0.899464 (0.028949)
```
### Fit the Best Model
* Logistic Regression (Using Sample)
```
Model.score(X_test, Y_test.ravel())
0.9929
```
### Refit on Entire Rows (Entire Dataset)
```
Model.score(X_test, Y_test.ravel())
0.6279
```
## Conclusion
Overall, although the model was not very accurate when tested on the entire dataset, with an accuracy rate of about 62.8 percent, it was still effective at predicting whether someone would default on a loan. 

In addition to including statistics related to age and marital status, the model could make a major improvement by exploring the GDP of the US at the time the loan was accepted. In theory, it not only improves the accuracy of the model because it takes into account the health of the US economy at the time, but also allows the model to be segmented by GDP growth rates.




<!---
yixuanlu17/yixuanlu17 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.

## Project Descriptions: 
Have a video demo if you cannot deploy. 
Project Requirements: What is needed to run the code. 
Project Results: information detailing project results. 
Project Contributors: Add people who worked on the project, and what their roles were. 
References: Add any references, or give credit to code that you’ve referenced or used. 

## Dataset Information 
The data come from the Open Data website of the UK government, where they have been published by the Department of Transport.

The dataset comprises of two csv files:

1. AccidentInformation.csv: every line in the file represents a unique traffic accident (identified by the AccidentIndex column), featuring various properties related to the accident as columns. Date range: 2005-2017

2. Vehicle_Information.csv: every line in the file represents the involvement of a unique vehicle in a unique traffic accident, featuring various vehicle and passenger properties as columns. Date range: 2004-2016
The two above-mentioned files/datasets can be linked through the unique traffic accident identifier (Accident_Index column).

The dataset will keep being updated as more data become available by the Department of Transport.

## Requirements 

### Libraries are required as follows

* `numpy`
* `pandas`
* `matplotlib`
* `seaborn`
* `datetime`
* `geopandas` 
* `scikit-learn`

## Results

* We started our analysis with exploratory data analysis to discern the dataset. Machine learning algorithms were used to explore the complex interactions among roadways, traffic, environmental elements and predicting accident severity. Since most of the predictor variables in the dataset were categorical, we recoded categorical variables. 11 models were built, evaluated for complexity and accuracy, and compared to conclude which model is the best fit for predicting accident severity. 

* Spot Checking technique was used to fit the 11 models to determine which models would predict the accident severity with the highest accuracy. We also performed feature engineering to enrich our dataset Hyperparameter tuning and pipelining the best performing model helped to improve the performance of the model by making accurate predictions. Gradient Boosting performed well with the accuracy of 86.71% and which were further improved by doing permutation testing for feature importance which played an important role in predictions.

```
Logistic Regression_1
56.33
Random Forest_1
60.52
Gradient Boosting_1
86.71
Linear Discriminant Analysis_1
55.76
Extra Trees_1
58.62
Bagging_1
55.67
```

#### Gradient Boosting scores
```
Model	Score
0	Gradient Boosting_1	86.71
```

#### Conclusion
Among all other techniques used, Gradient Boosting Classifier has performed best with the highest accuracy. One reason why RF works well is because the algorithm can look past and handle the missing values in the tweets.

#### Project Contributer
Lei Cao 

--->
