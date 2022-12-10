# Model Card

See the [example Google model cards](https://modelcards.withgoogle.com/model-reports) for inspiration. 

## Model Description

**Input:** Describe the inputs of your model 

- Country: Country
- Adult Mortality: Adult Mortality Rates of both sexes (probability of dying between 15 and 60 years per 1000 population)
- Alcohol: Alcohol, recorded per capita (15+) consumption (in litres of pure alcohol)
- Percentage Expenditure: Expenditure on health as a percentage of Gross Domestic Product per capita(%)
- BMI: Average Body Mass Index of entire population
- Polio: Polio (Pol3) immunization coverage among 1-year-olds (%)
- Diphtheria: Diphtheria tetanus toxoid and pertussis (DTP3) immunization coverage among 1-year-olds (%)
- HIV/AIDS: Deaths per 1 000 live births HIV/AIDS (0-4 years)
- GDP: Gross Domestic Product per capita (in USD)
- Population: Population of the country
- Thinness 1-19 years: Prevalence of thinness among children and adolescents for Age 10 to 19 (%)
- Thinness 5-9 years: Prevalence of thinness among children for Age 5 to 9(%)
- Income composition of resources: Human Development Index in terms of income composition of resources (index ranging from 0 to 1)
- Schooling: Number of years of Schooling(years)

**Output:** Describe the output(s) of your model

- Life expectancy: it is self-explanatory, estimate of the average number of additional years that a person of a given age can expect to live

**Model Architecture:** Describe the model architecture you’ve used

The model is a linear model fitted by minimizing a loss function loss with SGD (Stochastic Gradient Descent).

Specifically, It is the SGD Regresssor implementation provided by sci-kt [here](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.SGDRegressor.html#sklearn.linear_model.SGDRegressor)

The gradient of the loss is estimated each sample at a time and the model is updated along the way with a decreasing learning rate.

The model is well suited for the linear relation between the features and offers several hyperparanmeters for the optimization phase.

## Performance

Give a summary graph or metrics of how the model performs. Remember to include how you are measuring the performance and what data you analysed it on. 

The model has 0.74 score for the SGD Regressor model without hype rparameters optimization.

Applying Grid Search and Bayesian optimization we achieve 

 - a 0.77 score using Bayesian optimization
 - a 0.78 score using Grid Search optimization

They mostly got the same values for the hyper parameters, except for
 - **learning_rate**: it was "constant" for the Bayesian optimizer, and "adaptive" for the Grid Search.
 - **max_iter**: 2000 in BayesianOptimization, 3000 in Grid Search

 The best parameters set is the following one

  - alpha: 0.01
  - early_stopping: True
  - learning_rate: adaptive
  - loss: squared_error
  - max_iter: 3000
  - penalty: l1

## Limitations

Outline the limitations of your model.

It is a regression model, so we need feed the model with all tha parameters it needs. They are actually 15, another regression model can overccome this limitation

## Trade-offs

Outline any trade-offs of your model, such as any circumstances where the model exhibits performance issues. 

The model is linear, so no real performance issues here and no need for an impressive hardware to run the model. Unfortunately, the precision is limited to 0.78