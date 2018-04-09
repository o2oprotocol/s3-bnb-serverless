---
layout: post
title: Deploy the APIs
date: 2018-01-04 00:00:00
description: Use the “serverless deploy” command to deploy to AWS Lambda and API Gateway using the Serverless Framework. Running this command will display the list of deployed API endpoints and the AWS region it was deployed to. And we can run the "serverless deploy function" command when we want to update an individual Lambda function.
context: backend
code: backend_full
comments_id: 28
---

Now that our APIs are complete, let's deploy them.

<img class="code-marker" src="/assets/s.png" />Run the following in your working directory.

``` bash
$ serverless deploy
```

If you have multiple profiles for your AWS SDK credentials, you will need to explicitly pick one. Use the following command instead:

``` bash
$ serverless deploy --aws-profile myProfile
```

Where `myProfile` is the name of the AWS profile you want to use. If you need more info on how to work with AWS profiles in Serverless, refer to our [Configure multiple AWS profiles]({% link _chapters/configure-multiple-aws-profiles.md %}) chapter.

Near the bottom of the output for this command, you will find the **Service Information**.

``` bash
Service Information
service: notes-app-api
stage: prod
region: us-east-1
api keys:
  None
endpoints:
  POST - https://ly55wbovq4.execute-api.us-east-1.amazonaws.com/prod/notes
  GET - https://ly55wbovq4.execute-api.us-east-1.amazonaws.com/prod/notes/{id}
  GET - https://ly55wbovq4.execute-api.us-east-1.amazonaws.com/prod/notes
  PUT - https://ly55wbovq4.execute-api.us-east-1.amazonaws.com/prod/notes/{id}
  DELETE - https://ly55wbovq4.execute-api.us-east-1.amazonaws.com/prod/notes/{id}
functions:
  notes-app-api-prod-create
  notes-app-api-prod-get
  notes-app-api-prod-list
  notes-app-api-prod-update
  notes-app-api-prod-delete
```

This has a list of the API endpoints that were created. Make a note of these endpoints as we are going to use them later while creating our frontend. Also make a note of the region and the id in these endpoints, we are going to use them in the coming chapters. In our case, `us-east-1` is our API Gateway Region and `ly55wbovq4` is our API Gateway ID.

### Deploy a Single Function

There are going to be cases where you might want to deploy just a single API endpoint as opposed to all of them. The `serverless deploy function` command deploys an individual function without going through the entire deployment cycle. This is a much faster way of deploying the changes we make.

For example, to deploy the list function again, we can run the following.

``` bash
$ serverless deploy function -f list
```

Now before we test our APIs we have one final thing to set up. We need to ensure that our users can securely access the AWS resources we have created so far. Let's look at setting up a Cognito Identity Pool.
