---
title: Headless Metrics
description: 'Application environment metrics for headless projects'
position: 11
category: 'Metrics'
---

## Requests
Requests are sent to [AWS CloudFront](https://aws.amazon.com/cloudfront/), a fast content delivery network (CDN) service that caches the deployed version of your project via [S3](https://aws.amazon.com/s3)

## Bytes Downloaded

A total number of bytes sent out to the Internet

## Estimated Cost

This is an estimate based on the current [pricing listed](https://aws.amazon.com/cloudfront/pricing/) . The formula is:

```
request_costs = total_requests / (10000 * 0.01)
bytes_cost = total_bytes / (1e+9 * 0.085)
Total Charges = request_costs + bytes_cost
```

> Estimated Costs do not factor in free tier eligibility or cheaper tier rates





