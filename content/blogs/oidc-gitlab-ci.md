---
title: "OIDC authentication within Gitlab CI pipelines"
date: 2024-09-01T22:53:58+05:30
draft: false
github_link: "#"
author: "juanmiguel.rua"
tags:
  - OIDC
  - Gitlab CI
  - Terraform
  - AWS
image: /images/blog/post.jpg
description: ""
toc: 
---

Because the sucurity is quite important. :zap:

## OIDC authentication within Gitlab CI pipelines

When there are multiple teams working on different projects that need to be deployed in different accounts or regions,
it is important to have a secure way to authenticate with the cloud provider.

Using a single user account to authenticate with Gitlab CI is not a good practice for many reasons. One of the reasons is that the user account can be compromised and the attacker can have access to all the projects that the user has access to. Another reason is that the user account can be locked out or disabled, which will prevent the CI/CD pipeline from running.

The [OpenID Connect](https://openid.net/connect/) (OIDC) is a simple identity layer on top of the OAuth 2.0 protocol. It allows clients to verify the identity of the end-user based on the authentication performed by an authorization server, as well as to obtain basic profile information about the end-user in an interoperable and REST-like manner.

### What is Gitlab CI?

GitLab CI/CD is a tool built into GitLab for software development through the continuous methodologies: Continuous Integration (CI) and Continuous Deployment (CD). CI/CD is a method to frequently deliver apps to customers by introducing automation into the stages of app development. The main concepts attributed to these practices are continuous integration, continuous delivery, and continuous deployment.

### What is Terraform?
