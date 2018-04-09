---
layout: post
title: Create a New React.js App
date: 2018-01-06 00:00:00
description: Create React App helps you build React.js app with no configuration. Install the Create React App CLI using the NPM package and use the command to start a new React.js project.
context: all
comments_id: 29
---

Let's get started with our frontend. We are going to create a single page app using [React.js](https://facebook.github.io/react/). We'll use the [Create React App](https://github.com/facebookincubator/create-react-app) project to set everything up. It is officially supported by the React team and conveniently packages all the dependencies for a React.js project.

### Install Create React App

<img class="code-marker" src="/assets/s.png" />Move out of the directory that we were working in for the backend.

``` bash
$ cd ../
```

<img class="code-marker" src="/assets/s.png" />Create a new project in directory separate from the backend. Run the following command.

``` bash
$ npm install -g create-react-app
```

This installs the Create React App NPM package globally.

### Create a New App

<img class="code-marker" src="/assets/s.png" />From your working directory, run the following command to create the client for our notes app.

``` bash
$ create-react-app dapp-boilerplate
```

This should take a second to run, and it will create your new project and your new working directory.

<img class="code-marker" src="/assets/s.png" />Now let's go into our working directory and run our project.

``` bash
$ cd dapp-boilerplate
$ npm start
```

This should fire up the newly created app in your browser.

![New Create React App screenshot](/assets/react/new-create-react-app.png)

### Change the Title

<img class="code-marker" src="/assets/s.png" />Let's quickly change the title of our note taking app. Open up `public/index.html` and edit the `title` tag to the following:

``` html
<title>Boilerplate for React Ethereum dApps</title>
```

Create React App comes pre-loaded with a pretty convenient yet minimal development environment. It includes live reloading, a testing framework, ES6 support, and [much more](https://github.com/facebookincubator/create-react-app#why-use-this).

Next, we are going to create our app icon and update the favicons.