# Enron Email Classification
## Problem Statement 
Build a classification model to classify emails into 8 different categories.
## About the Dataset
The [dataset](https://bailando.berkeley.edu/enron_email.html) contains the internal and external email exchanges between employees of Enron. It also contains the labels attached to these emails. The labels cover fields such as Company, Business, Strategy; Purely personal; Logistic Arrangements, and so on. 

## Data Preprocessing
Steps taken for data preprocessing are – 


a)	Extract the email content from each individual email thread. This was done by removing all the other texts from each thread. 


b)	Extract the contents and the labels into a dataframe for further processing. 


c)	Once the dataframe was formed, the email contents were further processed by removing punctuations, and numbers. 


d)	Tf-Idf vectorizer was used for vectorizing the email contents. 


After the pre-processing, we plot a [bar graph](https://github.com/ArohanP/Enron_email_classification/blob/main/Data%20distribution%20and%20Model%20performance/Data_distribution.png)  to get an understanding of the distribution of labels in the data. We see that the data is significantly unbalanced with labels “1” and “4” in high numbers while labels “7” and “8” are quite low in number. 

## Model Development
Four models were trained and tested on the dataset after an 80-20 split of the dataset. These four models were – 

1) Linear Support Vector Machine.

2) Random Forest Classifier.

3) Naïve Bayes Classifier.

4) Logistic Regression. 


## Results and Analysis
Detailed classification reports of the four models were analyzed. Analysis shows that while accuracy, precision, and f1-score had slight variations for each model and each classification category, the overall performance of the models as measured by accuracy score, macro average, and weighted average showed a clear winner, i.e., support vector classifier. 

## Overall performance of each model
1) Classification report of [Linear Support Vector Classifier](https://github.com/ArohanP/Enron_email_classification/blob/main/Data%20distribution%20and%20Model%20performance/Classification_report_SVC.png).

2) Classification report of [Random Forest Classifier](https://github.com/ArohanP/Enron_email_classification/blob/main/Data%20distribution%20and%20Model%20performance/Classification_report_RF.png).

3) Classification report of [Naive Bayes Classifier](https://github.com/ArohanP/Enron_email_classification/blob/main/Data%20distribution%20and%20Model%20performance/Classification_report_NB.png).

4) Classification report of [Logistic Regression Classifier](https://github.com/ArohanP/Enron_email_classification/blob/main/Data%20distribution%20and%20Model%20performance/Classification_report_Logistic_reg.png).

On comparing the above classification reports, we see that although each model has its own high and low performance values with regard to each category, but the overall performance of the model as measured by accuracy, micro average, and weighted average is significantly higher for support vector machine.
