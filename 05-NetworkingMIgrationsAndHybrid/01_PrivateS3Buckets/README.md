
aws configure --profile cloudguru

# Create Main Stack
```shell
PROFILE=cloudguru
STACKNAME=mystack02
REGION=us-east-1
aws cloudformation deploy \
  --stack-name $STACKNAME \
  --template-file 01_A4L_privatevpc.yaml \
  --capabilities CAPABILITY_NAMED_IAM \
  --region $REGION \
  --profile $PROFILE
  ```