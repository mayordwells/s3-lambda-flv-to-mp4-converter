# s3-lambda-flv-to-mp4-converter

This project is an extension of https://github.com/simalexan/s3-lambda-ffmpeg-mov-to-mp4-s3, at the time of its creation, the project was already outdated and had the following problems.
1. The function was created 2 years so the code is a bit outdated
2. The runtime version, node version 8 is not supported anymore, the least supported version of node is now version 10. I have updated the function to use the latest supported version node 12
3. Issues with the S3 bucket name, names of s3 buckets has to be unique globally. That is not specified in the doc.

The source code and supporting files for a serverless application that you can deploy with the AWS Serverless Application Model (AWS SAM) command line interface (CLI). It includes the following files and folders:

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

## Deploy
Simply search for converter here - https://console.aws.amazon.com/serverlessrepo/home?region=us-east-1#/available-applications
