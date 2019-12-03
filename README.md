# Forecasting Ozone Days¶
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
We did however convert the DayClass from (1,2) to (0,1) where 0 is Normal Day and 1 is O-Zone Day.
We also applied various dimensional reducing methods such as PCA and LDA.

LDA seemed to be best at seperating O-Zone Days and Normal Days.

Afterwards, we created a training and test dataset.

## Modeling
We built the following models:

from sklearn.linear_model import LogisticRegression
from sklearn.naive_bayes import GaussianNB
from sklearn.neighbors import KNeighborsClassifier
from sklearn.tree import DecisionTreeClassifier
from sklearn.ensemble import RandomForestClassifier
from sklearn.svm import SVC
from sklearn.linear_model import SGDClassifier
from sklearn.ensemble import VotingClassifier

The Voting Classifier is a ensemble of the previous ones mentioned.

We also created a Neural Network and compared the results to the other classifiers.
We focused on Precision and Recall scores for assessing which classifier is better. Since this concerns the health of living creatures, we priortorized Recall score over Precision score.

## Predict
We chose to use the Neural Network and ran it on the test set

## Launch
Outputed the weights of the Neural Network
