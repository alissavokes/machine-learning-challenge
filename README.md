# machine-learning-challenge

## Background

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, you will create machine learning models capable of classifying candidate exoplanets from the raw dataset.

In this homework assignment, you will need to:

1. Preprocess the raw data
2. Tune the models
3. Compare two or more models

### Preprocess the Data

* Preprocess the dataset prior to fitting the model.
* Perform feature selection and remove unnecessary features.
* Use `MinMaxScaler` to scale the numerical data.
* Separate the data into training and testing data.

### Tune Model Parameters

* Use `GridSearch` to tune model parameters.
* Tune and compare at least two different classifiers.

### Reporting

* Compare each model's performance as well as summarize your findings
- - -

## Analysis

The two models used were k Nearest Neighbors (kNN) and Support Vector Machine (SVM). The feature selection was determined by using sklearn.feature_selection to remove columns that had at least 80% probability of containing the same or similar values in each row. The training and testing scores for the kNN model were plotted for odd valued neighbors between 1 and 20. Based on the plot, it appeared that 13 neighbors would be best (it also had the highest testing accuracy of 0.617), however when using grid search it was determined that only 11 neighbors were needed for the best model. Even after tuning, the accuracy was only 0.63 indicating that the kNN model was not the best model for predicting new exoplanets.

The other model used was SVM. It used the same features as the kNN model, but had a slightly higher testing accuracy of 0.66 and ended up with a higher best grid search score of 0.68. The SVM model seems to be a more accurate predictor or new exoplanets, but still not a great model to use. In order to improve the SVM model, a different kernel could be used. The linear kernel might not be the best kernel function and using a non-linear kernel could improve model accuracy.

## Resources

* [Exoplanet Data Source](https://www.kaggle.com/nasa/kepler-exoplanet-search-results)

* [Scikit-Learn Tutorial Part 1](https://www.youtube.com/watch?v=4PXAztQtoTg)

* [Scikit-Learn Tutorial Part 2](https://www.youtube.com/watch?v=gK43gtGh49o&t=5858s)

* [Grid Search](https://scikit-learn.org/stable/modules/grid_search.html)
