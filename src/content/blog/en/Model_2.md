---
title: Model Selection II
draft: false
author: Wilson Estrada,Yordy Gonzales, Felipe Benitez, Yuly Meza 
tags:
  - Optimization
image:
  src: https://i.ibb.co/mJJc3y8/decapcms.png
  alt: Model Selection II
snippet: Model Selection II
publishDate: 2024-01-01 12:00
category: Model Selection II
---

### Details about your selection

In this case, we chose a type of neural network known as an MLP (Multilayer Perceptron). After cleaning the data and removing dimensionless data, we eliminated outliers that exhibited highly unusual behavior compared to the distributions of other diamond features and measurements. We opted for neural networks because we observed that the data's behavior was not strictly linear, and we wanted to capture that non-linearity in some way. Neural networks offer us the possibility to do this thanks to their multiple layers and the weights between neurons that adjust with the data. Additionally, their strength lies in their ability to learn complex patterns and relationships, making them suitable given that the customizable architecture of MLP allows us to adjust the network's topology to optimize performance.

![RN ARCH](https://github.com/wilsone24/Optimization-Project/assets/118389840/276c172b-8880-4180-8329-57c2ee6b3fa6)

The next step was to discretize the qualitative variables, assigning them a corresponding value to observe their influence on the model's quality. After conducting tests, we chose Carat and Z as our inputs, which, as mentioned in the previous model, largely explain the diamond's price. Additionally, we added 'cut', 'color', and 'clarity', initially categorical and now numerical, as inputs because we observed that they have a greater influence than the other numerical variables. After several benchmarks with different architectures to find the optimal one, we used the following configuration: 5 inputs, 7 hidden layers (20 neurons per layer), 1 output, default Alpha, maximum 600 iterations, and Relu activation function (which provided the best result).

### Validation method and metrics

Cross-validation technique was used to avoid overfitting or bias issues, with an 80% data partition for training and the remaining 20% for testing. This allowed us to evaluate the model with data it hadn't seen before. Due to the prolonged duration of the process and the associated computational cost, attributed to the large amount of data, only 20 iterations were conducted to observe the score distribution across different data partitions. This helped us determine how sensitive the score is to data partitioning and how scattered the values are around the most likely score.

![Regression RN](https://github.com/wilsone24/Optimization-Project/assets/118389840/6255603a-459f-4f43-88e6-a8a1b2bb3ad2)

We obtained an average score of 0.9757, which is where the highest density is observed, with an operational margin of 0.5%. This means that the score can fluctuate between values close to 97% and 98% with the same probability. These results give us a good idea of the model's quality in relation to the data.

![Scores Rn](https://github.com/wilsone24/Optimization-Project/assets/118389840/bfe83748-4967-40ea-81c0-80346283f111)

Afterward, the loss curve was observed to understand how the process improves over iterations. It can be seen that only 175 iterations out of the initially indicated 600 were necessary, and the process stopped there because no substantial changes in the loss function were observed.

![Loss Curve Rn](https://github.com/wilsone24/Optimization-Project/assets/118389840/36d594ee-5625-4f70-ac99-16b59b932826)

The correlation between the variables and the weights assigned in the last layer concerning the output is evident.

![Both_2 RN](https://github.com/wilsone24/Optimization-Project/assets/118389840/c945c06e-04dd-4ba9-b666-b9e1efa53e39)

The last iteration was chosen to observe its score (how good the model is) and to get a good idea of the MSE and RMSE, which allows us to evaluate how close the model's predictions are to the actual values.

| Metric    | Value     |
|-----------|-----------|
| Score    | 0.973224   |
| MSE      | 427736.75  |
| RMSE     | 654.0158   |

The distribution of residuals and predicted values was verified compared to the actual data to evaluate the model's quality more accurately. It was found that the highest density of residuals is centered around 0, and the distribution of predicted values is very similar graphically to that of the actual values. Although there are certain peaks where they differ, the difference is minimal.

![Both_1 RN](https://github.com/wilsone24/Optimization-Project/assets/118389840/2be81d1b-ec71-4ab7-877d-d80109430336)

### Preliminary conclusions

* The model achieved an excellent score, indicating that it is very good and describes the output variable well.

* It is noted that, although the score is very high, there is still some lack of precision in predicting the price given the values of MSE and RMSE.

* The proposed categorical variables have a significant influence on the diamond price behavior.

* The number of layers in the proposed architecture allows for representing much more complex relationships, aiding in capturing a greater variability of the data.

* In other words, the high number of layers and neurons significantly influence the model's quality.

* The predictions align very well graphically with reality, increasing confidence in the model and suggesting it could be implemented in the market.

### How does this model compare to the first one?

* The score was improved, increasing from 0.88 to 0.975, indicating an improvement in the model's quality.

* Regarding the obtained residuals, there is a reduction in their dispersion in the neural network compared to linear regression.

* Metrics such as MSE and RMSE were lower in the neural network than in linear regression, indicating an improvement in accuracy when predicting the data.

* When comparing the regression plots in both the neural network and linear regression to visualize the relationship between the model's prediction and the actual values, a reduction in the variability of the slope, which would be the score, is observed.

* When comparing the distribution plots of predictions and actual values of both models, it can be seen how in the neural network, the predictions more closely resemble the actual values, although not perfectly, but the distribution is very similar.

* All of this suggests that with the neural network architecture, much more complex relationships can be captured than with linear regression.