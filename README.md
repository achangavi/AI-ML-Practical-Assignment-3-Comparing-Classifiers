### Summary (obtained from project description within ipynb file):
**Overview**: In this practical application, our goal is to compare the performance of the classifiers we encountered in this section, namely K Nearest Neighbor, Logistic Regression, Decision Trees, and Support Vector Machines.  We will utilize a dataset related to marketing bank products over the telephone.  

### Data (obtained from project description within ipynb file):

https://archive.ics.uci.edu/dataset/222/bank+marketing

The data is related with direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be ('yes') or not ('no') subscribed. 

There are four datasets: 
1) bank-additional-full.csv with all examples (41188) and 20 inputs, ordered by date (from May 2008 to November 2010), very close to the data analyzed in [Moro et al., 2014]
2) bank-additional.csv with 10% of the examples (4119), randomly selected from 1), and 20 inputs.
3) bank-full.csv with all examples and 17 inputs, ordered by date (older version of this dataset with less inputs). 
4) bank.csv with 10% of the examples and 17 inputs, randomly selected from 3 (older version of this dataset with less inputs). 
The smallest datasets are provided to test more computationally demanding machine learning algorithms (e.g., SVM). 

The classification goal is to predict if the client will subscribe (yes/no) a term deposit (variable y).

## Methods of observation:
This project contains data cleaning methods of removing and replacing null data and columns, including handle "unknown" values that are difficult to classify and work with. We compared four different models (KNN, Decision Tree Classifier, SVN, and Logistic Regression) to predict the output and compare to the baseline accuracy. We also used hyperparameter tuning and feature importance to optimize the models even further and improve the accuracy. 

### Findings:
## Baseline Models:
Running a basic pipeline for all of the models described, We can see that all of the training scores have beat the baseline prediction of 0.869. The test scores of the logistic regression and SVN models are identical to the baseline prediction, with the KNN and decision Tree Classifier models having a lower test accuracy. We can try to improve this further with feature importance and hyperparameter tuning. 

In terms of fit time, the KNN model fit the training data the fastest, while SVN took the longest amount of time. The recommended model for these initial findings is logistic regression, due to the low training time, and highest test score. 

## With Grid Search Optimized:
Using Grid Search to optimize hyperparameters, we have found that all models perform relatively similarly with training and test score accuracy. The test accuracy of all of the models is slightly lower than the baseline prediction at 0.869, while the training accuracy is slightly higher at greater than 0.87. Logistic Regression and SVC still appear to have identical training and test scores. 

KNN appears to have the highest training accuracy, while both logistic regression and SVC models have the higher test accuracies. 

## Identifying the most influential features: 
We can see that all of our models beat the baseline prediction of 0.869 by a minimum of 0.023 for the test scores. KNN once again appears to have the highest train score, with decision tree classifier containing the highest test accuracy. Interestingly, the training time for SVC is also significantly higher with the most important features, compared to only the bank feature parameters. 

Finding and selecting important features enabled us to beat the baseline accuracy and develop robust models. We recommend using the decision tree classifier for the fastest training time, and the highest test score for this particular feature set. 
