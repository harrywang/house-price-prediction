# About

Most of the code in this notebook is from https://github.com/ageron/handson-ml. This is a great book - please buy the book to support the author.

This notebook can serve as a good training tutorial for novice data scientists.

The 10-Step Machine Learning Project Workflow (My Version):

1. Define business object
2. Make sense of the data from a high level
    - data types (number, text, object, etc.)
    - continuous/discrete
    - basic stats (min, max, std, median, etc.) using boxplot
    - frequency via histogram
    - scales and distributions of different features
3. Create the traning and test sets using proper sampling methods, e.g., random vs. stratified
4. Correlation analysis (pair-wise and attribute combinations)
5. Data cleaning (missing data, outliers, data errors)
6. Data transformation via pipelines (categorical text to number using one hot encoding, feature scaling via normalization/standardization, feature combinations)
7. Train and cross validate different models and select the most promising one (Linear Regression, Decision Tree, and Random Forest were tried in this tutorial)
8. Fine tune the model using trying different combinations of hyperparameters
9. Evaluate the model with best estimators in the test set
10. Launch, monitor, and refresh the model and system

## Google Colab Notebook

You can run this kernel directly at Google Colab: https://colab.research.google.com/drive/1EDf2Fl507G_auObEhQsvpn1c6L0yMNML

## Kaggle Kernel

You can run this kernel directly at Kaggle.com: https://www.kaggle.com/harrywang/housing-price-prediction

## Local Setup

Tested with Python 3.6 via virtual environment. Clone the repo, go to the repo folder, setup the virtual environment, and install the required packages:


```shell
$ python3.6 -m venv venv
$ source venv/bin/activate
$ pip install -r requirements.txt
```

Run `$ jupyter notebook` to go over the tutorial step-by-step.


## Data

The data is based on California Census in 1990.

The following are the descriptions from the book author:

"This dataset is a modified version of the California Housing dataset available from Luís Torgo's page (University of Porto). Luís Torgo obtained it from the StatLib repository (which is closed now). The dataset may also be downloaded from StatLib mirrors.
...

This dataset appeared in a 1997 paper titled Sparse Spatial Autoregressions by Pace, R. Kelley and Ronald Barry, published in the Statistics and Probability Letters journal. They built it using the 1990 California census data. It contains one row per census block group. A block group is the smallest geographical unit for which the U.S. Census Bureau publishes sample data (a block group typically has a population of 600 to 3,000 people).
...

The dataset in this directory is almost identical to the original, with two differences:
207 values were randomly removed from the total_bedrooms column, so we can discuss what to do with missing data.
An additional categorical attribute called ocean_proximity was added, indicating (very roughly) whether each block group is near the ocean, near the Bay area, inland or on an island. This allows discussing what to do with categorical data.
Note that the block groups are called "districts" in the Jupyter notebooks, simply because in some contexts the name "block group" was confusing."

[Additional data description from Luís Torgo](http://www.dcc.fc.up.pt/%7Eltorgo/Regression/cal_housing.html):

"We collected information on the variables using all the block groups in California from the 1990 Cens us. In this sample a block group on average includes 1425.5 individuals living in a geographically co mpact area. Naturally, the geographical area included varies inversely with the population density. W e computed distances among the centroids of each block group as measured in latitude and longitude. W e excluded all the block groups reporting zero entries for the independent and dependent variables. T he final data contained 20,640 observations on 9 variables. The dependent variable is ln(median house value)."
