# Solution - Thomas Poignant
Here is my solution to the SRE aircall test.


# Result
The code is deployed on my personal AWS account.

You can upload your image with this command:
```shell
curl -X POST https://2an99qlb8i.execute-api.eu-west-1.amazonaws.com/prod/image \
--form 'file=@filename.jpg' \
--form 's3Key=filename.jpg'
```

It will be available on this S3 bucket : `https://tpoi-aircall-bucket-prod.s3.eu-west-1.amazonaws.com/`.  
In our example it will be available at [https://tpoi-aircall-bucket-prod.s3.eu-west-1.amazonaws.com/filename.jpg](https://tpoi-aircall-bucket-prod.s3.eu-west-1.amazonaws.com/filename.jpg).

# Documentation

## Architecture


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
