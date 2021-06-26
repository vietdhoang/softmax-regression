# Multi-Class Logistic Regression and Gradient Descent
**COMP 551: Applied Machine Learning** <br />
**Authors: Viet Hoang, Andrei Dragoi, Weiming Guo**

Logistic regression is one of the most widely used classifiers in academia. Unfortunately, it is only able to classify binary variables and fails in categorical classification problems. Softmax regression, a generalization of logistic regression, addresses this problem. The main objective of this project was to manually implement a softmax regression model that could be used across a variety of datasets and whose performance would be competitive against other classifiers. Three datasets were used to test the accuracy of the model. The first two dealt with images of handwritten digits, and the third dataset consisted of satellite images of the earth’s surface, with the true soil type representing the labels.

## Datasets
We used the following datasets
- [UCI Handwritten Digits Data Set](https://archive.ics.uci.edu/ml/datasets/Optical+Recognition+of+Handwritten+Digits)
- [Semeion Handwritten Digit Data Set](https://archive.ics.uci.edu/ml/datasets/semeion+handwritten+digit)
- [Statlog (Landsat Satellite) Data Set](https://archive.ics.uci.edu/ml/datasets/Statlog+(Landsat+Satellite))

## Methods
To fit the softmax regression model to the data, we determined the optimal parameters for the model by minimizing the cross-entropy cost function. We minimized the cost function using stochastic gradient descent (SGD) with mini-batches and momentum.

## Results
We found that our implementation produced very accurate classifications with all three datasets havingat least 75% accuracy. We also analyzed the effects of the hyperparameters (mini-batch size, learning rate, momentum) on the performance of the models.  Increasing mini-batch size past 10 did little to improve accuracy while also worsening the run-time. Learning rates that were too low (10<sup>-4</sup>) or toohigh (>1) resulted in poorer classification. Finally, high momentum (>0.9) slightly reduced accuracy. When comparing our model with decision trees we found the two to have comparable accuracies with our model being better for the 2 digit datasets and the decision tree slightly outperforming our model in the satellite image dataset.
