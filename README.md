Table of Contents

Overview

Structure of the project

Building blocks

Installation

Results

License


OVERVIEW:
This project is an end-to-end data science solution for predicting student performance indicators. Leveraging machine learning techniques, the model aims to provide insights into factors influencing student success, aiding educators and administrators in making informed decisions.


STRUCTURE OF THE PROJECT:
1. setup.py, requirements.txt are key components that build the package and install all required libraries.(install requirements.txt to build package first)
2. The folder 'src' or source holds the following files:
    a. utils.py : a kind of utility belt, that holds functions that have been called in future pipelines.
    b. logger.py : a py script that inserts logs at every necessary checkpoint in the runtime of the application. Increasing the reliability of the code. Decreasing time spent on debugging.
    c. exception.py : py script to create Custom Exceptions and decreasing time spent on debugging.
    d. Folder 'components' : The backbone of this full stack data science project:
        d1. data_ingestion.py : This py script is responsible for the streamlined ingestion of data from data source which is artifacts/data.csv.
        d2. data_transformation.py : py script responsible for transforming data by imputing, one-hot encoding, scaling, etc.
        d3. model_trainer.py : py script responsible for training the model by first selecting the best performing model and then training it. returns the trained model as a pickle file 'model.pkl'. Also responsible for GridSearchCV on popular regressor models. extensive hyperparameter tuning also performed here.
    e. Folder 'pipeline' :
        e1. predict_pipeline.py : This py script takes the saved model in the pickle format as an input and preprocessor in the pickle format as an input and predicts the math score of a child depending on his/her other parameters. It is also responsible for creating a streamlined pipeline between the hosted application and local runtime.



BUILDING BLOCKS:
Data Preprocessing: Clean and preprocess raw student data to make it suitable for analysis.
Exploratory Data Analysis (EDA): Perform in-depth EDA to understand patterns and trends in student performance data.
Feature Engineering: Create relevant features to enhance model performance.
Machine Learning Model: Implement a predictive model using state-of-the-art algorithms.
Evaluation Metrics: Utilize appropriate metrics to assess the model's performance.
Deployment: Deploy the model for real-world use, making predictions accessible to end-users.


INSTALLATION:
1. Feel free to clone the repository :

- git clone https://github.com/angryprincess/End2End-Student-Performance-Prediction.git
- cd End2End-Student-Performance-Prediction

2. Install the required dependencies:

- pip install -r requirements.txt

RESULTS:
The highest performing model has been Linear Regression. With an r2_score of 88.0956

LICENSE:
TBD.
