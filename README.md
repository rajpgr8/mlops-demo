## mlops-demo with python, just for learning   
( Ref: https://github.com/DataTalksClub/mlops-zoomcamp )

### commands
```
# Start with creating virtual env
python3 -m venv .venv
source .venv/bin/activate

# Inside virtual env, run these
pip install -r requirements.txt
python3 -m ipykernel install --user --name={PROJECT_NAME}
jupyter notebook


=> For example, run these commands 
python3 -m venv .venv && source .venv/bin/activate
pip install -r mlops-demo/01-intro/requirements.txt
python3 -m ipykernel install --user --name=mlops
code mlops-demo/01-intro
    => Then Select kernel in VSCODE like .venv(Python 3.8.20), and run notebook locally.
    => OR run 'jupyter notebook' to open Juyper notebook in the browser
```

### Other commands
```
# Insatll Anaconda3 (Optional)
wget https://repo.anaconda.com/archive/Anaconda3-2022.05-Linux-x86_64.sh
bash Anaconda3-2022.05-Linux-x86_64.sh

# Create and activate env
conda create -n exp-tracking-env
conda activate exp-tracking-env

# List all installed python packages
pip list  # you can see mlflow and othe ml related packages

# Commands to run mlflow
cd 02-experiment-tracking && \
conda activate exp-tracking-env && \
pip install -r requirements.txt && \
mlflow ui --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./mlruns

# mlflow comands
mlflow
mlflow ui --backend-store-uri sqlite:///mlflow.db
mlflow ui --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./mlruns
```
```
#  Example of mlflow code, how to use log_param/log_param/log_metric/log_artifact
with mlflow.start_run():

    mlflow.set_tag("developer", "rp")

    mlflow.log_param("train-data-path", "../data/yellow_tripdata_2021-01.parquet")
    mlflow.log_param("valid-data-path", "../data/yellow_tripdata_2021-02.parquet")

    alpha = 0.12
    mlflow.log_param("alpha", alpha)
    lr = Lasso(alpha)
    lr.fit(X_train, y_train)

    y_pred = lr.predict(X_val)
    rmse = mean_squared_error(y_val, y_pred, squared=False)
    mlflow.log_metric("rmse", rmse)

    mlflow.log_artifact(local_path="models/lin_reg.bin", artifact_path="models_pickle")  # Save model from local path to artifact 
```

#  Other Example code:
```
df = pd.read_parquet("../data/fhv_tripdata_2021-01.parquet")
OR
df = pd.read_parquet("https://d37ci6vzurychx.cloudfront.net/trip-data/fhv_tripdata_2021-01.parquet")
```

![image](https://github.com/rajpgr8/mlops-demo/assets/23621486/969eb493-d02e-4629-bfa5-9cf8baeb55a2)

### Screenshot of jupyter notebook

![image](https://github.com/rajpgr8/mlops-demo/assets/23621486/360a35b9-5a7f-4681-9b25-d1438506d9b0)   

### Screenshot of mlflow UI
![image](https://github.com/rajpgr8/mlops-demo/assets/23621486/11e08d95-ee56-4cc3-886c-df776690a5e3)


![image](https://github.com/rajpgr8/mlops-demo/assets/23621486/c14d3a09-0ac1-4160-b2a1-d43d60053d5e)

### model file and local mlflow artifact
![image](https://github.com/rajpgr8/mlops-demo/assets/23621486/a9e12cb3-4883-4770-81ea-9ef951db9be6)

![image](https://github.com/rajpgr8/mlops-demo/assets/23621486/02272e40-a7a5-4f56-92e2-a9c41e0eb3d1)



