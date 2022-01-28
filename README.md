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


### Relationships of Features and Well Status
Our first step was to take a look at the relationships with well status within the dataset.

<img src="images\heatmap.png" width=80%>


### Model
We ran more than 15 models to find the best model that predicts the well status. Although we had models that were more than 99% correct they did not show the same success on the unseen data. In order to prevent this overfitting we ran more models and built a model that shows similar results on both train and test data. Our best model predicted the unseen test data with a score of 81.10% in the Driven Data competition. The competition is going on for 7 years now and the best score is 82.94% 

<img src="images\visualizatdrivendata_submission.png" width=80%><br>

### Features of a Water Well
Our next process was to look at how much effect each feature has on the water well. We ran permutaion importance on our model to see how important our features are. Location of the well is by far the most important one. Another important aspect was the type of the waterpoint. Total Static Head and Construction Year are 2 other important features. It is important to make sure waterpoint has access to enough water when building new wells. The last thing to keep in mind is if a well needs repair we need to check how old is the well as well. Data shows almost all wells are non-functional after 35 years. We suggest that UNICEF do not fix more than 30 years old wells, instead building new wells is a better investment.

Here you can see the status of wells based on what year they were built.
<img src="images\construction_year_status.png" width=80%><br>


### Location, Location, Location

We used our model and specifications to find the kind of house we need and used a algorithm to determine how much that house would cost in different areas. In this case, we looked for three bedroom homes and visualized it on a map.

The more north you go, the prices of homes start to increase. Where as you go south, houses become much cheaper. 

The zip code map on the top shows the areas of lowest average price of homes (where the darker the colored area, the higher the price)  while the bottom depicts the location of homes and their price (where  the darker the color the cheaper it is). We would recommend buying homes in the lighter areas of the zip code map.

<img src="images\3_bedroom_map.PNG" width=80%>

<img src="images\3_bedroom__home_price_map.PNG" width=80%><br>


### Four Bedroom Home Maps
Here we have our 4 bedroom version which we used our algorithm again to determine how much a house would cost in different zip codes. Note that we have fewer zip codes with cheaper homes compared to 3 bedroom homes

<img src="images\4_bedroom_map.PNG" width=80%>

<img src="images\4_bedroom__home_price_map.PNG" width=80%> <br>


### Linear Regression Model
For each data point, we checked against our model. It looks like our model does a decent job with predicting price!

<img src="images\price_predictions_vs_actual_price.png" width=80%>

***
## Conclusion
This analysis gives us three recommendations for purchasing homes for KCHA's Family Matters Program:
- <u> Where should we buy homes? </u>
    - Buy the most amount of homes, target the lighter areas on the zip code map.
<br><br>

- <u>What feature is most important for prices of homes?</u>
    - Grade and square feet living are the most prominent factors in price
<br><br>
- <u>How to search for the best fit home?</u>
    - Use the Robin Hood Algorithm™  to decide whether a specific house is a good buy compared to the KC area.

***
## Next Steps
Further analyses could result with additional insights to further improve our recommendations:
- <u> Where should we buy homes? </u>
    - School district data
    - Crime rate data
    - Zip code area vs socioeconomic status
<br><br>

- <u>What feature is most important for prices of homes?</u>
    - Additional feature data such as garage, size of rooms, or if the home is furnished or not
<br><br>
- <u>How to search for the best fit home?</u>
    - More engineering to streamline the input process

***
## For More Information
Please review our full analysis in our [Jupyter Notebook](./Main.ipynb) or our [presentation]().

For any additional questions, please contact

<img src="images\Hoang.png" width=10%> Hoang Nguyen: hvnguyen90@gmail.com <br />

<img src="images\ferit.png" width=10%> Ferit Yikar: yikarferit@gmail.com <br />

<img src="images\eddie.png" width=10%> Edel Prado: edel.prado.jr@gmail.com <br />


## Repository Structure

```
├── README.md                           
├── Main.ipynb   
├── Presentation.pdf 
├── notebooks  
├── data                                
└── images 
```
