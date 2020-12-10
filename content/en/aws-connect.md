---
title: Connect to AWS 
description: 'Connecting to your AWS Account'
position: 3
category: 'Guide'
---


AWS Accounts are associated with teams.

* Fume requires a temporary user with IAM access to create the <a class="text-indigo-600 hover:text-indigo-700" href="https:///docs.fume.app/fume-role" target="_new">fume role</a>
* You can use [this link](https://console.aws.amazon.com/iam/home#/users$new?step=review&accessKey&userNames=fume-temp-user&permissionType=policies&policies=arn:aws:iam::aws:policy%2FIAMFullAccess) to help create your credentials.
* Create the user and then copy the Access Key ID and Secret Access Key.
* You may delete the user after you have linked the account.

<alert type="info">

These credentials will __not__ be stored and can be deleted immediately after.

</alert>
