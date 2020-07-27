# s3-lamda-flv-to-mp4-converter

This project contains source code and supporting files for a serverless application that you can deploy with the AWS Serverless Application Model (AWS SAM) command line interface (CLI). It includes the following files and folders:

- `src` - Code for the application's Lambda function.
- `__tests__` - Unit tests for the application code.
- `template.yml` - A template that defines the application's AWS resources.

Resources for this project are defined in the `template.yml` file in this project. You can update the template to add AWS resources through the same deployment process that updates your application code.

## Deploy this application
### Step 1:
First, deploy this - https://serverlessrepo.aws.amazon.com/applications/arn:aws:serverlessrepo:us-east-1:145266761615:applications~ffmpeg-lambda-layer

It will return an ARN that will be needed in the lambda function.

### Step 2:
Supply unique values for the following:
1. InputS3BucketName
2. OutputS3BucketName
3. AwsRegion
4. LayerArn - ARN returned in Step 1
