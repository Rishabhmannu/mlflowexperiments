## ML FLow experiements

MLFLOW_TRACKING_URI=https://dagshub.com/krishnaik06/mlflowexperiments.mlflow \
MLFLOW_TRACKING_USERNAME=krishnaik06 \
MLFLOW_TRACKING_PASSWORD=7104284f1bb44ece21e0e2adb4e36a250ae3251f \
python script.py

import dagshub
dagshub.init(repo_owner='Rishabhmannu', repo_name='mlflowexperiments', mlflow=True)

import mlflow
with mlflow.start_run():
  mlflow.log_param('parameter name', 'value')
  mlflow.log_metric('metric name', 1)