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
- Bucket name- tianasdemobucket
- ACLs Disabled
- Uncheck 'Block all public access' and acknowledge
- Enable bucket versioning if you wish to restore previous iterations of the site
- Leave deafult settings for default encryption
- Leave object lock as diabled if not using versioning
- Click create bucket

## Upload website files to S3
- Create Index.html file in TextEdit

<!DOCTYPE html>
<html>
<head>
  <title>Tiana’s Cool Demo Site</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Hello from AWS S3!</h1>
  <p>This is a static website hosted on Amazon S3.</p>
</body>
</html>

- Create style.css file in TextEdit

body {
  font-family: Arial, sans-serif;
  text-align: center;
  margin-top: 50px;
}
h1 {
  color: #2b6cb0;
}

- Upload the Index.html and style.css file to the S3 bucket
- In the S3 bucket click the Properties tab
- Scroll down to Static website hosting
- Click enable
- Click Host a static website
- For index document enter 'Index.html'
- Leave error document blank
- Leave redirection rules blank
- Save changes

## Change S3 bucket policy
- Click on the permissions tab
- Edit Bucket polixy
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "Statement1",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:*",
            "Resource": "arn:aws:s3:::tianasdemobucket/*"
        }
    ]
}
