End-to-End-Machine-Learning-Project-with-MLFlow


## Workflow
1. Update config.yaml
2. Update schema.yaml
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline
8. Update the main.py
9. Update the app.py



# How to Execute the Project
### STEPS:

Clone the repository

```bash
https://github.com/Shoaib-Alauudin/End-to-End-Machine-Learning-Project-with-MLFlow
```

### Step 1 - Create a conda environment after clone the repository


```bash
conda create -n ml_project_env python=3.8 -y
```

```bash
conda activate ml_project_env
```


### STEP 2 - Install the Requirements
```bash
pip install -r requirements.txt
```


```bash
# Finally Execute the Following Command
python app.py
```

Now,
```bash
open up you local host and port
```


## MLflow
[Documentation](https://mlflow.org/docs/latest/index.html)


##### cmd
- mlflow ui

### dagshub
[dagshub](https://dagshub.com/)

MLFLOW_TRACKING_URI=https://dagshub.com/Shoaib-Alauudin/End-to-End-Machine-Learning-Project-with-MLFlow.mlflow \
MLFLOW_TRACKING_USERNAME=Shoaib-Alauudin \
MLFLOW_TRACKING_PASSWORD=f42b27e81f01196ca6c58b286c047cc1585ebfd4 \
python script.py

Execute Below Commands to Export as Environment Variables:

```bash

export MLFLOW_TRACKING_URI=https://dagshub.com/Shoaib-Alauudin/End-to-End-Machine-Learning-Project-with-MLFlow.mlflow

export MLFLOW_TRACKING_USERNAME=Shoaib-Alauudin 

export MLFLOW_TRACKING_PASSWORD=f42b27e81f01196ca6c58b286c047cc1585ebfd4

```



# AWS CICD Deployment with Github Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: 566373416292.dkr.ecr.ap-south-1.amazonaws.com/mlproj

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

    ECR_REPOSITORY_NAME = simple-app




## About MLflow 
MLflow

 - Its Production Grade
 - Trace all of your expriements
 - Logging & tagging your model