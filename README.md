# AWS-ML-Engineer-Course-Project2
Predict Bike Sharing Demand using AutoGluon

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I used AutoGluon on the tarin data and then ran "predict" on the test data: the output didn't contain negative values, so I submitted the
predictions without any adjustments. The submissions file went through on Kaggle without any issues.

### What was the top ranked model that performed?
It was WeightedEnsemble_L3 with the Kaggle score of 1.32845.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
As suggested, I split the datetime feature into year, month and day, and made them new features. I also added the 'day_of_week' feature.

### How much better did your model preform after adding additional features and why do you think that is?
The best model this time around was still WeightedEnsemble_L3 with a slightly worse Kaggle score of 1.32851.

Obviously, the added features gave more detailed information to models, but it didn't seem to help with the score.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
I added two sets of hyperparameters for lightGBM gradient boosted trees and neural networks hoping that those types of models would
perform better now. Indeed, the list of the best performing models this time included a lot of LightGBM models and a couple of NN
models. But overall performnce stayed the same: the best model was still WeightedEnsemble_L3 with the Kaggle score of 1.32851.

### If you were given more time with this dataset, where do you think you would spend more time?
I would experiment with feature engineering and hyperparameters more.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
![model-comparison.png](img/model-comparison.png)
          
### Create a line plot showing the top model score for the three (or more) training runs during the project.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

![model_test_score.png](img/model_test_score.png)

## Summary
Very nice experience with AutoGluon. I lerned about it form the course and now I'll try using in my models.
