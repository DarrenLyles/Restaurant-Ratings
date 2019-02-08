# Restaurant-Ratings

This project takes a dataset, which is comprised of reviews and ratings for San Francisco
restaurants. The objective is to predict (or classify) restaurant reviews
by rating, which ranges from 1- to 5-stars. This is a supervised learning problem and 
incorporates fundamental natural language processing techniques, which will be explained further.

### Dataset_and_Wrangling.ipynb

This notebook goes through the data wrangling process in which we convert the raw JSON dataset into
a CSV file. 

### EDA_Stage.ipynb

We explore the dataset in this notebook, but before doing so, we also added another column, which contains the 
tokenized version of the review text. This required the use of natural language processing fundamentals,
such as removing stop words and punctuation, and lemmatizing the words to reduce variants of the same
root and meaning.

### The following notebooks contain tests for their respective machine learning models. 
<ul>
  <li>SVC_Model.ipynb</li>
  <li>NaiveBayes_Model.ipynb</li>
  <li>RandomForest_Model.ipynb</li>
  <li>XGBoost_Model.ipynb</li>
 </ul>

Each notebook compares the performance for their respective models under the following parameters: <br/>
<ul>
  <li>CountVectorizer</li>
  <li>TfIdfVectorizer</li>
  <li>n-gram features</li>
</ul>

The CountVectorizer uses the bag of words concept and is applied to the tokenized review text, whereas
the TfIdfVectorizer is applied to the raw review text. With the exeption of XGBoost_Model.ipynb, the
models were evalued with using 1-gram, 2-gram, 3-gram, 4-gram, and 5-gram.  The XGBoost classifier
was reduced to being evaulated with 1-gram and 2-gram due to runtime constraints.
