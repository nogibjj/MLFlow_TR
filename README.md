# IDS706_Week12_MLFlow
[![CI](https://github.com/nogibjj/MLFlow_TR/actions/workflows/cicd.yml/badge.svg)](https://github.com/nogibjj/MLFlow_TR/actions/workflows/cicd.yml)

Tianji Rao

## Overview
In this project, we build a Logistics regression model to run classification on the Irish dataset. Here we also use the MLFlow to manage the project, including tracking metrics.

## Preparation 
- git clone this repo to local
- install necessary packages
- run `python main.py`
- view and load ML models saved in `mlruns`

## MLFlow 
In this project, the MLflow library is used to manage the machine learning experiment and log various aspects of the experiment. The experiment involves training a simple logistic regression model on the Iris dataset. Here's a summary of the MLflow usage in this code:

Tracking Experiment Runs: MLflow is used to start and log information about the experiment run. mlflow.start_run() initiates a new run, and within this context, hyperparameters (mlflow.log_params), a metric (mlflow.log_metric for accuracy), and a tag (mlflow.set_tag) are logged. This information helps in tracking and comparing different runs.

Model Logging: The trained logistic regression model is logged using mlflow.sklearn.log_model. This logs the model artifact and its associated metadata. The model is logged with a specified artifact path ("iris_model"), and the signature of the model is inferred using infer_signature. The registered model name is set as "tracking-quickstart".

Loading the Model: After the run is completed, the code demonstrates how to load the logged model using mlflow.pyfunc.load_model. This allows for the retrieval and use of the trained model for making predictions without having to retrain it.

Overall, MLflow is employed to organize and track the machine learning experiment, making it easy to reproduce, compare, and deploy models. The logging of hyperparameters, metrics, and models provides a comprehensive record of the experiment, facilitating collaboration and model management.

## Make actions 
1. Format `make format`
2. Lint `make lint`
3. Test `make test`
