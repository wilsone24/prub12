---
title: Model Selection I
draft: false
author: Wilson Estrada,Yordy Gonzales, Felipe Benitez, Yuly Meza 
tags:
  - Optimization
image:
  src: https://i.ibb.co/mJJc3y8/decapcms.png
  alt: Model Selection I
snippet: Model Selection I
publishDate: 2024-01-01 12:00
category: Model Selection I
---

![LR](https://github.com/wilsone24/Optimization-Project/assets/118389840/b83ba0e1-dd6a-4172-a639-d92c63abb7b0)

### Objectives

* Identify the variables (dimensions and characteristics) that explain to a greater extent the behavior of diamond prices to build the predictive model and understand how these variables affect them.

* Compare different models to determine which one offers the best accuracy.

* Have an impact on the diamond market analysis by allowing for a more effective evaluation of their prices.

### Details about your selection

First, we clean the data to remove dimensionless diamonds and eliminate highly atypical diamonds that could pose difficulties for model development. Based on the initial analysis, we choose a linear regression model due to the high correlation between price and many variables, considering that there could be a linear relationship and price is a continuous variable. We select carat and z as variables for our model.

![Diamond dimension](https://github.com/wilsone24/Optimization-Project/assets/118389840/b96a148f-89b6-4daa-a256-ecff1550e735)

We opted for carat and z because, in our opinion and according to our descriptive analysis, they are the variables that most characterize the price of diamonds. Carat represents the weight of the diamond, and z represents the depth. According to our research, the greater the weight and depth of the diamond, the higher its cost. We discarded the other dimensions (x, y) because when included in the model alongside carat and z, a high correlation was observed among them, and the model's outcome did not significantly vary. Therefore, we selected the variable that had the most influence on the model among the three dimensions. In this initial part of the analysis, we did not use the categorical variables from the dataset because we considered them not highly relevant in this context.


### Validation method and metrics

For the model validation process, a cross-validation technique was employed to detect issues such as overfitting or selection bias. The data was divided into training and testing sets, with an 80-20 ratio, respectively. The process was repeated 1000 times, where in each iteration, a linear regression model was first fitted using the training data, and then the obtained model was validated using the testing data to evaluate its performance against unseen data during the model training. This allows us to have a better insight and overview of the overall model quality rather than just under one data split, so in each iteration, samples were taken to better understand the model's behavior.

![Score_Dis_M1](https://github.com/wilsone24/Optimization-Project/assets/118389840/6305f86d-d963-4889-af96-f325d1f7d940)

At the end of the 1000 iterations, an average score of 0.8564 was achieved, which is the peak of the bell curve and where there is the highest density of score samples. This is not the actual score of the model, but rather an approximation through the distribution of the samples taken. An operating margin of 1.5% was obtained, where scores can range from 84% to 87% depending on the partition.

![Intercept_Dis_M1](https://github.com/wilsone24/Optimization-Project/assets/118389840/11daf39e-4388-478f-bfd6-afda7349de6d)

At the end of the 1000 iterations, an average intercept of 3170.410 was achieved. An operating margin of 400 was obtained, where intercept values can range from 2800 to 3600, depending on the partition.

![Params_Dis_M1](https://github.com/wilsone24/Optimization-Project/assets/118389840/85cad72b-de00-4c60-982e-ccd1208a78ac)

At the end of the 1000 iterations, an average carat of 10976.82 and an average z of -2258.90 were achieved. It can be observed that the relationship between the two parameters is inversely proportional: as the carat increases, the z decreases in value, according to the distribution of the parameters. For the final model, the average values of both the intercept and the parameters were applied to conduct various validations of the model and assess how good it is. Additionally, the correlation of the variables in our new model is also shown.

![Eq_M1](https://github.com/wilsone24/Optimization-Project/assets/118389840/e1b48ccc-0315-45dc-a3a5-bdfc8f3edb81)

![123](https://github.com/wilsone24/Optimization-Project/assets/118389840/bdfe8b9d-c86a-4878-b53c-5dfd0f9b74df)

The correlation between the variables of the final model was obtained, noting that they are highly correlated and that removing one would not result in a drastic change in the model's score. It would have an impact and it would be lower, but not drastically so. The regression is observed, showing how well the model fits the data, how much dispersion of the model is captured by the data, and whether what the model says is actually true.

![Res-Pred-Real__M1](https://github.com/wilsone24/Optimization-Project/assets/118389840/238e86c3-06b9-44cc-9b6c-341065ef874d)

Likewise, to obtain other ways of visualizing the model's quality, we chose to observe the distribution of residuals and the comparison between predicted and actual values. It was found that the highest density of errors is centered around 0; however, there is dispersion and uncertainty. In another graph, it was observed that although initially there is a higher density of data corresponding to lower-priced diamonds, the distributions of the actual and predicted values are similar but differ slightly. As the diamond price increases, it is observed that the behavior of the actual values is not fully captured in the distribution of the predicted values. To primarily evaluate the predictive capability and performance of the model, the R2 score or coefficient of determination was used as a metric to analyze the correlation between the model's predictions and the actual data. We consider this to be the best measure as it provides an idea of the quality of the model's fit to the data. Additionally, the MSE and RMSE were calculated to assess how close the model's predictions are to the actual values. All of this was done considering the model created from the average of the coefficients and intercept, which resulted in a slightly higher score than the average.

| Metric    | Value     |
|-----------|-----------|
| Score    | 0.8669998  |
| MSE      | 2077644.93 |
| RMSE     | 1441.403   |

### Preliminary conclusions

* It can be established by observing the score that the model is good and largely describes the variability of the price.

* I t is noted that the model is not the most precise; price predictions are not exact and have a margin within which the predicted value can differ from the actual one.

* After many tests, it has been determined that the variable that most influences the model is carat.

* A pattern is observed where the model does a much better job of predicting relatively low diamond prices than high prices, where precision is lower.

* It is essential to evaluate how significant the difference between actual and predicted values would be for practical use in the market. If exact precision is not needed, the diamond price could be adequately described in this manner.