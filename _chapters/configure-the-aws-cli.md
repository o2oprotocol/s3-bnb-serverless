---
layout: post
title: Configure the AWS CLI
date: 2018-03-26 00:00:00
description: To interact with AWS using the command line we need to install the AWS command line interface (or AWS CLI). It also needs to be configured with our IAM user Access key ID and Secret Access key from the AWS console.
context: all
comments_id: 14
---

To make it easier to work with a lot of the AWS services, we are going to use the [AWS CLI](https://aws.amazon.com/cli/).

### Install the AWS CLI

AWS CLI needs Python 2 version 2.6.5+ or Python 3 version 3.3+ and [Pip](https://pypi.python.org/pypi/pip). 

``` bash
apt-get update                     &&
apt-get install --yes python       &&
apt-get install --yes python-pip   &&
python --version     			         &&
pip --version
```

<img class="code-marker" src="/assets/s.png" />Now using Pip you can install the AWS CLI (on Linux, macOS, or Unix) by running:

``` bash
// $ sudo pip install awscli
$ export LC_ALL=C  &&  pip install awscli --upgrade --user

// MacOS: 
$ brew install awscli
```

If you are having some problems installing the AWS CLI or need Windows install instructions, refer to the [complete install instructions](http://docs.aws.amazon.com/cli/latest/userguide/installing.html).

### Add Your Access Key to AWS CLI

We now need to tell the AWS CLI to use your Access Keys from the previous chapter.

It should look something like this:

- Access key ID **AKIAIOSFODNN7EXAMPLE**
- Secret access key **wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY**

<img class="code-marker" src="/assets/s.png" />Simply run the following with your Secret Key ID and your Access Key.

``` bash
$ aws configure
```

You can leave the **Default region name** and **Default output format** the way they are.

Next let's get started with setting up our backend.
