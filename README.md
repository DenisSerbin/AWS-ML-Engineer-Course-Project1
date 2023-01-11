# AWS-ML-Engineer-Course-Project2
Predict Bike Sharing Demand using AutoGluon

## Initial Training
### AutoML approach (Autogluon)
This project uses AutoGluon to find the most suitable model for demand prediction. After the best model was found, inference was made, and a file with predictions was submitted to Kaggle.

### Top performing model
The best model found by Autogluon was WeightedEnsemble_L3 with the Kaggle score of 1.32845.

## Exploratory data analysis and feature creation

### Exploratory data analysis + additional features
As suggested, the datetime feature was split into year, month and day, and they formed new features. The 'day_of_week' feature was added too.

### Performance with additional features
The best model this time around was still WeightedEnsemble_L3 with a slightly worse Kaggle score of 1.32851.

Obviously, the added features gave more detailed information to models, but it didn't seem to drastically help with the score.

## Hyper parameter tuning
### Performance with different hyper parameters
Two sets of hyperparameters for lightGBM gradient boosted trees and neural networks were added in hope that those types of models would perform better. Indeed, the list of the best performing models this time included a lot of LightGBM models and a couple of NN models. But overall performnce stayed the same: the best model was still WeightedEnsemble_L3 with the Kaggle score of 1.32851.

### The models used + hyperparameters modified, and their Kaggle scores.
![Model comparison](Screenshots/model-comparison.png)

## Summary
Very nice experience with AutoGluon. I learned about it form the course and now I'll try using in my models.
