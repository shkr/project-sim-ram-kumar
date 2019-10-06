# Classify Wikipedia Disease Articles

There are lots of different kinds of articles, and one flavor is those that describe a disease. The data are html dumps of wikipedia articles. We give you a labelled set of disease articles (positives), and non-diseases articles (negatives).


## Part 1

Classifying whether article is about disease or not, It is a binary classification problem. 


## Tasks

* Extracting text out of html dump
* Cleaning the dataset
* EDA for understanding dataset
* Model Selection


### Extracting text out of html dump

[link to notebook](https://github.com/shkr/project-sim-ram-kumar/blob/master/HTML_to_csv.ipynb)

I have used `beautifulsoup` libray to parse html document and extract text from `<title></title>` and all `<p></p>` tags. And Created few csv files 

**Columns** `article, y`

* positive-combined.csv (A CSV of all postive samples)
* negative-combined.csv (A CSV of all negative samples)


### Cleaning the dataset

[link to notebook](https://github.com/shkr/project-sim-ram-kumar/blob/master/Data%20Cleaning.ipynb)

For cleaning text data, I have followed some typical cleaning process as follows: 

* Lower casing
* Removal of Punctuations
* Removal of Stopwords
* Stemming

And merged the postive and negative csv into single csv `dataset.csv` for model selection and EDA


### EDA for understanding dataset

[link to notebook](https://github.com/shkr/project-sim-ram-kumar/blob/master/EDA.ipynb)

* I have looked at the word count statistics, And identified at no of words per article 90th percentile is less the 1000 words.

* created a word cloud for negative and positive samples



###  Model Selection

[link to notebook](https://github.com/shkr/project-sim-ram-kumar/blob/master/Model_Selection_V1.ipynb)

**Initial Idea** I have decided to go with CNN with 1-D convolution model. Based on my previous experience in working with text data.

* Tokenized the words
* Padded the sequence to max length of 1000  since 90th percentile word count is less than 1000
* Used Deep Conv 1D with trainable embeddings layer

#### Model Metrics

**Confusion Matrix**

| Negative | Positive |
| ------ | ------ |
| 991 | 9 |
| 4 | 366 | 

**Test Accuracy** 

`99%`

**Test F1 Score** : `0.9825503355704698`

**Evauation Metrics**

              precision    recall  f1-score   support

           0       1.00      0.99      0.99      1000
           1       0.98      0.99      0.98       370

    accuracy        -        -         0.99      1370
   

* I have tried `class_weights` it also yields similar F1-score



