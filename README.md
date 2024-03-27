# Title
A simple serverless [FastAPI](https://fastapi.tiangolo.com/) application using [Mangum](https://pypi.org/project/mangum/) to run on an AWS [Lambda](https://aws.amazon.com/lambda/).

# Pre-Requisites
* Step 1: Setup Virtual Environment
```
pip3 install virtualenv 
virtualenv -p python3 env
source ./env/bin/activate
```
* Step 2: Clone repo
```
git clone https://github.com/krishnamaram2025/fastapi-lambda.git
```

### Package Lambda
* Step 1: Install app level Dependencies
```
pip3 install -r fastapi-lambda/requirements.txt
```
* Step 2:Package Dependencies
```
cd env/lib/python3.10/site-packages
zip -r9 ../../../../fastapi-lambda/function.zip .
cd ../../../../fastapi-lambda
zip -g ./function.zip -r app
```
# Run the application on local
```shell
uvicorn app.main:app --host 0.0.0.0 --port 8000 --reload
```
# Create S3 bucket

# Create Lambda Function

# Create API Gateway

# References

### [Simple Serverless FastAPI with AWS Lambda Complete Walkthrough](https://deadbearcode.com/simple-serverless-fastapi-with-aws-lambda/)
