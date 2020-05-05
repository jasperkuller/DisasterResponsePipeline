# Disaster Response Pipeline Project

## Description
This project is part of an assignment for the Udacity Data Scientist nanodegree course. In it, students are required to build an ML pipeline for processing and classifying messages, to enable quick response in a disaster situation. The data consists of real-life tweets that are pre-labelled with categories like 'earthquake', 'food' and 'medical_help'. 

The project follows this sequence:
1. ETL pipeline
	- Loads and merges data
	- Cleans the data
	- Stores it in a SQLite database
2. ML pipeline
	- Loads data from the SQLite database
	- Splits the dataset into training and test sets
	- Builds a text processing and machine learning pipeline
	- Exports the model as a pickle file
3. Web deployment
	- Created backend using `Flask` and `Plotly`
	- Deployed with `Heroku`

## Getting started 
Cloning the GIT repository to your local machine can be done using 
`git clone https://github.com/jasperkuller/DisasterResponsePipeline.git`

All necesary libraries are imported, the code should run with no issues using Python versions 3.*. 

The jupyter notebooks containing the ETL and ML pipelines are included in the project folder for further experimenting. These also include the process leading to the configuration of the final ML model.  

### To run the app: 
1. Run the following commands in the project's root directory to set up your database and model.
    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/

## Author
[Jasper Küller](https://github.com/jasperkuller)

## License
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Acknowledgements
[Figure Eight](https://www.figure-eight.com/) provided the datasets for this assignment.

