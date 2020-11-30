---
title: Fume Role 
description: 'Details about the Fume Role'
position: 20
category: 'AWS'
---

Fume creates a role `fume-role` when you connect your cloud account. 

Below is the policy `fume-role-policy` fume creates and attaches.

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Action": [
                "iam:*",
                "apigateway:*",
                "cloudfront:*",
                "route53domains:*",
                "route53:*",
                "s3:*",
                "lambda:*",
                "acm:*"
            ],
            "Effect": "Allow",
            "Resource": "*"
        }
    ]
}
```
