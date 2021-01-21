---
title: Reserved Variables
description: 'Lambdas reserved environment variables'
position: 21
category: 'AWS'
---

## Lambdas reserved environment variables
Lambda runtimes set several environment variables during initialization.
The keys for these environment variables are reserved and **cannot** be set in your function configuration.

* `_HANDLER` – The handler location configured on the function.
* `_X_AMZN_TRACE_ID` – The X-Ray tracing header.
* `AWS_REGION` – The AWS Region where the Lambda function is executed.
* `AWS_EXECUTION_ENV` – The runtime identifier, prefixed by AWS_Lambda_—for example, AWS_Lambda_java8.
* `AWS_LAMBDA_FUNCTION_NAME` – The name of the function.
* `AWS_LAMBDA_FUNCTION_MEMORY_SIZE` – The amount of memory available to the function in MB.
* `AWS_LAMBDA_FUNCTION_VERSION` – The version of the function being executed.
* `AWS_LAMBDA_INITIALIZATION_TYPE` – The initialization type of the function, which is either on-demand or provisioned-concurrency. For information, see Configuring provisioned concurrency.
* `AWS_LAMBDA_LOG_GROUP_NAME` , `AWS_LAMBDA_LOG_STREAM_NAME` – The name of the Amazon CloudWatch Logs group and stream for the function.
* `AWS_ACCESS_KEY_ID` , `AWS_SECRET_ACCESS_KEY`, `AWS_SESSION_TOKEN` – The access keys obtained from the function's execution role.
* `AWS_LAMBDA_RUNTIME_API` – (Custom runtime) The host and port of the runtime API.
* `LAMBDA_TASK_ROOT` – The path to your Lambda function code.
* `LAMBDA_RUNTIME_DIR` – The path to runtime libraries.
* `TZ` – The environment's time zone (UTC). The execution environment uses NTP to synchronize the system clock.

## More info
More information about Lambda environment variables found [here](https://docs.aws.amazon.com/lambda/latest/dg/configuration-envvars.html).
