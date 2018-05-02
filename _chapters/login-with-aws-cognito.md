---
layout: post
title: Login with AWS Cognito
date: 2018-01-14 00:00:00
description: To allow users to login using Amazon Cognito in our React.js app, we are going to use AWS Amplify. We need the Cognito User Pool Id and our App Client Id. We login the user by calling the Auth.signIn() method from AWS Amplify.
context: frontend
comments_id: 38
---

We are going to use AWS Amplify to login to our Amazon Cognito setup. Let's start by importing it. 

### Import Auth from AWS Amplify

<img class="code-marker" src="{{ site.baseurl }}/assets/s.png" />Add the following to the header of our Login container in `src/containers/Login.js`.

``` coffee
import { Auth } from "aws-amplify";
```

### Login to Amazon Cognito

The login code itself is relatively simple.

<img class="code-marker" src="{{ site.baseurl }}/assets/s.png" />Simply replace our placeholder `handleSubmit` method in `src/containers/Login.js` with the following.

``` javascript
handleSubmit = async event => {
  event.preventDefault();

  try {
    await Auth.signIn(this.state.email, this.state.password);
    alert("Logged in");
  } catch (e) {
    alert(e.message);
  }
}
```

We are doing two things of note here.

1. We grab the `email` and `password` from `this.state` and call Amplify's `Auth.signIn()` method with it. This method returns a promise since it will be logging the user asynchronously.

2. We use the `await` keyword to invoke the `Auth.signIn()` method that returns a promise. And we need to label our `handleSubmit` method as `async`.

Now if you try to login using the `admin@example.com` user (that we created in the [Create a Cognito Test User]({{ site.baseurl }}{% link _chapters/create-a-cognito-test-user.md %}) chapter), you should see the browser alert that tells you that the login was successful.

![Login success screenshot]({{ site.baseurl }}/assets/react/login-success.png)

Next, we'll take a look at storing the login state in our app.
