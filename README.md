# Credit Card Clients Default Modelling


## Non-technical explanation of this GitHub repository
This repo contains a *full Machine Learning journey for any financial analyst*, like me, that will be dealing with *credit risk assessments* in his/her career 🚀

Referring to the master piece work about the topic, [Credit Risk Modelling by David Jamieson Bolder](https://link.springer.com/book/10.1007/978-3-319-94688-7?source=shoppingads&locale=en-it), we present different Machine Learning models to determine on the [Taiwan Credit Default dataset](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients) (please, refer to its detailed [data sheet here](DATASHEET.md) and to the data folder where the data is actually in) if a client **will be defaulting or not** during the next month.

The challenge here is to solve a **binary classification problem**: we will determine if an **unknown client** will be dafaulting or not **given previous clients' defaults**. Therefore, We will give a label (default or not-defualt) ti any new *unseen* client.

Each model presented in the Jupyter Notebook has the following procedural steps:

1. *hyperparameters tuning (using [Bayes Optimisation](https://en.wikipedia.org/wiki/Bayesian_optimization)),*
2. *model training and model fitting,*
3. *single model performance metrics evaluation.*

At the end of the notebook, we show the **overall models comparison** to choose the best model among [Logistic Regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html), [Random Forest](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html), [kNN](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html), [Gradient Boosting](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingClassifier.html), [SVM](https://scikit-learn.org/stable/modules/svm.html) and [Naive Bayes](https://scikit-learn.org/stable/modules/naive_bayes.html).
We report that in the Notebook we have performed EDA (i.e. *exploratory data analysis*), just at the beginning of the notebook itself, to balance the dataset.
Please, refer to the model card [here](MODELCARD.md) to gain the model and its processes specifications with deeper details.

Happy coding and learning to you all !


## Data
In order to make this GitHub project as portable as possible but still effective, I have been using the [Default Credit Card Clients](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients) dataset which contains 30.000 obeservations with no missing data and it has a weight of few megabytes ! 
Please, refer to the detailed **data sheet** (it can be found [here](DATASHEET.md)) contained in this GitHub repo for all the possible details about it.

## Models 
As said in the short *non technical* descrition above, we used more than one single model to be compared against each other. These models *are parametric, non parametric and tree based* to better compare all possible aspects.

## Hyperparameter optimisation
In order to perfrom *paramter optimisation* I have been using [Bayes Optimisation](https://en.wikipedia.org/wiki/Bayesian_optimization) on each single model: this is usefule for *better understanding each single model peculiar paramters !* 

## Results
Out of all the models, *ensemble Random Forest Classificator* performs better given the (ROC AUC)[https://developers.google.com/machine-learning/crash-course/classification/roc-and-auc?hl=en] classifier which is very frequently used for *binary classification problems* like this one. To have a closer look to the **ROC**, please refer to image loaded into the  the below image.

## Contact details
Please, let's connect if possible to exchange ideas and points of view ! Here you have my (LinkedIn Profile)[https://www.linkedin.com/in/andrea-ferrante-72b8b343/].
