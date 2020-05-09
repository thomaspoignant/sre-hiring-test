# Solution - Thomas Poignant
Here is my solution to the SRE aircall test.


## Prerequisite
Before deploying the project you should have `docker` and set up your AWS credentials.

## Infra as code
The infrastructure as code of this app is build with the [`serverless` framework](https://www.serverless.com/).
The configuration is available in the [serverless.yml](serverless.yml) file.

## Build the app
This AWS lambda is build in a docker image.
To build the image you can run 
```shell
npm run docker:build
```

We also use the image to deploy the infra-structure
```shell
npm run serverless:deploy
```

If you want to build and deploy at the same time, just run `npm run deploy` like you was doing before.




- use serverless
- use docker for the build
- use docker for the deployment


-> logs --> cloudwatch






[![Build Status](https://travis-ci.com/thomaspoignant/sre-hiring-test.svg?branch=master)](https://travis-ci.com/thomaspoignant/sre-hiring-test)
