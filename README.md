# Capstone Project: Predicting Customer Churn on Sparkify

# Installations

The following packages (i.e., libraries) are necessary to successfully run this project on your local machine:

1. python >=3.6
2. numpy >= 1.19.2
3. pandas >= 1.0.1
4. PySpark >= 2.4
5. matplotlib >= 3.0


# Motivation


The main goal of this project is to create a machine learning model to predict which customer will (possibly) churn at a given time. 
If the machine learning model is capable of predicting with high reliability which customer is likely to churn, the same model applied over millions of customers should be able to save millions of dollars for (the fictitious) Sparkify by contacting these customers and offering them a discount, potentially avoiding the predicted churns to take place. 
Exploratory data analysis, feature engineering and machine learning modeling will come in handy to find a good approach to solve this problem in PySpark.

# Summary of the Results and Blog

A detailed discussion of the results presented here is shown in this [medium post](https://vagnerzeizer.medium.com/sparkify-using-pyspark-to-predict-customer-churn-10060cff9d71).

The best model, the Random Forest, presents a quite good result on the training data (0.98796) and test data(0.98829), with the best number of trees equals 50 and maximum depth equals 15. 
More trees or a larger maximum depth do not make the algorithm perform better. 
These values are quite good for a Random Forest classifier and train relatively faster. 
Cross validations with K=2 or K=3 were run and similar results were found. 
Additionally, the top 3 features of this model make very sense to be responsible for customer churn, as previously discussed. 
Moreover, Random Forest is suitable for large datasets.

Random Forest is my current choice as to be the best machine learning model for this problem because of its easy understanding due to its nature on decision trees and relatively fast training speed. 
Although more complex than decision trees, Random Forest is not prone to overfit in the test data. 
Moreover, the power and scalability of Random Forest for massive data makes it proper to run it in clusters such as Amazon Web Services, or IBM Cloud.


# Main Conclusions

The EDA results have pointed out that a small fraction of the customers churn and more females churn than males. 
Locations, itemInSessions, userAgent were investigated and customer churn can be minimized by properly handling these features.
The current machine learning model results have shown that one can consider Random Forest as the most appropriate one for this problem. 
This model has a great f1-score on the test data, therefore it probably would save money millions of dollars for Sparkify when applied over millions of users when trying to minimize customer churn. 
The most predictive columns of this model are 'userAgent', 'itemInSession', and 'ts' (time). 
This is quite interesting since the two first features were explored are very related to churn.
So, working on these features is really important and deserves strong attention from the (fictitious) enterprise Sparkify.


# Files Description:

1. Sparkify.ipynb: the full code of the PySpark analysis, containing the data cleaning, EDA and machine learning;
2. Sparkify_projectv1.ipynb: the pdf version of the full code.



# How to interact to interact with your project

Just download (or git-clone) this project and use it with anaconda :)
Constructive criticism is welcome :)

# Licensing

## MIT License

Copyright (c) 2021 Vagner Zeizer C. Paes

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


# Acknowledgements

Udacity and the reviewers are strongly acknowledged for this great experience of working on a real-world problem in PySpark.


# Author

1. Vagner Zeizer Carvalho Paes

This project is the Capstone (final) project of the Data Scientist Nanodegree of Udacity.


