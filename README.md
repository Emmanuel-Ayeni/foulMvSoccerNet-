# FoulMvSoccerNet- Project


## Introduction
<p>To apply computer vision using video input in Python with the SoccerNet dataset, we can follow the end-to-end machine learning lifecycle. The SoccerNet dataset is a multi-frame dataset that includes video clips of soccer matches, annotated with various events such as fouls, goals, and cards</p>

## Problem Definition
* Objective: Build a computer vision model to detect fouls in soccer matches using video input from the SoccerNet dataset.

* Input: Video frames from the SoccerNet dataset.

* Output: Classification of frames or sequences as containing a foul or not.



## Project Deliverables
My repository/folder contains the following:

### README.md 
* Description of the problem
* Instructions on how to run the project Data

### Notebook (name - notebook.ipynb)
* Data preparation and data cleaning
* EDA
* Feature Importance Analysis
* Model selection process and parameter tuning

### Script train.py (name - App.py)
* Training the final model
* Saving it to a file (e.g. pickle) or saving it with specialized software (BentoML)
  
### Script predict.py (suggested name)
* Loading the model
* Serving it via a web service (with Flask or specialized software - BentoML, KServe, etc)
* Files with dependencies
* Pipenv and Pipenv.lock if you use Pipenv
* or equivalents: conda environment file, requirements.txt or pyproject.pipenv run python -m ipykernel install --user --name=mlzoomcamp-midterm-project

### Dockerfile for running the service
### Deployment
URL to the service you deployed or
Video or image of how you interact with the deployed service

## Set up Environment and Component Testing
### Clone the Application Code
Please ensure you have the application code (including Pipfile, Pipfile.lock, and app.py) in your working directory. If it's in a repository, clone it:


```
$ cd <repository_directory>
```

### Install pipenv

```
$ pip install pipenv
```

### Set Up the Virtual Environment
* Run pipenv install to create a virtual environment and install all dependencies specified in the Pipfile.lock:

```
$ pipenv install
```

### Activate the Virtual Environment for Development Test Functions
* Enter the pipenv shell to work within the virtual environment:

```
 $ pipenv shell
```
### Run the final.py
* Extract the dataset from SoccerNet via API, generate an ?? model and download the attrition model by
  running the final.py script:
* Ensure you set up a SoccerNet API before running the script.

```
$ pipenv run python ?-final.py
```
  
### Interfacing with the Prediction Endpoint
### Run the Flask Application
#### Run Application Service Using Python Script
* Start the Flask application by running the app.py script:

```
$ pipenv run python app.py
```

* This will start the Flask application, and you should see an output similar to:
* Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)

#### Run Application Test from Jupyter Notebook
* Open a new terminal window to interact with the web service.
* Start up a Jupyter notebook.
* Open up the predict_test.ipynb and use the test to run JSON formatted data for the prediction service.

##### Activate the Virtual Environment for Jupyter Notebook
Enter the pipenv shell to work within the virtual environment:

```
 $ pipenv shell
```

```
$ pipenv run python app.py
```

Open the Jupyter Notebook from your browse and double-click on predict_test.ipynb

Run the input data as a test:
```
input_data = {
    ???
}
```

* Step-click through to the last cell in the predict_test.ipynb and see the prediction result.

  
* Prediction result is noted after the last cell.
* Check the Service log message as 200: OK or indicates a successful request.
#### Using Curl ?
#### Using Postman ?

## Deploying with Docker

### Build the Docker image:
```
$ docker build -t ???-predict-app .
```

### Run the container:
```
$ docker run -p 9696:9696 attrition-predict-app
```

### Use the same steps above (curl, Postman, or Python) to interact with the application.


## Cloud Infrastructure Deployment
