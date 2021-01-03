---
title: Headless Metrics
description: 'Application environment metrics for headless projects'
position: 11
category: 'Metrics'
---

## Requests
Requests are sent to [AWS CloudFront](https://aws.amazon.com/cloudfront/), a fast content delivery network (CDN) service that caches the deployed version of your project via [S3](https://aws.amazon.com/s3)

## Average Duration

Duration is calculated from the time your code begins executing until it returns or otherwise terminates, rounded up to the nearest 1ms*.

## Estimated Cost

This is an estimate based on the current [pricing listed](https://aws.amazon.com/lambda/pricing/) . The formula is:

```
total_compute_seconds = total_invocations * average_duration * 0.001 (ms to second)
gigabyte_per_second = total_compute_seconds * 0.125
monthly_compute = gigabyte_per_second * 0.0000166667 ( for every gb/s )
monthly_requests = this.total_invocations * 0.0000002
Total Charges = monthly_compute + monthly_requests
```





