# Amazon S3

![](https://d2908q01vomqb2.cloudfront.net/0a57cb53ba59c46fc4b692527a38a87c78d84028/2019/07/31/Untitled-Diagram-2.jpg)
Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance


Features of Amazon S3
- Storage classes:a range of storage classes designed for different use cases


- Storage management: manage costs, meet regulatory requirements, reduce latency, and save multiple distinct copies of your data for compliance requirements using S3 Lifecycle ,S3 Object Lock ,S3 Replication ,S3 Batch Operations.



- Access management:You can use AWS Identity and Access Management (IAM) to manage access to your Amazon S3 resources,You can control access to each of your buckets and objects using an access control list (ACL)





- Data processing:
modify and process data as it is returned to an application. Filter rows, dynamically resize images, redact confidential data, and much more,Trigger workflows that use Amazon Simple Notification Service (Amazon SNS),


- Storage logging and monitoring
- Analytics and insights
- Strong consistency


## Amazon S3 data consistency model
Amazon S3 provides strong read-after-write consistency for PUTs and DELETEs of objects in your Amazon S3 bucket in all AWS Regions.

Amazon S3 achieves high availability by replicating data across multiple servers within AWS data centers. If a PUT request is successful, your data is safely stored. Any read (GET or LIST) that is initiated following the receipt of a successful PUT response will return the data written by the PUT

 common operations
Create a bucket
Write an object
Read an object
Delete an object


## Amazon S3 application programming interfaces (API)
it's provides a REST and a SOAP interface
- The REST interface The REST API is an HTTP interface to Amazon S3. Using REST, you use standard HTTP requests to create, fetch, and delete buckets and objects.

- The SOAP interface The SOAP API provides a SOAP 1.1 interface using document literal encoding. The most common way to use SOAP is to download the WSDL

## Related services
Amazon Elastic Compute Cloud (Amazon EC2),Amazon EMR,AWS Snow Family,AWS Transfer Family.

## step for STORAGE
1. amplify add storage answer some qustion
2.amplify push
3.add dependencies and  Sync .
4.Initialize Amplify Storage by
her he CLI will configure appropriate IAM policies on the bucket using a Cognito Identity Pool Role. You will have the option of adding CRUD (Create, Update, Read and Delete) based permissions as well, so that Authenticated and Guest users will be granted limited permissions within these levels

you can

- upload file using different ways
- Download file using Amplify. Storage.downloadFile
- You can list all of the objects uploaded under a given prefix


       Amplify.Storage.list("/",
       result -> {
        for (StorageItem item :   result.getItems()) {
            Log.i("MyAmplifyApp", "Item: " + item.getKey());
        }
       },
          error -> Log.e("MyAmplifyApp", "List failure", error)
       
       );
- To delete an object uploaded to S3, use Amplify.Storage.remove and specify the key 