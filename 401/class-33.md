
## Creating a useful GraphQL server using AWS Amplify
![](https://www.qsstechnosoft.com/wp-content/uploads/2019/09/RelayReducers.png)
- AWS Amplify brings together multiple AWS services in a powerful tool that generates the backend infrastructure, communication and authentication between AWS services.


- @connection directive enables you to specify relationships between @model types

The tool can allow you to write a GraphQL schema, have the backend resolvers and database generated automatically, plus host everything on AWS, and a lot more so we need AWS account

## Set up AWS Amplify
- First, follow the [first page of this guide](https://docs.amplify.aws/cli/start/install/#pre-requisites-for-installation) to set up AWS Amplify CLI.

- add Amplify features to the project
- Open the folder you want to contain your project in your terminal, and run the command amplify init This will ask you some basic questions about your app, but it’s good to keep things as default for now

## Create a basic GraphQL API
  you have to use a custom Amplify GraphQL directive called @connection. This creates a link between two fields, and can be implemented per the following:

       type Topic @model {
     id: ID!
     title: String!
      description: String
      comments: [Comment] @connection(keyName: "TopicComments")
      tags: [Tag]
     }

    type Tag @model {
     id: ID!
          tag: String
    topics: [Topic]
     }

      type Comment @model {
         id: ID!
         text: String
     topic: Topic @connection(keyName: "TopicComments")
      }






- If you save your updated schema and refresh GraphiQL, you will notice in the documentation for the createCommment mutation that there is a new field on the input for this type

       mutation {
      createComment(input: {
       text: "Yeah, let's look into Amplify.",
      commentTopicId: "9500834d-186e-41ae-9ac5-ccef4b838afb"
       }) {
       id
       text
       }
        }

one-to-one connection

      type Project @model {
       id: ID!
     name: String
       team: Team @connection
    }

     type Team @model {
     id: ID!
     name: String!
     }


-  one-to-many connection

        type Post @model {
        id: ID!
        title: String!
        comments: [Comment] @connection(keyName: "byPost", fields: ["id"])
       }

       type Comment @model
         @key(name: "byPost", fields: ["postID", "content"]) {
         id: ID!
         postID: ID!
         content: String!
         }
- Many-to-many connections
we can implement many to many using two 1-M @connections, an @key, and a joining @model.