# YouFrame backend api

Follow bellow instructions for setting up YouFrame backend api. Installing nodejs and npm is basic prerequisite.

- install aws cli in your system from this [website (click here)](https://aws.amazon.com/cli/).

# create AWS IAM user and configure it.

- create aws IAM user role of name 'demo-user' and give admin privelleges or specific resource privellegs to use lambda, s3, and dynamodb.
- run following command in terminal.

```
aws configure --profile demo-user
```

- enter credentials of 'demo-user' profile which aws provides.
- credentials includes access key id, secrete access key, region: ap-south-1, and then last yaml

# install serverless package

- install serverless globally using bellow command

```
npm i -g serverless
```

# deploy to aws

```
sls deploy -v
```

Api endpoint will be show in terminal. Copy that url and replace it with value of REACT_APP_API_URL in .env of frontend.

- check logs

```
sls logs -f app -t
```