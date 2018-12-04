# https://github.com/serverless/serverless/issues/5558
```
$ sls print
service: sls-5558
provider:
  name: aws
  runtime: nodejs8.10
custom:
  schedules:
    default: rate(60 minutes)
    prod: rate(10 minutes)
functions:
  hello:
    handler: handler.hello
    events:
      - schedule: rate(60 minutes)
```
