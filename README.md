# FakeNews
Fake vs Real News Binary Classification

**Contents of this Repository**
Data Wrangling - Removal of duplicates/non-English language articles
Data Preprocessing - TF-IDF Vectorization, Lemmatization
Exploratory Data Analysis, fake news has a higher variability on readability scores
Modeling- ~90% accuracy

(The most interesting part of this project: in my opinion. 
This was (as far as I know) a novel and successful use of readability scores as a feature for classifying fake news. 

Just a note: This repository is a portfolio display and as such I currently upload the documents directly). 
Version controlled notebooks/documentation are found in the Springboard repository

The removal of duplicates was a difficult task for this project. The computing resources necessary were quite intensive to even do vectorized
fuzzy matching. Thus, I came up with a method using the python library textstat (which would ultimately produce features as well). This method was not perfect, but 
was computer efficient. Though I did not do it in this ideally any match this method caught or at least some subset should be checked via fuzzy matching. 

Data preprocessing was basic for a NLP project. TF-IDF Vectorization, tokenization, and lemmatization. 

EDA - The most interesting finding out of EDA was that readability scores have a much higher variability or range of scores compared with real news. I take this to indicate
more adherence to institutional style guides by major legitimate news outlets compared to fake news outlets. 

Modelling - No baseline was used as there wasn't much one could do naively except a no skill assumption (random guessing)
Logistic Regression, Random Forest Classifier, and Support Vector Machine were compared

Random Forest Classifier was a narrow winner over Logistic Regression on all relevant measures, but paricularly the ROC score. A voting classifier was used for all three models,
this was not as good as Random Forest or Logistic Regression. 

Overall the accuracy of the final model was ~90%. And textstat readability features competed with the TF-IDF vectors for best model features
