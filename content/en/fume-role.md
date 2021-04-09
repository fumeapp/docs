---
title: Fume Role 
description: 'Details about the Fume Role'
position: 20
category: 'AWS'
---

Fume creates a role `fume-role` when you connect your cloud account.


Below are the permissions for the `fume-role-policy`.

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Action": [
                "iam:*",
                "apigateway:*",
                "cloudfront:*",
                "cloudwatch:*",
                "logs:*",
                "route53domains:*",
                "route53:*",
                "s3:*",
                "lambda:*",
                "ecr:*",
                "ecr-public:*",
                "acm:*"
            ],
            "Effect": "Allow",
            "Resource": "*"
        }
    ]
}
```

Below are the trust relationships

```json
{
    "Version": "2012-10-17",
        "Statement": [
        {
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:iam::751311555268:root"
            },
            "Action": "sts:AssumeRole"
        },
        {
            "Effect": "Allow",
            "Principal": {
                "Service": "apigateway.amazonaws.com"
            },
            "Action": "sts:AssumeRole"
        },
        {
            "Effect": "Allow",
            "Principal": {
                "Service": "lambda.amazonaws.com"
            },
            "Action": "sts:AssumeRole"
        },
        {
            "Effect": "Allow",
            "Principal": {
                "Service": "datasync.amazonaws.com"
            },
            "Action": "sts:AssumeRole"
        }
    ]
}
```

You may view this role, its policy, and trust in your account [here](https://console.aws.amazon.com/iam/home?region=us-east-1#/roles/fume-role)
