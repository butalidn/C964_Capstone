# NBA Player Salary Machine Learning Project: Capstone

This project was the final project of my WGU degree. The purpose of the project was to develop a machine learning solution to solve a business problem. A formal proposal was written to describe the product and its implementation and is included in this repo. 

Click [here](https://github.com/butalidn/C964_Capstone/blob/main/NBA%20Machine%20Learning%20Project.ipynb) for the original Jupyter Notebook file

The business problem I attempted to solve was how to better optimize a NBA team's cap space. The application aimed to solve this issue by using machine learning to determine a player's monetary value based on their given stats for a year. 

The development of the project followed the SEMMA (Sample, Explore, Modify, Model, and Assess) methodolgy. The main source of data came from a Kaggle.com [dataset](https://www.kaggle.com/datasets/sumitrodatta/nba-aba-baa-stats?select=Advanced.csv). The data was scraped by a contributor from the Basketball-Reference website. 

A combination of advanced metrics and basic basketball statistics were analyzed against the salaries of NBA players from 2000 to 2020. After the data was cleaned up and imputed, a model using scikit-learn's [Random Forest Regressor](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html) estimator was created. Once the initial model was fitted and scored, the model was improved by using scikit-learn's [Randomized Search CV](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.RandomizedSearchCV.html) function. It utilizes cross-validation over a randomized set of hyperparameters to find the best settings for a machine learning model.

After an improved model was created, the model was evaluated using mean absolute error, mean squared error, coefficient of determination score, and mean absolute percentage error. The model found *games started, player efficiency rating, and value over replacement player* to be the top three features that contribute to a player's salary. The r-squared value of the improved model, however, was only a **0.473** which is not a strong enough correlation to make any definitive claims. Areas of improvement include: more relevant data, incorporating inflation between years, larger data sets, a different base model, different hyperparameters and many more. No cloud computing was utilized during this project so that could also be incorporated.

Once the model was completed, a web application was created using Heroku, a cloud hosting platform. The application includes the original dashboard of the Jupyter Notebook and the ability to input different statistics for the model to determine a NBA salary from. 

[Link](https://butalid-c964.herokuapp.com/) for the web app.
**Warning: the web app takes a minute or two to start up**
