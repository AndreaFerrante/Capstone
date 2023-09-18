# Model Card

We have been pointing to the following model cards examples: [examples from Google](https://modelcards.withgoogle.com/model-reports).
In our case, since we are modelling here a **binary classification problem**, we have compared different algorithms *(SVM, GBM, Logistic Regression, Naive Bayes, Random Forest, kNN)* to find out that Random Forest is the one that performs best. In order to have a correct dataset, we have balanced the data used using [undersampling methodology](https://machinelearningmastery.com/undersampling-algorithms-for-imbalanced-classification/).

## Model Description

**Input:**
  1. **Dataset**: default of *Credit Card Clients Dataset*, it can be downloaded [here](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients) <br>
  2. **Features**: the model takes 23 features as input, which include demographic information such as age, sex, education, and marriage status, and payment history, including the amount of the bill statement and previous payment. <br>
  3. **Preprocessing**: the data is standardized using `StandardScaler` from scikit-learn to have a mean of 0 and a standard deviation of 1. <br>
  
**Output:** 
  1. **Classification**: The output is a binary classification indicating whether a client will default on their credit card payment the next month (1 for default, 0 for not default). <br>
  2. **Probabilities**: The model can also output the probabilities of belonging to each class. <br>

**Model Architecture:** 
  1. **Algorithm**: Random Forest Classifier <br>
  2. **Hyperparameters**: The model's hyperparameters such as `n_estimators`, `max_depth`, `min_samples_split`, and `min_samples_leaf` are optimized using Bayesian optimization with the hyperopt library. <br>
  3. **Library**: scikit-learn Python package widely used. <br>

## Performance

**Metrics**
  1. **Accuracy**: The primary metric used for evaluating the model is accuracy, which is the ratio of correctly predicted observation to the total observations. <br>
  2. **ROC-AUC**: The ROC-AUC score is also calculated to evaluate the model's ability to distinguish between the two classes. <br>
  3. **Confusion Matrix and Classification Report**: these provide a detailed breakdown of the model performance, including *precision, recall, and F1-score.* <br>

**Summary**

  1. **Graph**: a [ROC curve](https://it.wikipedia.org/wiki/Receiver_operating_characteristic) is plotted to visualize the true positive rate against the false positive rate like follows:

![alt text](https://github.com/AndreaFerrante/Capstone/blob/main/images/roc_rf.png)
     
  2. **Data**: the model is evaluated on a test set which is a portion of the total dataset, and *the performance metrics are calculated based on this test set.*

## Limitations

  1. **Imbalanced Data**: the dataset is imbalanced with a higher number of non-default cases, which might lead to a model biased towards predicting the majority class. We have been performed balancing tecniques and, as a future development, *it would be ideal to test balancing tecniques furthermore.*
  2. **Feature Engineering**: the model might benefit from more sophisticated feature engineering to potentially uncover more complex patterns in the data.
  3. **Hyperparameter Tuning**: the Bayesian optimization was performed with a limited number of evaluations, *which might not be sufficient to find the optimal set of hyperparameters.*

## Trade-offs

Every model has its own peculiarities but the all share the same point of attention: *interpretability*.

  1. **Complexity vs. Interpretability**: ***Random Forest is a complex model with many trees***, making it *less interpretable compared to simpler models like logistic regression.*
  2. **Training Time**: Random Forest models generally take a longer time to train compared to simpler models, especially with a large number of trees.
  3. **Overfitting**: While Random Forest is less prone to overfitting compared to individual decision trees, there is still a risk, especially with a large number of trees and deep trees.

