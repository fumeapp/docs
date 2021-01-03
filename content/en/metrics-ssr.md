---
title: SSR Metrics
description: 'Application environment metrics for SSR projects'
position: 10
category: 'Metrics'
---

## Invocations

 Invocations (requests) are executed synchronously, the AWS API Gateway invokes Lambda to run the function and waits for a response.

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





