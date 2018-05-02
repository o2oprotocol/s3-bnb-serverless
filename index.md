---
layout: home
description: Free step-by-step guideline for creating full-stack apps with Serverless Framework and React.js. Build a Serverless REST-API and connect it to a React.js single-page application.
---

{: .toc-header }
## Table of Contents

### Set up your AWS account

- [Create an IAM user]({{ site.baseurl }}{% link _chapters/create-an-iam-user.md %})
  - [What is IAM]({{ site.baseurl }}{% link _chapters/what-is-iam.md %})
  - [What is an ARN]({{ site.baseurl }}{% link _chapters/what-is-an-arn.md %})
  - [Customize the Serverless IAM Policy]({{ site.baseurl }}{% link _chapters/customize-the-serverless-iam-policy.md %})
- [Configure the AWS CLI]({{ site.baseurl }}{% link _chapters/configure-the-aws-cli.md %})

### Setting up the Serverless Backend

- [Create a DynamoDB table]({{ site.baseurl }}{% link _chapters/create-a-dynamodb-table.md %})
- [Create an S3 bucket]({{ site.baseurl }}{% link _chapters/create-an-s3-bucket.md %})
- [Create an S3 bucket for file uploads]({{ site.baseurl }}{% link _chapters/create-an-s3-bucket-for-file-uploads.md %})
- [Create a Cognito user pool]({{ site.baseurl }}{% link _chapters/create-a-cognito-user-pool.md %})
  - [Create a Cognito test user]({{ site.baseurl }}{% link _chapters/create-a-cognito-test-user.md %})
- [Set up the Serverless Framework]({{ site.baseurl }}{% link _chapters/setup-the-serverless-framework.md %})
  - [Add support for ES6/ES7 JavaScript]({{ site.baseurl }}{% link _chapters/add-support-for-es6-es7-javascript.md %})

### TODO

### Deploying the Backend

- [Deploy the APIs]({{ site.baseurl }}{% link _chapters/deploy-the-apis.md %})
- [Create a Cognito identity pool]({{ site.baseurl }}{% link _chapters/create-a-cognito-identity-pool.md %})
  - [Cognito user pool vs identity pool]({{ site.baseurl }}{% link _chapters/cognito-user-pool-vs-identity-pool.md %})
- [Test the APIs]({{ site.baseurl }}{% link _chapters/test-the-apis.md %})

### Setting up a React App

- [Create a new React.js app]({{ site.baseurl }}{% link _chapters/create-a-new-reactjs-app.md %})
  - [Add app favicons]({{ site.baseurl }}{% link _chapters/add-app-favicons.md %})
  - [Set up custom fonts]({{ site.baseurl }}{% link _chapters/setup-custom-fonts.md %})
  - [Set up Bootstrap]({{ site.baseurl }}{% link _chapters/setup-bootstrap.md %})
- [Handle routes with React Router]({{ site.baseurl }}{% link _chapters/handle-routes-with-react-router.md %})
  - [Create containers]({{ site.baseurl }}{% link _chapters/create-containers.md %})
  - [Adding links in the navbar]({{ site.baseurl }}{% link _chapters/adding-links-in-the-navbar.md %})
  - [Handle 404s]({{ site.baseurl }}{% link _chapters/handle-404s.md %})
- [Configure AWS Amplify]({{ site.baseurl }}{% link _chapters/configure-aws-amplify.md %})

### Building a React App

- [Create a login page]({{ site.baseurl }}{% link _chapters/create-a-login-page.md %})
  - [Login with AWS Cognito]({{ site.baseurl }}{% link _chapters/login-with-aws-cognito.md %})
  - [Add the session to the state]({{ site.baseurl }}{% link _chapters/add-the-session-to-the-state.md %})
  - [Load the state from the session]({{ site.baseurl }}{% link _chapters/load-the-state-from-the-session.md %})
  - [Clear the session on logout]({{ site.baseurl }}{% link _chapters/clear-the-session-on-logout.md %})
  - [Redirect on login and logout]({{ site.baseurl }}{% link _chapters/redirect-on-login-and-logout.md %})
  - [Give feedback while logging in]({{ site.baseurl }}{% link _chapters/give-feedback-while-logging-in.md %})
- [Create a signup page]({{ site.baseurl }}{% link _chapters/create-a-signup-page.md %})
  - [Create the signup form]({{ site.baseurl }}{% link _chapters/create-the-signup-form.md %})
  - [Signup with AWS Cognito]({{ site.baseurl }}{% link _chapters/signup-with-aws-cognito.md %})
- [Add the create Listing page]({{ site.baseurl }}{% link _chapters/add-the-create-listing-page.md %})
  - [Call the create API]({{ site.baseurl }}{% link _chapters/call-the-create-api.md %})
  - [Upload a file to S3]({{ site.baseurl }}{% link _chapters/upload-a-file-to-s3.md %})
- [List all the Listings]({{ site.baseurl }}{% link _chapters/list-all-the-listing.md %})
  - [Call the list API]({{ site.baseurl }}{% link _chapters/call-the-list-api.md %})
- [Display a Listing]({{ site.baseurl }}{% link _chapters/display-a-listing.md %})
  - [Render the Listing form]({{ site.baseurl }}{% link _chapters/render-the-listing-form.md %})
  - [Save changes to a Listing]({{ site.baseurl }}{% link _chapters/save-changes-to-a-listing.md %})
  - [Delete a Listing]({{ site.baseurl }}{% link _chapters/delete-a-listing.md %})
- [Set up secure pages]({{ site.baseurl }}{% link _chapters/setup-secure-pages.md %})
  - [Create a route that redirects]({{ site.baseurl }}{% link _chapters/create-a-route-that-redirects.md %})
  - [Use the redirect routes]({{ site.baseurl }}{% link _chapters/use-the-redirect-routes.md %})
  - [Redirect on login]({{ site.baseurl }}{% link _chapters/redirect-on-login.md %})

### Deploying a React app on AWS

- [Deploy the Frontend]({{ site.baseurl }}{% link _chapters/deploy-the-frontend.md %})
  - [Deploy to S3]({{ site.baseurl }}{% link _chapters/deploy-to-s3.md %})
  - [Create a CloudFront distribution]({{ site.baseurl }}{% link _chapters/create-a-cloudfront-distribution.md %})
  - [Set up your domain with CloudFront]({{ site.baseurl }}{% link _chapters/setup-your-domain-with-cloudfront.md %})
  - [Set up www domain redirect]({{ site.baseurl }}{% link _chapters/setup-www-domain-redirect.md %})
  - [Set up SSL]({{ site.baseurl }}{% link _chapters/setup-ssl.md %})
- [Deploy updates]({{ site.baseurl }}{% link _chapters/deploy-updates.md %})
  - [Update the app]({{ site.baseurl }}{% link _chapters/update-the-app.md %})
  - [Deploy again]({{ site.baseurl }}{% link _chapters/deploy-again.md %})

### Advanced Topics

Backend

  - [API Gateway and Lambda Logs]({{ site.baseurl }}{% link _chapters/api-gateway-and-lambda-logs.md %})
  - [Debugging Serverless API Issues]({{ site.baseurl }}{% link _chapters/debugging-serverless-api-issues.md %})

  - [Serverless environment variables]({{ site.baseurl }}{% link _chapters/serverless-environment-variables.md %})
  - [Stages in Serverless Framework]({{ site.baseurl }}{% link _chapters/stages-in-serverless-framework.md %})

  - [Configure multiple AWS profiles]({{ site.baseurl }}{% link _chapters/configure-multiple-aws-profiles.md %})

  - [Customize the Serverless IAM Policy]({{ site.baseurl }}{% link _chapters/customize-the-serverless-iam-policy.md %})

Frontend

  - [Code Splitting in Create React App]({{ site.baseurl }}{% link _chapters/code-splitting-in-create-react-app.md %})
  - [Environments in Create React App]({{ site.baseurl }}{% link _chapters/environments-in-create-react-app.md %})

### Reference

- [Connect to API Gateway with IAM auth]({{ site.baseurl }}{% link _chapters/connect-to-api-gateway-with-iam-auth.md %})
- [Serverless Node.js Starter]({{ site.baseurl }}{% link _chapters/serverless-nodejs-starter.md %})