---
layout: home
description: Free step-by-step guideline for creating full-stack apps with Serverless Framework and React.js. Build a Serverless REST-API and connect it to a React.js single-page application.
---

{: .toc-header }
## Table of Contents

### Set up your AWS account

- [Create an IAM user]({% link _chapters/create-an-iam-user.md %})
  - [What is IAM]({% link _chapters/what-is-iam.md %})
  - [What is an ARN]({% link _chapters/what-is-an-arn.md %})
  - [Customize the Serverless IAM Policy]({% link _chapters/customize-the-serverless-iam-policy.md %})
- [Configure the AWS CLI]({% link _chapters/configure-the-aws-cli.md %})

### Setting up the Serverless Backend

- [Create a DynamoDB table]({% link _chapters/create-a-dynamodb-table.md %})
- [Create an S3 bucket for file uploads]({% link _chapters/create-an-s3-bucket-for-file-uploads.md %})
- [Create a Cognito user pool]({% link _chapters/create-a-cognito-user-pool.md %})
  - [Create a Cognito test user]({% link _chapters/create-a-cognito-test-user.md %})
- [Set up the Serverless Framework]({% link _chapters/setup-the-serverless-framework.md %})
  - [Add support for ES6/ES7 JavaScript]({% link _chapters/add-support-for-es6-es7-javascript.md %})

### TODO

### Setting up a React App

- [Create a new React.js app]({% link _chapters/create-a-new-reactjs-app.md %})
  - [Add app favicons]({% link _chapters/add-app-favicons.md %})
  - [Set up custom fonts]({% link _chapters/setup-custom-fonts.md %})
  - [Set up Bootstrap]({% link _chapters/setup-bootstrap.md %})
- [Handle routes with React Router]({% link _chapters/handle-routes-with-react-router.md %})
  - [Create containers]({% link _chapters/create-containers.md %})
  - [Adding links in the navbar]({% link _chapters/adding-links-in-the-navbar.md %})
  - [Handle 404s]({% link _chapters/handle-404s.md %})
- [Configure AWS Amplify]({% link _chapters/configure-aws-amplify.md %})

### Building a React App

- [Create a login page]({% link _chapters/create-a-login-page.md %})
  - [Login with AWS Cognito]({% link _chapters/login-with-aws-cognito.md %})
  - [Add the session to the state]({% link _chapters/add-the-session-to-the-state.md %})
  - [Load the state from the session]({% link _chapters/load-the-state-from-the-session.md %})
  - [Clear the session on logout]({% link _chapters/clear-the-session-on-logout.md %})
  - [Redirect on login and logout]({% link _chapters/redirect-on-login-and-logout.md %})
  - [Give feedback while logging in]({% link _chapters/give-feedback-while-logging-in.md %})
- [Create a signup page]({% link _chapters/create-a-signup-page.md %})
  - [Create the signup form]({% link _chapters/create-the-signup-form.md %})
  - [Signup with AWS Cognito]({% link _chapters/signup-with-aws-cognito.md %})
- [Add the create Listing page]({% link _chapters/add-the-create-listing-page.md %})
  - [Call the create API]({% link _chapters/call-the-create-api.md %})
  - [Upload a file to S3]({% link _chapters/upload-a-file-to-s3.md %})
- [List all the Listings]({% link _chapters/list-all-the-listing.md %})
  - [Call the list API]({% link _chapters/call-the-list-api.md %})
- [Display a Listing]({% link _chapters/display-a-listing.md %})
  - [Render the Listing form]({% link _chapters/render-the-listing-form.md %})
  - [Save changes to a Listing]({% link _chapters/save-changes-to-a-listing.md %})
  - [Delete a Listing]({% link _chapters/delete-a-listing.md %})
- [Set up secure pages]({% link _chapters/setup-secure-pages.md %})
  - [Create a route that redirects]({% link _chapters/create-a-route-that-redirects.md %})
  - [Use the redirect routes]({% link _chapters/use-the-redirect-routes.md %})
  - [Redirect on login]({% link _chapters/redirect-on-login.md %})

### Deploying a React app on AWS

- [Deploy the Frontend]({% link _chapters/deploy-the-frontend.md %})
  - [Create an S3 bucket]({% link _chapters/create-an-s3-bucket.md %})
  - [Deploy to S3]({% link _chapters/deploy-to-s3.md %})
  - [Create a CloudFront distribution]({% link _chapters/create-a-cloudfront-distribution.md %})
  - [Set up your domain with CloudFront]({% link _chapters/setup-your-domain-with-cloudfront.md %})
  - [Set up www domain redirect]({% link _chapters/setup-www-domain-redirect.md %})
  - [Set up SSL]({% link _chapters/setup-ssl.md %})
- [Deploy updates]({% link _chapters/deploy-updates.md %})
  - [Update the app]({% link _chapters/update-the-app.md %})
  - [Deploy again]({% link _chapters/deploy-again.md %})