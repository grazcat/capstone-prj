# PORTFOLIO PROJECT


## NON-TECHNICAL EXPLANATION OF YOUR PROJECT

Life expectation is an information that can be useful in several business domains and not. 

Two exampples, among the others

 - Insurance Business: price of life insurance policies vary in function of the life expectation of the specific countries and the healthy habits of the citizens
 - Medical domain: unserstandig the correlation between Life Expectancy and  eating habits, lifestyle, exercise, smoking, drinking alcohol etc.

This projects aims to determine life expectation using as predictors country, morthality, alcohol consumption, infant deaths, diphtheria, population, HIV, hepatite, ...

## DATA
**A summary of the data you’re using, remembering to include where you got it and any relevant citations.**

The dataset has been downloaded from kaggle at the [Life Expectancy (WHO)](https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who) page.

This dataset contains information compiled by the World Health Organization and the United Nations to track factors that affect life expectancy. The data contains 2938 rows and 22 columns. The columns include: country, year, developing status, adult mortality, life expectancy, infant deaths, alcohol consumption per capita, country's expenditure on health, immunization coverage, BMI, deaths under 5-years-old, deaths due to HIV/AIDS, GDP, population, body condition, income information and education.


## MODEL 
**A summary of the model you’re using and why you chose it.**

The model I chose is a linear model fitted by minimizing a loss function loss with SGD (Stochastic Gradient Descent).

Specifically, I am using the SGD Regresssor implementation provided by sci-kt [here](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.SGDRegressor.html#sklearn.linear_model.SGDRegressor)

The gradient of the loss is estimated each sample at a time and the model is updated along the way with a decreasing learning rate.

I chose this model for the linear relation between the features and because offers several hyperparanmeters for the optimization.

A [model card](model_card.md) is available for more info about the model.

## HYPERPARAMETER OPTIMSATION
**Description of which hyperparameters you have and how you chose to optimise them.**

A subset of the hyperparameters accepted by SGD Regressor and that I chose to optimize are

- alpha: Constant that multiplies the regularization term. The higher the value, the stronger the regularization.
- loss: The loss function to be used. The possible values are ‘squared_error’, ‘huber’, ‘epsilon_insensitive’, or ‘squared_epsilon_insensitive’
- penalty: The penalty (aka regularization term) to be used
- learning_rate: ic can be 'constant', 'optimal', 'invscaling', 'adaptive'e 
- max_iter: The maximum number of passes over the training data (aka epochs)
- early_stopping: Whether to use early stopping to terminate training when validation score is not improving

## RESULTS
**A summary of your results and what you can learn from your model**

I got a 0.74 score for the SGD Regressor model without hype rparameters optimization.

Applying Grid Search and Bayesian optimization I obtained 

 - a 0.77 score using Bayesian optimization
 - a 0.78 score using Grid Search optimization

 They mostly got the same values for the hyper parameters, except for
 - **learning_rate**: it was "constant" for the Bayesian optimizer, and "adaptive" for the Grid Search.
 - **max_iter**: 2000 in BayesianOptimization, 3000 in Grid Search

## (OPTIONAL: CONTACT DETAILS)

This is a sample projetc for the AI/ML Certification Course by London Implerial College, no need to include contact details.
