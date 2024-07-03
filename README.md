# mlops-demo with python

### commands
```
# Insatll Anaconda3
wget https://repo.anaconda.com/archive/Anaconda3-2022.05-Linux-x86_64.sh
bash Anaconda3-2022.05-Linux-x86_64.sh

# Create and activate env
conda create -n exp-tracking-env
conda activate exp-tracking-env

cd 02-experiment-tracking
pip install -r requirements.txt
pip list  # you can see mlflow and othe ml related packages
```
### mlflow
```
mlflow
mlflow ui --backend-store-uri sqlite:///mlflow.db
mlflow ui --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./mlruns
```
![alt text](image.png)



