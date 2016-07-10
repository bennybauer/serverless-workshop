# Serverless Workshop
***Work in Progress***

## Goal
Create a Slack slash command that will return a stock price. The implementation will be based on using **Function as a Service** with the help of the **Serverless Framework**. Language used is node.js.

## Background 
#### Function as a Service
Running server-side logic on a stateless compute containers that are event-triggered, ephemeral (may only last for one invocation), and fully managed by a 3rd party. 

[Read more here](http://martinfowler.com/articles/serverless.html)

#### Serverless Framework
The Serverless Framework is an application framework for building web, mobile and IoT applications powered by **AWS Lambda**, AWS API Gateway and in the future other Function as a Service providers. 

[Read more here](https://github.com/serverless/serverless).

#### AWS Lambda
AWS Lambda is a compute service where you can upload your code to AWS Lambda and the service can run the code on your behalf using AWS infrastructure.

[Read more here](https://aws.amazon.com/lambda/).

## Let's do it!
1. Make sure you have an AWS access key & secret with admin permissions.
2. Follow the Serverless Framework [guide](https://github.com/serverless/serverless/tree/v1.0/docs/guide):
	1. [Installation](https://github.com/serverless/serverless/blob/v1.0/docs/guide/installation.md)
	2. [Setting an AWS profile](https://github.com/serverless/serverless/blob/v1.0/docs/guide/provider-account-setup.md#setting-a-default-aws-profile)
	3. [Creating a service](https://github.com/serverless/serverless/blob/v1.0/docs/guide/creating-a-service.md)
	4. [Creating a http endpoint for function](https://github.com/serverless/serverless/blob/v1.0/docs/guide/overview-of-event-sources.md#http-endpoint)
	5. [Deploying a service](https://github.com/serverless/serverless/blob/v1.0/docs/guide/deploying-a-service.md)
	6. [Invoking a function](https://github.com/serverless/serverless/blob/v1.0/docs/guide/invoking-a-function.md)

3. Add Slack [slash command](https://api.slack.com/slash-commands) that will receive a stock ticker (e.g. ADSK) and will send a `GET` request to your FaaS endpoint, passing the ticker as a query param. Make sure to create a *unique* command name.
4. Your function will: 
	5. Read the ticker argument
	6. Call `http://www.google.com/finance/info?q=NASDAQ:ticker` and parse the response
	7. Return the stock price to the slack command

For example:

**TODO: screenshot**

## Good Reads
- [Serverless resources](https://github.com/bennybauer/Serverless-Resources)
