# mlops-demo with python

### commands
```
# Insatll Anaconda3
wget https://repo.anaconda.com/archive/Anaconda3-2022.05-Linux-x86_64.sh
bash Anaconda3-2022.05-Linux-x86_64.sh
```
### Commands to run mlflow
```
cd 02-experiment-tracking && \
conda activate exp-tracking-env && \
pip install -r requirements.txt && \
mlflow ui --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./mlruns
```
### Commands to run jupyter notebook
```
jupyter notebook
```
### Other commands
```
# Create and activate env
conda create -n exp-tracking-env
conda activate exp-tracking-env

# List all installed python packages
pip list  # you can see mlflow and othe ml related packages

# mlflow comands
mlflow
mlflow ui --backend-store-uri sqlite:///mlflow.db
mlflow ui --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./mlruns
```
### Screenshot of jupyter notebook

![image](https://github.com/rajpgr8/mlops-demo/assets/23621486/360a35b9-5a7f-4681-9b25-d1438506d9b0)   

### Screenshot of mlflow UI
![image](https://github.com/rajpgr8/mlops-demo/assets/23621486/11e08d95-ee56-4cc3-886c-df776690a5e3)


![image](https://github.com/rajpgr8/mlops-demo/assets/23621486/c14d3a09-0ac1-4160-b2a1-d43d60053d5e)



