# mlflow_tutorial


## For Dagshub:

MLFLOW_TRACKING_URI=https://dagshub.com/nerdjumbo/mlflow_tutorial.mlflow \
MLFLOW_TRACKING_USERNAME=nerdjumbo \
MLFLOW_TRACKING_PASSWORD=c9af63b2d61172ad9a42cdd1b0ab5ea29da26b4b \
python script.py


```bash

export MLFLOW_TRACKING_URI=https://dagshub.com/entbappy/MLflow-Basic-Demo.mlflow

export MLFLOW_TRACKING_USERNAME=entbappy 

export MLFLOW_TRACKING_PASSWORD=6824692c47a369aa6f9eac5b10041d5c8edbcef0


```


# MLflow on AWS

## MLflow on AWS Setup:

1. Login to AWS console.
2. Create IAM user with AdministratorAccess
3. Export the credentials in your AWS CLI by running "aws configure"
Also install aws cli in your local machine
4. Create a s3 bucket
5. Create EC2 machine (Ubuntu) & add Security groups 5000 port

Run the following command on EC2 machine
```bash
sudo apt update

sudo apt install python3-pip

sudo pip3 install pipenv


sudo pip3 install virtualenv && mkdir mlflow && cd mlflow && pipenv install mlflow && pipenv install awscli && pipenv install boto3 && pipenv shell


## Then set aws credentials
aws configure


#Finally 
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-nerdjumbo

#open Public IPv4 DNS to the port 5000


#set uri in your local terminal and in your code 
export MLFLOW_TRACKING_URI=http://ec2-23-22-237-173.compute-1.amazonaws.com:5000/
```

