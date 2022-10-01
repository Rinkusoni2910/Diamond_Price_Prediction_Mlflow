# Diamond_Price_Prediction_Mlflow
# Introduction to Experiment Tracking
# Terminologies:

1. Experiment
2. Run
3. Metadata (i.e. Tags, Parameters, Metrics)
4. Artifacts (i.e. Output files associated with experiment runs)

# What do you want to track for each Experiment Run?
1. Training and Validation Data Used
2. Hyperparameters
3. Metrics
4. Models

# Why Track?
Organization Optimization Reproducibility

# Tool - MLFlow
MLFlow helps you to organize your experiments into runs.

#MLFlow keeps track of:
- Tags
- Parameters
- Metrics
- Models
- Artifact
- Source code, Start and End Time, Authors etc..

# Run below mentioned commands to install mlflow on your system:

- pip install mlflow
- mlflow ui --backend-store-uri sqlite:///mlflow.db

# Introduction to MLFlow
# Step 1 - Import MLFlow

import mlflow

# Step 2 - Set the tracker and experiment

- mlflow.set_tracking_uri(DATABASE_URI)
- mlflow.set_experiment("EXPERIMENT_NAME")

# Step 3 - Start a experiment run

with mlflow.start_run():

# Step 4 - Logging the metadata

- mlflow.set_tag(KEY, VALUE)
- mlflow.log_param(KEY, VALUE) mlflow.log_metric(KEY, VALUE)

# Step 5 - Logging the model and other files (2 ways)

- Way 1 - mlflow.<FRAMEWORK>.log_model(MODEL_OBJECT, artifact_path="PATH")
- Way 2 - mlflow.log_artifact(LOCAL_PATH, artifact_path="PATH")

# Below are screenshots of experiment tracking of diamond price prediction models
![image](https://user-images.githubusercontent.com/65038531/193413610-73fe5599-a4c6-453b-8698-216f096bcf50.png)

![image](https://user-images.githubusercontent.com/65038531/193414436-fe7778f5-dc60-4e66-a36e-a3294ad21a70.png)

![image](https://user-images.githubusercontent.com/65038531/193414587-ebde3926-530a-4416-b4a0-83b4da462331.png)
