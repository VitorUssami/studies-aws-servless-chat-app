# [Studies][AWS] Servless Chat App

> This project represents hands on study, based on the [course 'Build a Serverless App' with AWS Lambda'  by Sundog Education](https://www.udemy.com/course/build-a-serverless-app-with-aws-lambda-hands-on).

## Summary

### **Hands-on using AWS servless services**

<p style="float:left">
    <img src="https://img.shields.io/badge/Amazon%20AWS-232F3E?style=plastic&logo=Amazon%20AWS&logoColor=white" /> 
    <img src="https://img.shields.io/badge/AWS%20Lambda-FF9900?style=plastic&logo=aws%20lambda&logoColor=white" /> 
	<img src="https://img.shields.io/badge/Amazon%20S3-569A31?style=plastic&logo=Amazon%20S3&logoColor=white" /> 
	<img src="https://img.shields.io/badge/Amazon%20CloudWatch-FF4F8B?style=plastic&logo=Amazon%20CloudWatch&logoColor=white" /> 
	<img src="https://img.shields.io/badge/Amazon%20API%20Gateway-FF4F8B?style=plastic&logo=Amazon%20API%20Gateway&logoColor=white" /> 
	<img src="https://img.shields.io/badge/Amazon%20DynamoDB-4053D6?style=plastic&logo=Amazon%20DynamoDB&logoColor=white" /> 
	<img src="https://img.shields.io/badge/Amazon%20CloudFront-8c3123?style=plastic" /> 
	<img src="https://img.shields.io/badge/Amazon%20Cognito-7a3e64?style=plastic" /> 
	<img src="https://img.shields.io/badge/AWS%20IAM-71973c?style=plastic" />
    <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=plastic&logo=JavaScript&logoColor=black" />
    <img src="https://img.shields.io/badge/HTML-dd4b25?style=plastic" />
    <img src="https://img.shields.io/badge/CSS-304cd9?style=plastic" />
</p>


The main goal of this project is to get some hands on experience on AWS. 

This is a chat app where users can login/signup and open conversation with another users.
The solution is based on AWS servless services.


### **Project Overview**
![overview](/docs/assets/images/overview.png)

### **What I've learned**

#### ***Amazon S3***
 - Create bucket and apply permissions to it. 
 - Upload and modify bucket's objects.

#### ***AWS Lambda***
 - Create Lambda functions
   - using javascript
 - Attach a role to functions
 - Create custom tests to validate the lamda function
 - Create alias  to functions
    - using alias approach you can 'decouple' some specific version while you're configuring the lambda on API gateway.
 - Create versions to functions
    - versions are important to not affect your stable production stage while you're modifying and validating some logic.
 - Lambda triggers

#### ***AWS Identity and Access Management (IAM)***
 - Create custom policies and roles
 - Policies and roles are super important to ensure a secure access to AWS resources.
 - Apply roles to AWS resources,

#### ***Amazon API Gateway***
 - Work using proxy mode
 - Work using mapping mode
 - Resources and methods
 - Models
   - attach models to methods executions
 - Deploy using Stages
   - create and use stages variables to decouple api gateway from client/implementation
 - Request flow
   - (client) -> method request -> integration request  -> (logic tier)
   - method request: 
     - It's where you can authorize, validate, cache
     - input: request path variables, query string params, request headers, request body
   - integration request:
     - receive incoming request and send it to destination
     - you can passthrough, remap
 - Response flow:
   - (client) <- method response <- integration response <- (logic tier)
   - method response: response definitions
   - integration response: response mapping, status code mapping
 - Export client (sdk generation)
 - Export documentation (Swagger/OpenAPI)

#### ***Amazon Cognito***
 - Create and configure 'user pools' 
 - Integrate cognito with API Gateway using 'Authorization' header

#### ***Amazon DynamoDB***
 - Create table, indexes
 - Create, read, update, delete itens to tables

#### ***Amazon CloudFront***
 - How to use CloudFront to exposes S3 objects more efficiently across the globe
 - Config cache time to live (TTL)
 - Invalidate cache/object

#### ***Amazon CloudWatch***
 - How to use CloudWatch to monitor metrics, alarms and logs.

### **Possible improvements**
 - Use a custom domain and Amazon Route 53.
 - Config API Gateway to use custom domain
