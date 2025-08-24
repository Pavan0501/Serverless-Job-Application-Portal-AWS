# Serverless-Job-Application-Portal-AWS

A serverless job application portal built on AWS using Lambda, API Gateway, DynamoDB, and S3.  
Applicants can submit resumes, recruiters can review applications, all powered by a scalable and cost-effective serverless architecture.  

### Overview

A fully serverless job application portal designed with the following stack: 

Frontend--> HTML, CSS, JavaScript (static hosting on S3)  

Backend--> AWS Lambda (Python), API Gateway, DynamoDB, and S3 

Features

- Applicants can submit details and upload resumes.
  
- Recruiters can view all applications and open resumes directly from the portal.
  
- Application data is stored in "DynamoDB" and resumes in "S3".
  
- Fully serverless architecture ensuring scalability, high availability, and low cost.

Architecture Diagram

<img width="1676" height="964" alt="serverless-web-application" src="https://github.com/user-attachments/assets/62b73644-7fcd-4a65-81fa-5eebd9d91f8e" />

How It Works

Applicant Portal:

1. Users fill out a form and upload their resume.
    
2. Data is sent to an API Gateway endpoint, which triggers a Lambda function.
  
3. The Lambda function stores application details in DynamoDB and uploads resumes to S3.

Recruiter Portal:

1. Recruiters access a protected page to view submitted applications.
 
2. The page retrieves data from a GET Lambda endpoint exposed via API Gateway.
  
3. Resumes can be accessed through secure S3 links.

Configuration

- Update the API endpoint URLs in the frontend JavaScript as required.
  
- To use a different S3 bucket for resumes, update the `bucketName` variable in the recruiter portal JavaScript file.

Deployment

1. Deploy Lambda functions using AWS Console or Serverless Framework.
 
2. Upload static frontend files to an S3 bucket with static website hosting enabled.
 
3. Enable CORS on API Gateway for your frontend domain.

This setup delivers a production-ready, scalable, and cost-efficient job application management portal using AWS serverless services.
