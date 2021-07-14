---
title: Provisioned Concurrency
description: 'For Lambda Functions'
position: 22
category: 'AWS'
---

By default, when an environment is deployed, the first request it receives may encounter "cold starts". These requests typically incur a penalty of a few seconds while AWS loads a serverless container to serve the request. Once a request has been served by that container, it is typically kept warm to serve further requests with no delay.

To mitigate this issue, Amazon supports "provisioned concurrency". When using this feature, the requested number of execution environments / containers will be provisioned and kept "warm" for you automatically, allowing them to immediately serve any incoming requests. To enable this feature, visit the `Settings` page of the environment you want to configure and set the `Capacity` to a value larger than zero.


<alert type="warning">

Increasing your provisioned concurrency capacity past zero will [effect pricing](https://aws.amazon.com/lambda/pricing/#Provisioned_Concurrency_Pricing)

</alert>


<alert type="info">
Setting your capacity to zero will remove any existing provisioned concurrency
</alert>
