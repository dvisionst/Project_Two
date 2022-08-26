# Predicting The Potability of Water
## Using Predictive Machine Learning Models
Author: Jose Flores

## Problem Statement:
Using data authored by Aditya Kadiwal in regards to water in order to determine if it is drinkable or not.

## Data:
Original data was downloaded from https://www.kaggle.com/datasets/adityakadiwal/water-potability.
This dataset has 10 columns and 3276 rows. This dataset will be used for this classification problem. The column description for the dataset is as follows:
Column description:

1. ph: pH of 1. water (0 to 14).
2. Hardness: Capacity of water to precipitate soap in mg/L.
3. Solids: Total dissolved solids in ppm.
4. Chloramines: Amount of Chloramines in ppm.
5. Sulfate: Amount of Sulfates dissolved in mg/L.
6. Conductivity: Electrical conductivity of water in μS/cm.
7. Organic_carbon: Amount of organic carbon in ppm.
8. Trihalomethanes: Amount of Trihalomethanes in μg/L.
9. Turbidity: Measure of light emitting property of water in NTU.
10. Potability: Indicates if water is safe for human consumption. Potable -1 and Not potable -0

## Methods:
I chose to use a simple impuder because 14.9%  of the ph column had missing values. I did not want to risk the loss of information in that feature along with the missing Sulfates (23.8%) and Trihalomethanes(4.9%). I chose the mean imputation strategy with the simple Imuder because all three of the aforementioned features are normally distributed. 

## Results:

Here are two visualizations from the data set. 

![image](https://github.com/dvisionst/Project_Two/blob/main/%231.png)

The plot shows the different averages of the sulfates and hardness of the water. Both are measured in milligrams per liter. As can be seen for this particular dataset, water on average has a higher sulfates measure than hardness.




 ![image](https://github.com/dvisionst/Project_Two/blob/main/%232.png)

The plot shows averages of the cholormines and organic carbons in the water. Both are measured in parts per million (ppm). The chart shows that on average there is a higher amount of organic carbon than cholormines in this water dataset. 

## Model:

The final model that will be chosen is the KNN model. Potable water is of the upmost importance, people rely on it to drink, cook, and clean. They can’t be using water that’s non-potable because it could be severely detrimental to their health. This is why I decided to base my decision on the Precision of the model. If I were to only consider the Accuracy metric the KNN model is the choice as it leads the way with a max accuracy of 0.66 compared to the other three models. Overall the KNN outperforms the Logistic Regression, KNN with PCA, and Decision Tree models in Accuracy, Precision, Recall, and F1 Score. The poorest performing model was the Logistic Regression model, this could be due to the fact that the dataset didn’t have any linear relationships between features All of the metrics can be seen in the table below and it clearly shows why KNN is the chosen model. 

![image](https://github.com/dvisionst/Project_Two/blob/main/Water_Table.png)

## Recommendations:
It may be a fruitful endeavor to next time focus on some feature engineering techniques with the dataset. For example kmeans could be used to cluster the data, and create a whole new column. Adding the cluster data could reveal potential non-linear relationships that aren’t easy to observe through linear methods.  In general doing feature engineering to create more ways to interpret the dataset. 

## Limitations & Next Steps:
Besides the obvious limitation of not having enough data, the biggest limitations were the zero correlations and non-linear relationships. It was limited in being able to succinctly visually present the data to a non-technical audience. Time was spent in trying to find any relationship between features through different filters using the potability column. A pairplot was even created which just confirmed that the data had no correlations or linear relationships. This also affected the predictive ability of the models, in particular the Logistic Regression model. With more focus on feature engineering a better model could be built. 

## For further information:
For any additional questions, please contact me at dvisionstwat@gamil.com 


