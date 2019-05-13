# StockMarket-Prediction

StockMarket prediction is a typical binary-classification problem, it is an open dataset from [Kaggle](https://www.kaggle.com/aaron7sun/stocknews/home), 
which has three raw datasets:

1. **RedditNews.csv**: The first column is the "date", and second column is the "news headlines". News headlines come from 
[Reddit WorldNews Channel](https://www.reddit.com/r/worldnews) (/r/worldnews). They are ranked by reddit users' votes, and only 
the top 25 headlines are considered for a single date. In the csv file all news are ranked from top to bottom based on how 
hot they are. Hence, there are 25 lines for each date.

2. **DJIA_table.csv**: Dow Jones Industrial Average (DJIA), downloaded directly from 
[Yahoo Finance](https://finance.yahoo.com/quote/%5EDJI/history?p=%5EDJI&guccounter=1): check out the web page for more info. 

3. **Combined_News_DJIA.csv**: Combined two above datasets with 27 columns. The first column is "Date", the second is "Label",
and the following ones are news headlines ranging from "Top1" to "Top25".

Time range is from 2008-08-08 to 2016-07-01, for task evaluation, we use data from 2008-08-08 to 2014-12-31 as 
Training Set, and Test Set is then the following two years data (from 2015-01-02 to 2016-07-01). This is roughly a 80%/20% 
split.

Since it's a binary-classification problem, it only has two labels:

* "**1**" when DJIA Adj Close value rose or stayed as the same.
* "**0**" when DJIA Adj Close value decreased.

For reading convenience, I divide the whole project to several parts:
### [PartI](https://github.com/victorchennn/StockMovement-Prediction/blob/master/Part_I.ipynb)
* Phase1: Loading in the Data
* Phase2: EDA
* Phase3: Sentiment Analysis
* Phase4: Text Encoding techniques
* Phase5: Stemming
### [PartII](https://github.com/victorchennn/StockMovement-Prediction/blob/master/Part_II.ipynb)
* Phase1: Empirical Probability
* Phase2: Sigmoid Function
* Phase3: KL Divergence
* Phase4: Cross Entropy Loss
* Phase5: Gradient Descent
* Phase6: SGD and Mini-Batch Gradient Descent
### [PartIII](https://github.com/victorchennn/StockMovement-Prediction/blob/master/Part_III.ipynb)
* Phase1: Basic Classifier
* Phase2: Confusion Matrix
* Phase3: Classification Threshold & F-measure
* Phase4: ROC curve & AUC
### [PartIV](https://github.com/victorchennn/StockMovement-Prediction/blob/master/Part_IV.ipynb)
* Phase1: Naive Bayes
* Phase2: Decision Tree
* Phase3: Random Forest
* Phase4: Gradient Boosting

## Install
Since most of work is done on jupyter, you should install it with `pip`:
```
python3 -m pip install --upgrade pip
python3 -m pip install jupyter
```
**Notice**, Python is a requirement (Python 3.3 or greater, or Python 2.7) for installing the Jupyter Notebook itself, details can 
be found at [HERE](https://jupyter.org/install).
