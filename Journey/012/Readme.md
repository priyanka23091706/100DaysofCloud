**Add a cover photo like:**
![placeholder image](https://via.placeholder.com/1200x600)

# CodeDeploy to ECS

## Introduction

✍️ 
```
## Get the root access using the following command: 

sudo su

## Now run the updates using the following command: 

yum -y update

## Check the Docker version by running the following command:

docker version

## Install AWS CLI by running the following command:

yum install awscli -y

## Pull the docker image called httpd. By running the below command, you will pull httpd:latest from docker hub.

docker pull httpd

## List the docker images, using the following command:

docker images

## Create an ECR Repository and copy its repository URI from output of the below command:

aws ecr create-repository --repository-name httpd --region us-east-1

```
docker tag httpd:latest <Accountid>.dkr.ecr.us-east-1.amazonaws.com/httpd:latest

Login into the ECR and push the docker image 
## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[link](link)
