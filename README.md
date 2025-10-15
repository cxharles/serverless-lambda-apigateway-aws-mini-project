#  How to setup serverless-lambda-apigateway-aws-mini-project
# 

[https://harishnshetty.github.io/projects.html](https://harishnshetty.github.io/projects.html)

[![Video Tutorial](https://github.com/harishnshetty/image-data-project/blob/f7b2a2490ad8bae5c0ee6f9056160a6275678341/serverless%20pyhton%20Project.jpg)](https://youtu.be/G6xeBhUgGBo)

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


[![Video Tutorial](https://github.com/harishnshetty/image-data-project/blob/f7b2a2490ad8bae5c0ee6f9056160a6275678341/serverless%20pyhton%20Project1.jpg)](https://youtu.be/G6xeBhUgGBo)


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

## Createa ACM certificate

## Access the API Gateway Via Custom Domain

- in the API GATEWAY Select the  [ Custom domain names ]
- Add domain name
- api.harishshetty.xyz
- Attach the ACM certificate
- Configure API mappings

- API [ lambda ]
- Stage [ dev ]
- Path (optional) [ dev ]

## Add it in the Route53

- Creata a Record [ api ]
- Alias
- select service
- select region
- Select the api url