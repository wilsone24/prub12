---
title: "Dataset selection"
draft: false
author: Wilson Estrada,Yordy Gonzales, Felipe Benitez, Yuly Meza 
tags:
  - Optimization
image:
  src: https://cdn-icons-png.flaticon.com/512/2103/2103787.png
  alt: Diamonds
snippet: Dataset selection
publishDate: 2024-01-01 12:00
category: Dataset selection
---

![Diseño sin título](https://github.com/wilsone24/Optimization-Project/assets/118389840/00704de8-ad2e-408e-b2c7-7f3410716ddd)


After examining various datasets from which a future model could be derived, we chose this one due to certain variables, such as the quantity of data it contains, around 53,940 rows where valuable information can be extracted. This substantial amount of data allows for a more profound, clear, and optimal analysis of the problem. Additionally, it is known that diamond prices pose a problem that affects people every day, creating economic difficulties, primarily focusing on individuals with the economic capacity to access these goods or entrepreneurs engaged in this business. Therefore, its impact on both the economy and the daily lives of people makes it a suitable dataset and problem to address. Similarly, the variables included in the dataset are well-known, easy to relate to when analyzing the problem, and the correlations found would facilitate the creation of our model. Finally, we consider that dealing with diamonds is not common, and for that reason, it seemed more interesting to us.

### Our Team

| ![Integrante 1](https://github.com/wilsone24/Optimization-Project/assets/118389840/1ad141ba-4520-4d3e-add6-724df3f272ce)  | ![Integrante 2](https://github.com/wilsone24/Optimization-Project/assets/118389840/92da7de6-a034-40f4-affa-2887ebc5fed3)  |
| --- | --- |
| **Data engineer**  Wilson Estrada Ortega is a student at the Universidad del Norte in the systems engineering program in seventh semester, graduated from Biffi La Salle school in 2020, his area of interest is focused on the management of big data, cloud computing and technology sales. He has knowledge in various programming languages but focuses mainly on python and sql for data manipulation. He is passionate about sports and learning new things. The role he will develop in the team will be a data engineer and he will be one of the people in charge of data manipulation and data cleaning. | **Data engineer** Yuli Meza Barros, 22 years old student on 9th-semester of systems engineering at Universidad del Norte, completed her studies at Nuestra Señora de Lourdes School in 2019. With a profound interest in cybersecurity, she demonstrates proficiency in Java and Python programming languages. Her fascination extends to data analytics, showcasing a versatile skill set. In the team, Yuli plays a vital role as a data engineer, specializing in meticulous data manipulation and cleaning processes  Her diverse interests and skills contribute to the dynamic and collaborative environment within the team. |

| ![Integrante 3](https://github.com/wilsone24/Optimization-Project/assets/118389840/d1a88f04-6a50-42de-9387-6965a03343dd)  | ![Integrante 4](https://github.com/wilsone24/Optimization-Project/assets/118389840/85134bbd-01ca-44b2-8ed7-af2ecd0a8bcb)  |
| --- | --- |
| **Backend engineer** Felipe Benítez, a seventh-semester student at Universidad del Norte, graduated from nuevo colegio del prado, has a keen interest in backend development, databases, and distributed systems. With a passion for crafting robust solutions and learning from existent ones. Outside of the tech realm, Felipe enjoys expressing his creativity through drawing and has a particular fondness for manga. | **Frontend engineer** Yordi González, a seventh-semester systems engineering student at Universidad del Norte, graduated from I.E.T.C. Francisco Javier Cisneros at 2020, who has some experience in backend development and database management. Proficient in Python, SQL, and relational databases. Dedicated to designing efficient systems to meet project goals. I am responsible for the visual part of the project emphasizing the user experience. |

### Visualizations

![graphs](https://github.com/wilsone24/Optimization-Project/assets/118389840/b730627f-6528-478d-a752-e4925849b160)

### Statistical insights

Taking into account the following analysis and observing the dataset, we can derive the following premises:

* Diamond prices range from $326 to $18,823, with a mean of 3932.79. Additionally, the objective is to analyze the distribution and identify patterns in different price ranges.

* Despite the presence of outliers, concerning the dimensions x, y, z of the diamonds, they follow a trend that can be linearly modeled in each of the proposed graphs. The respective means for each dimension are: x (5.731157), y (5.734526), z (3.538734). The dimensions include length (x) ranging from 0 to 10.74 mm, width (y) ranging from 0 to 58.9 mm, and depth (z) ranging from 0 to 31.8 mm. The goal is to explore the relationship between physical dimensions and diamond prices, considering the importance of shape and proportions.

* Other observations: We observe that the trend of carats concerning the price of diamonds follows a quadratic function, where the data is not dispersed as much. Carat weights vary from 0.2 to 5.01, with a mean of 0.797940. The correlation coefficient of this variable with respect to the diamond price is the highest and is 0.92.

* The other variables, both qualitative and quantitative, also influence the diamond price but not as much as those mentioned earlier. We observe that as the count decreases, the price is lower, and the density concerning the price follows two trends, first rising and then declining.

![Matriz de correlación](https://github.com/wilsone24/Optimization-Project/assets/118389840/cf952684-999a-4dfd-baf5-8bac9e6194fe)

### Hypothesis

Taking into account various observations, it is necessary to highlight the initial hypothesis that the working team has about the dataset. Diamond prices do not depend solely on a particular variable; instead, they are determined and influenced by multiple variables, such as each of the different dimensions and weight, which collectively impact the price. This is the hypothesis we will be developing throughout the model with the objective of identifying which variables have a greater influence on diamond prices and in what manner.