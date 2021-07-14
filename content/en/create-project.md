---
title: Create a Project
description: 'Create your first project'
position: 4
category: 'Guide'
---

Once your team and AWS account are created you're ready to [create a project](https://fume.app/project/create).  

### Name and Logo
Choose a project name and optional logo, make sure the correct team has been selected.

<alert type="warning">

You will not be able to rename your project, you may delete and re-add it.

</alert>


### Connected AWS Account
Choose the cloud account you want this project deployed to

### Framework
Choose either a [NuxtJS](https://nuxtjs.org) or [NestJS](https://nestjs.com) framework
* NuxtJS projects can be either SSR or Static
* NestJS projects require SSR by default

### Project Structure (NuxtJS only)
Choose either SSR functionality or Headless.
* SSR structures will be deployed to a Lambda Function backed by an Api Gateway.
  * You will be able to turn on caching later based on the environment.
* Headless structures deploy to S3 buckets backed by CloudFront.

### Repository
Providing a repository will help Fume:
* Link to the commits related to your deployments on the web app.
* Link the related commits and branches in the webhook payload.


### Environments 
We will start you off with two standard environments, but feel free to customize that here

<alert type="success">
You will be able to add and remove environments at any time
</alert>


