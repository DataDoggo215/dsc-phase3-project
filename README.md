# **Improving Water Well Quality in Tanzania**

**Authors:** _Hoang Nguyen, Ferit Yikar, Edel Prado_


## Overview


## Business Problem

There are a lot of water wells in Tanzania. About half of them are either non-functional or needs repairing. We need to come up with a model that gives us the status of the wells. Using this model we can identify which wells need to be repaired. 

***
## Data
We have a data from 59.400 water wells on which we made our model. This data consists of various specifications such as who built the well, where is the well located, when it was built and what is the quality/quantity of the water. We are trying to understand if we can predict the status of the well from these specifications. We then compare our best model to another data of 1111 wells to which we do not know the status of the wells. With this we can see how succesful our model is when predicting unseen data.

***
## Methods
This project uses various models to understand how our parameters affect the status of the wells. We built pipelines using knn model, decision tree model, random forest model, bagging model etc. and since our data was not equally distributed between functional, non-functional and needs repair wells we used SMOTE to create dummy rows that will result in a data set with equal ratios to each status. We compared the scores we get from different models to find the best one.
***
## Results