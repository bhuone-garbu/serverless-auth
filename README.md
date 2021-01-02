# Simple serverless auth service using Auth0

### 0. Prerequisites

Install `serverless` framework if you haven't

```sh
npm install -g serverless
```

Create a free developer account with [Auth0](https://auth0.com/) and setup an application. (A new tenant environment if u need to)

### 1. Install dependencies

```sh
npm install
```

### 2. Create `secret.pem` file

This file will contain your Auth0 public certificate, used to verify tokens.

Create a `secret.pem` file in the root folder of this project. Simply paste your public certificate in there from Auth0.

### 3. Deploy the stack

We need to deploy the stack in order to consume the private/public testing endpoints.

```sh
sls deploy -v
```

### 4. Final test

To make sure everything works, send a POST request (using curl, Postman etc.) to your private endpoint.

You can grab a test token from Auth0. Make sure to provide your token in the headers like so:

```
"Authorization": "Bearer YOUR_TOKEN"
```

And should be golden!!! 😎

To use the authorizer reference it on your existing aws lambda function or public AWS API gateway.
