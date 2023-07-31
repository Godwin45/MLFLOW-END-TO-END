# End-to-end-Machine-Learning-Project-with-MLflow(Wine Quality Prediction Software)

<img width="314" alt="mlflow2" src="https://github.com/Godwin45/MLFLOW-END-TO-END/assets/71969710/3184d81b-4909-4ba8-a8ec-b5b76179bbed">

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Machine Learning Model - Elastic Model](#machine-learning-model---elastic-model)
- [MLflow Tracking](#mlflow-tracking)
- [AWS Deployment](#aws-deployment)
- [Continuous Integration and Continuous Deployment (CI/CD) Pipelines](#continuous-integration-and-continuous-deployment-cicd-pipelines)
- [Docker Containers](#docker-containers)
- [Getting Started](#getting-started)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Welcome to the Wine Quality Prediction Software! This innovative application utilizes the power of Machine Learning to predict the quality of wines. Whether you're a wine enthusiast, a sommelier, or a winemaker, this software will help you make informed decisions about wine quality based on data-driven predictions.

## Features

- Wine Quality Prediction: The software uses advanced Machine Learning algorithms to predict the quality of wines based on various input features.
- Elastic Model: Our predictive model is built on the Elastic Model architecture, ensuring optimal adaptability and accuracy across different datasets.
- MLflow Tracking: Track, manage, and visualize your Machine Learning experiments effortlessly with MLflow integration, making it easy to compare and reproduce results.
- AWS Deployment: Deploy your Wine Quality Prediction Software on Amazon Web Services (AWS) for reliable and scalable performance.
- Continuous Integration and Continuous Deployment (CI/CD) Pipelines: Implement seamless integration and deployment processes to ensure efficiency and robustness in software updates.
- Docker Containers: Package the application and its dependencies in Docker containers, making deployment and portability straightforward.

## Machine Learning Model - Elastic Model

The Wine Quality Prediction Software incorporates an Elastic Model for wine quality predictions. The Elastic Model architecture is designed to handle varying data distributions, making it a robust choice for diverse wine datasets. It can adapt and scale efficiently as new data becomes available, ensuring continuous high-quality predictions.

## MLflow Tracking

With MLflow integration, the Wine Quality Prediction Software allows you to keep track of your Machine Learning experiments effortlessly. MLflow provides a comprehensive tracking system, enabling you to log 
and compare different models, hyperparameters, and metrics.
<img width="951" alt="mlflow0" src="https://github.com/Godwin45/MLFLOW-END-TO-END/assets/71969710/a1cc179e-6ce9-4dbe-9c46-a0367fb895e0">
 This ensures transparency, reproducibility, and optimal decision-making in your wine quality predictions.

<img width="681" alt="mlflow1" src="https://github.com/Godwin45/MLFLOW-END-TO-END/assets/71969710/cbe5635f-50d8-4e60-af67-26bb0cb43996">


## AWS Deployment

Deploy your Wine Quality Prediction Software on Amazon Web Services (AWS) to leverage its powerful cloud infrastructure. AWS provides high availability, scalability, and security, ensuring your application is accessible to users worldwide without compromising performance.

## Continuous Integration and Continuous Deployment (CI/CD) Pipelines

Our software leverages CI/CD pipelines, automating the process of integrating new code changes and deploying updates efficiently. This results in a more streamlined development workflow, faster releases, and robust software delivery.
<img width="373" alt="mlflow3" src="https://github.com/Godwin45/MLFLOW-END-TO-END/assets/71969710/0be72121-3287-4bd9-8710-631203d9be04">

## Docker Containers

We believe in simplifying deployment and portability. That's why we package our Wine Quality Prediction Software and all its dependencies into Docker containers. Docker enables you to run the software consistently across different environments, eliminating potential compatibility issues and ensuring seamless deployment.

## Getting Started

Follow these simple steps to get started with the Wine Quality Prediction Software:

1. Clone the repository: `git clone https://github.com/your-username/wine-quality-prediction.git`
2. Install the required dependencies: `pip install -r requirements.txt`
3. Launch the application: `python app.py`
4. Access the software through your web browser: `http://localhost:8000`

That's it! You are now ready to explore the world of wine quality prediction!

## Contributing

We welcome contributions from the community. If you have any ideas, suggestions, or bug fixes, please feel free to open an issue or submit a pull request.

## License

This software is distributed under the MIT License. See [LICENSE](LICENSE) for more information.

Enjoy predicting wine quality with the Wine Quality Prediction Software! Cheers! 🍷🍷🍷


## Workflows

1. Update config.yaml
2. Update schema.yaml
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline 
8. Update the main.py
9. Update the app.py



# How to run?
### STEPS:

Clone the repository

```bash
https://github.com/Godwin45/MLFLOW-END-TO-END```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n mlproj python=3.8 -y
```

```bash
conda activate mlproj
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


```bash
# Finally run the following command
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

MLFLOW_TRACKING_URI=https://dagshub.com/Godwin45/MLFLOW-END-TO-END.mlflow \
MLFLOW_TRACKING_USERNAME=Godwin45 \
MLFLOW_TRACKING_PASSWORD=8895347721dd5cd1b0369aba5665f82a77ca7d72 \
python script.py

Run this to export as env variables:

```bash

set MLFLOW_TRACKING_URI=https://dagshub.com/Godwin45/MLFLOW-END-TO-END.mlflow 

set MLFLOW_TRACKING_USERNAME=Godwin45

set MLFLOW_TRACKING_PASSWORD=8895347721dd5cd1b0369aba5665f82a77ca7d72

```



# AWS-CICD-Deployment-with-Github-Actions

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


