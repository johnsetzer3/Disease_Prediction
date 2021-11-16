# Data Analysis Final Project: Disease Prediction

## Code Blue Team Members
* Frank Sullivan
* Jade Bible
* John Setzer
* Morgan Behr 
* Summer Bell


### Roles for project:
Our team will transition roles during the different segments of the project. We have five group members so we will have multiple people within one role.

Square: The square role focuses on the machine learning model. 
John completed the data exploration and analysis. 

Triangle: The member in the triangle role will upscale the project's database. 
Our datasets are uploaded into PgAdmin.
The static database will be used throughout the project and maintained by Morgan. 

Circle: The members in the circle role will continue to refine the project analysis and support the presentation with data visualizations.
Summer and Frank are providing descriptive analysis of the project and the project progress.
MatplotLib is utilized for additional data visualizations.

X: The member in the X role work on the team's dashboard
Jade is creating our storyboard in Tableau.
This dashboard will clearly represent our data with support of 3 images.

## Topic Selected: Disease Prediction using Machine Learning 
This topic uses data that has 132 parameters to help predict 42 different types of diseases. 

## Reason Why the Topic Was Selected: 
Disease impacts all people throughout the world.
Developing a model where select symptoms can be input to make disease predictions can help make diagnosing diseases faster.

## Questions We Hope to Answer with the Data:
 * Can our machine learning model be used to predict the correct disease based on symptoms entered?
 * How many symptoms need to be present to increase the accuracy of the model?


## Description of the Source of Data: 
The data we used is two csv file downloaded from Kaggle. 
The dataset provided is in a testing and training file.
The training file is [Training.csv](Resources/Training.csv) and the testing file is [Testing.csv](Resources/Testing.csv).
The source of the data from the author is not disclosed.

## Description of the Data Exploration Phase of the Project:
The training file [Training.csv](Resources/Training.csv) and the testing file [Testing.csv](Resources/Testing.csv) where imported into Juypter Notebook.
To begin the preprocessing the two CSV datasets were assigned to the variables: train_data and test_data.  
The data preprocessing was completed in [Disease_Prediction_preprocessing.ipynb](Disease_Prediction_preprocessing.ipynb).
A key part of the data exploration phase is preprocessing the data.
This allows us to learn about the data characteristics and identify potential problems.
We used the pandas info and describe functions to explore the data
For the model to function correctly all data in both data sets has to be in the correct data type.
We also needed to isolate columns with null data and drop that data.
The isnull with any functions identified the null values then the drop function was used to remove it from the dataframe.


## Database
The preprocessed train_data, test_data and sympt_df data sets were exported into PostgresSQL as three separate tables.
This created a static database in pgAdmin for use during the project.
The pdf file [ERD_Disease_Prediction.pdf](./Resources/SQL/ERD_Disease_Prediction.pdf) shows a detailed ERD that displays the relationships.
A join was performed on the tables.
The database interfaces with [Disease_Prediction_ML.ipynb](Disease_Prediction_ML.ipynb).
Using 'from sqlalchemy import create_engine' the PostgresSQL data is used in our machine learning model.


## Machine Learning Model
The model starts by pulling the training and testing tables from PostgresSQL
A list of symptoms and diseases was created to allow for a GUI where symptoms could be selected from a drop down box.
Decision Tree, Random Forest, Naive Bayes and logistic regression models are applied to the symptom selections.
Each model used utilizes the same logic but passes it through a different algorithm.
Each function starts by importing the necessary dependencies and fitting the model to the trained data.
Each function gathers a list of user imported symptoms and iterates through the data, if that symptom is marked as a 1 in the data set (meaning the symptom is present),
then it stores the symptom as present and continues through the list of user selected values.
An inputtest variable is created to test for the symptom's presence in a disease and designates a disease based on the symptoms.
The inputtest variable is run through an accuracy score test to validate the accuracy of the prediction based on the training data and number of symptoms present.
The predicted disease populates into the corresponding field in the GUI and prints the accuracy score to the Jupyter notebook.
This allows us to analyze which model is most accurate as well as how the number of symptoms entered impacts the models accuracy.


## Description of the Analysis Phase of the Project:
Three test patients were run through the model.
This allowed us to compare the accuracy and results of the different machine learning models.
We used the first test patient and used the exact symptoms presented in the training data to determine if the model worked.
We then added miscellaneous, but related symptoms to test the outcome.


## Dashboard
We have a fully functioning and interactive dashboard in Tableau.
Our analysis will be displayed with a story board that provides a clear data visualization.
There are 3 charts that show insightful relationships in our data.
The first chart displays that a balanced dataset was utilized.
The other two charts both display the diseases and symptoms. 
Our interactive chart allows us to select a symptom and easily see based off color how many diseases have it.

[Link to Tableau Dashboard](https://public.tableau.com/app/profile/jade3140/viz/DiseasePredictionProject/DiseasePredictionData?publish=yes)


 





