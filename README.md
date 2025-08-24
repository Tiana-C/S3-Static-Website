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
<br></br>
![Final Website](https://github.com/Tiana-C/S3-Static-Website/blob/main/htmldemo.png)
-Create style.css file in TextEdit
<br></br>
![Final Website](https://github.com/Tiana-C/S3-Static-Website/blob/main/cssdemo.png)

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
<br></br>
![Final Website](https://github.com/Tiana-C/S3-Static-Website/blob/main/bucketpolicy.png)
## Static website is now hosted on an S3 bucket
![Final Website](https://github.com/Tiana-C/S3-Static-Website/blob/main/Static%20Site%20on%20S3.png)

