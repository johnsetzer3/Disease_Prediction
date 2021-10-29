# Technologies Used for Disease Prediction Project

## Presentation

A Google slide presentation will be used.
That presentation will provide an outline of our Disease Prediction Project.


## Database 

The training file is [Training.csv](Resources/Training.csv) and the testing file is [Testing.csv](Resources/Testing.csv) these data sets are uploaded into PgAdmin as tables.
With PostgreSQL a join was performed on the tables.
Using sqlalchemy as a connection we will import the static database into Juypter Notebook and perform machine learning with Python coding.
There is a detailed ERD the displays the database relationships.

## Machine Learning

##Data Cleaning and Analysis
In Python the Pandas library will be used to clean the data and perform an exploratory analysis. 
A key part of the data exploration phase is preprocessing the data.
This allows us to learn about the data characteristics and identify potential problems.
Machine learning utilizes both training and testing data.
Our dataset was already split into training and testing files.
Both the training and testing datasets are split into attributes and labels with Python to allow for the machine learning model to be applied.
This binary data is optimal for a logistical regression model because the prediction is categorical.
A machine learning logistical regression algorithm can be used to predict the outcome of dependent variables based on previous training data. 
One assumption of successful logistical regression analysis is that there is little to no multicollinearity which is an occurrence of high intercorrelations among two or more independent variables. 

Will we need this because we have two datasets already split - Using the train_test_split model to generate the datasets.
Are we using - SciKitLearn is the ML library we'll be using to create a classifier. 
Only if we have time - We will also incorporate Random Forest to make predictions using our testing data.  

## Dashboard

We will create a fully functioning and interactive dashboard in Tableau.
Our analysis will be displayed with a story board that provides a clear data visualization.
There will be charts and graphs that show insightful relationships in our data.