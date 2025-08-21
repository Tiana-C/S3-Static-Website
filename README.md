# AWS Project: Static Website Hosting on S3

## Overview
This project demonstrates how to host a **static website on Amazon S3** using the AWS Free Tier.  
It includes:
- An S3 bucket for static content
- S3 bucket website hosting configuration
- Public access policies

## Services Used
- **Amazon S3** – Static website hosting
- **IAM** – Access control

## Architecture
- End User > S3 bucket

## Deployment 
## Create a S3 bucket
- Go to S3 > Create bucket
- Bucket type- General purpose
- Bucket name- DemoSiteBucket
- ACLs Disabled
- Uncheck 'Block all public access' and acknowledge
- Enable bucket versioning if you wish to restore previous iterations of the site
- Leave deafult settings for default encryption
- Leave object lock as diabled if not using versioning 
