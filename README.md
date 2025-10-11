# serverless-lambda-apigateway-aws-mini-project


## Create a Dynamo DB

- create table
---
- Table name : harish
- Partition key : email
- [create table]

## Create a IAM Role For lambda

- Click on the Roles
- Create a Role 
- Aws Service [Select - Lambda ]
- Select [ AdministratorAccess ]
- Role name [ Lambda-Role ]

## Create a Lambda

- Createa a function 
- Function name [ harish ]
- Runtime [ Python 3.13 ]
- Use an existing role [ Lambda-Role ]

- Click on the configuration [ Edit ] 
- Timeout [ 15 Minutes 0 Sec ]

- Upload the Contents Via the Code 


## Create a API gateway

- Create an API 
- REST API [ Build ]
- API name [ Lambda ]
- Create method 
- Method type [ GET ]
- Lambda proxy integration [ Enable ]
- Lambda function [ Select the lambda Function ]

- Create method 
- Method type [ POST ]
- Lambda proxy integration [ Enable ]
- Lambda function [ Select the lambda Function ]

- Deploy API
- *New Stage*
- Stage name [ dev ]

- Copy the Invoke URL : https://xxxxxx.execute-api.ap-south-1.amazonaws.com/dev
