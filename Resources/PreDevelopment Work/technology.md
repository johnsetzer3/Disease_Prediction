# Technologies Used for Disease Prediction Project

## Presentation

A PowerPoint presentation will be used.
The presentation will provide an outline of our Disease Prediction Project.



## Database 

Our dataset was already split into training and testing files.
The training file is [Training.csv](Resources/Training.csv) and the testing file is [Testing.csv](Resources/Testing.csv) these data sets are uploaded into PgAdmin as tables.
With PostgreSQL a join was performed on the tables.
Using sqlalchemy as a connection we will import the static database into Juypter Notebook and perform machine learning with Python coding.
There is a detailed ERD the displays the database relationships.

## Machine Learning

##Data Cleaning and Analysis
In Python the Pandas library was used to clean the data and perform an exploratory analysis. 
A key part of the data exploration phase is preprocessing the data.
This allows us to learn about the data characteristics and identify potential problems.
The connection to SQL allows for current data from the data tables within PostgreSQL.

Machine learning utilizes both training and testing data.
Both the training and testing datasets are split into attributes and labels with Python to allow for the machine learning model to be applied.
A list of symptoms and disease was created to allow for a GUI where symptoms could be selected from a drop down box.
Decision Tree, Random Forest, Naive Bayes and logistic regression models are applied to the symptom selections.
These models assign variables to give disease predictions.
Along with the disease prediction the model shows the different accruacy scores.
This allows us to analyze which model is most accruate as well as how the number of symptoms entered impacts the models accuracy. 


This binary data is optimal for a logistical regression model because the prediction is categorical.
A machine learning logistical regression algorithm can be used to predict the outcome of dependent variables based on previous training data. 
One assumption of successful logistical regression analysis is that there is little to no multicollinearity which is an occurrence of high intercorrelations among two or more independent variables. 



## Dashboard

We will create a fully functioning and interactive dashboard in Tableau.
Our analysis will be displayed with a story board that provides a clear data visualization.
There will be charts and graphs that show insightful relationships in our data.