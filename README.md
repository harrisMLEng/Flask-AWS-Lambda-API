# Serverless Flask Application on AWS Lambda
This project demonstrates how to deploy a serverless Flask application on AWS Lambda using the AWS Serverless Application Model (SAM).

## Prerequisites
Before you begin, make sure you have the following installed and configured:

- Python 3.8 or later
- AWS CLI
- AWS SAM CLI
- Docker

## Project Structure
The project contains the following key files and directories:

* hello_world/: Contains the Flask application and its dependencies.
* template.yaml: Defines the AWS resources, including Lambda function and API Gateway, for the serverless application.
* samconfig.toml: Stores deployment configurations for the AWS SAM CLI.

## Local Development and Testing
To test your serverless Flask application locally, follow these steps:

1. Build your application using the sam build command.
2. Start the API Gateway locally with the sam local start-api command.
3. Test your application by making a request to the local API Gateway using a tool like curl or by simply opening the URL in your web browser.

For more details on local development and testing, refer to the sections above on testing locally and testing using events.

## Deployment
To deploy your serverless Flask application to AWS, follow these steps:

1. Run ```sam build``` to build your application.
2. Run ```sam deploy -g --stack-name flask-aws-lambda-api``` to initiate the guided deployment process, which will prompt you for deployment parameters and create or update the CloudFormation stack.

## Cleanup
To delete all resources created by the deployment process, run the following command:

```aws cloudformation delete-stack --stack-name flask-aws-lambda-api```
