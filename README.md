# Forecasting Ozone Days
Collaborators: Richard Huang, Ruofan Wu, Shamil Saeed¶

## Understand
Here we present the problem in which we wish to explore in this notebook, in that we wish to be able to forecast days in which Ozone levels are high. In this notebook, we will be looking at the 8hr peak dataset whose data was collected from 1998 to 2004 at the Houston, Galveston and Brazoria area.

## Load
The data is loaded from OpenML
https://www.openml.org/data/v1/download/1592279/ozone-level-8hr

## Explore
There is a scatter_matrix and correlation heatmap of the features. 

## Scrubbing
There were no missing values, we double checked. It seems that the missing values in the original dataset from where this is based off of was acquired and filled. 

## Modeling
We built the following models:

- LogisticRegression
- GaussianNB
- KNeighborsClassifier
- DecisionTreeClassifier
- import RandomForestClassifier
- SVC
- SGDClassifier
- VotingClassifier

The Voting Classifier is a ensemble of the previous ones mentioned.

We also created a Neural Network and compared the results to the other classifiers.
We focused on Precision and Recall scores for assessing which classifier is better. Since this concerns the health of living creatures, we priortorized Recall score over Precision score.

## Predict
We chose to use the Neural Network and ran it on the test set

## Launch
Outputed the weights of the Neural Network
