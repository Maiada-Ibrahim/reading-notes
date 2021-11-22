# Serverless
Serverless computing is a method of providing backend services on an as-used basis. Servers are still used, but a company that gets backend services from a serverless vendor is charged based on usage, not a fixed amount of bandwidth or number of servers.

- some cloud services:AWS Lambda ,Google Cloud Functions ,Azure Functions ,IBM OpenWhisk ,Alibaba Function Compute ,Iron Functions ,Auth0 Webtask ,Oracle Fn Project ,Kubeless

##  some inftomation for serverless : 
-  reduced the cost
- in networking The downside is that Serverless functions are accessed only as private APIs.
- for dependency we must package these dependencies into the application itself
- Setting up different environments for Serverless is easy
- there’s a hard 300-second timeout limit.
- Scaling process is automatic and seamless

## The Serverless App
A Serverless solution consists of a web server, Lambda functions (FaaS), security token service (STS), user authentication and database.
![](https://hackernoon.com/hn-images/1*TIrjN7EjLUVJmJ6YvHR7Dg.png)

## Benefits of Serverless Architecture
- Benefits of Serverless Architecture
 reduced the cost,Process agility,Cost of hiring backend infrastructure engineers goes down.
- From developer perspective
Lower costs,Simplified scalability,Simplified backend code,Quicker turnaround .

## Serverless Frameworks
Serverless Framework (Javascript, Python, Golang)
Apex (Javascript)
ClaudiaJS (Javascript)
Sparta (Golang)
Gordon (Javascript)
Zappa (Python)
Up (Javascript, Python, Golang, Crystal)

# FaaS
FaaS is an implementation of Serverless architectures where engineers can deploy an individual function or a piece of business logic
![](https://s7280.pcdn.co/wp-content/uploads/2020/12/key-14.png)
Principles of FaaS:

Complete management of servers
Invocation based billing
Event-driven and instantaneously scalabl2
properties of FaaS

With Serverless, everything is stateless
Ephemeral
functions can be invoked directly,
Scalable by default
Fully managed by a Cloud vendor
A Serverless solution consists of a web server, Lambda functions (FaaS), security token service (STS), user authentication and database


# AWS Amplify
 is a JavaScript library for frontend and mobile developers building cloud-enabled applications. The library is a declarative interface across different categories of operations in order to make common tasks easier to add into your application.
 Benefits in pic
 ![](https://d1.awsstatic.com/AWS%20Amplify/Features/product-page-diagram_Amplify_How-it-works_Deliver%402x%20(1).26991c2935dc23236759635449c17c56e549658a.png)


 # API (GRAPHQL)
helps you quickly create backends for your web and mobile applications on AWS. With the GraphQL Transform

define your application’s data model using the GraphQL Schema Definition Language (SDL) and the library handles converting your SDL definition into a set of fully descriptive AWS CloudFormation templates that implement your data model.

## Create a GraphQL API
1. amplify init
2. amplify add api
- Select GraphQL
- When asked if you have a schema, say No
- Select one of the default samples; you can change this later
- Choose to edit the schema and it will open the new schema.graphql in your editor
3. amplify push
for updatting schema amplify api gql-compile then amplify push