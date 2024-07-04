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

# List all install python packages
pip list  # you can see mlflow and othe ml related packages

# Explore mlflow
mlflow
mlflow ui --backend-store-uri sqlite:///mlflow.db
mlflow ui --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./mlruns
```

![image](https://github.com/rajpgr8/mlops-demo/assets/23621486/360a35b9-5a7f-4681-9b25-d1438506d9b0)   

![image](https://github.com/rajpgr8/mlops-demo/assets/23621486/12aebdd5-14d0-4236-933a-868ae315e234)   



![image](https://github.com/rajpgr8/mlops-demo/assets/23621486/c14d3a09-0ac1-4160-b2a1-d43d60053d5e)



