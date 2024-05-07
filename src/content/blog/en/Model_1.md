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

### Objectives

* Identify the variables (dimensions and characteristics) that explain to a greater extent the behavior of diamond prices to build the predictive model and understand how these variables affect them.

* Compare different models to determine which one offers the best accuracy.

* Have an impact on the diamond market analysis by allowing for a more effective evaluation of their prices.



### Details about your selection

First, we clean the data to remove dimensionless diamonds. Based on the initial analysis, we choose a linear regression model due to the high correlation between price and many variables, considering that there could be a linear relationship and price is a continuous variable. We select carat and z as our model variables.

![Eq Model](https://github.com/wilsone24/Optimization-Project/assets/118389840/3fa4acae-745c-4587-9c9e-854537ef6ec9)

We opted for carat and z because, in our opinion and according to our descriptive analysis, they are the variables that most characterize the price of diamonds. Carat represents the weight of the diamond, and z represents the depth. According to our research, the greater the weight and depth of the diamond, the higher its cost. We discarded the other dimensions (x, y) because when included in the model alongside carat and z, a high correlation was observed among them, and the model's outcome did not significantly vary. Therefore, we selected the variable that had the most influence on the model among the three dimensions. In this initial part of the analysis, we did not use the categorical variables from the dataset because we considered them not highly relevant in this context.

![Diamond dimension](https://github.com/wilsone24/Optimization-Project/assets/118389840/b96a148f-89b6-4daa-a256-ecff1550e735)

### Validation method and metrics

For the model validation process, cross-validation technique was employed to flag problems such as overfitting or selection bias. The data was divided into training and testing sets, with an 80-20 ratio, respectively. First, a linear regression model was fitted using the training data, and then the obtained model was validated using the test data to evaluate its performance against data not seen during the model training.

![Score and Residuals](https://github.com/wilsone24/Optimization-Project/assets/118389840/39263c05-fecb-45b2-9a39-140bb3661a3f)


To primarily evaluate the predictive capability and performance of the model, the score or the coefficient of determination R2 was used as a metric to analyze the correlation between the model predictions and the actual data. We consider this to be the best measure as it provides an idea of the model's fit quality to the data. Additionally, the MSE and RMSE were obtained to assess how close the model predictions are to the actual values.

| Metric    | Value     |
|-----------|-----------|
| Score    | 0.8558926  |
| MSE      | 2257140.68 |
| RMSE     | 1502.378   |

### Preliminary conclusions

* It can be established by observing the score that the model is good and largely describes the variability of the price.

* I t is noted that with the other measures, the model is not the most precise; price predictions are not exact and have a margin within which the predicted value can differ from the actual one.

* After many tests, it has been determined that the variable that most influences the model is carat.

* A pattern is observed where the model does a much better job of predicting relatively low diamond prices than high prices, where precision is lower.

* It is essential to evaluate how significant the difference between actual and predicted values would be for practical use in the market. If exact precision is not needed, the diamond price could be adequately described in this manner.