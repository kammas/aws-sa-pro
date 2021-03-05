
aws configure --profile cloudguru

# Create AWS Stack
```shell
PROFILE=cloudguru
STACKNAME=AWS
REGION=us-east-1
aws cloudformation deploy \
  --stack-name $STACKNAME \
  --template-file 01_A4L_AWS.yaml \
  --capabilities CAPABILITY_NAMED_IAM \
  --region $REGION \
  --profile $PROFILE
  ```

  # Create ONPREM Stack
```shell
PROFILE=cloudguru
STACKNAME=ONPREM
REGION=us-east-1
aws cloudformation deploy \
  --stack-name $STACKNAME \
  --template-file 02_A4L_ONPREM.yaml \
  --capabilities CAPABILITY_NAMED_IAM \
  --region $REGION \
  --profile $PROFILE
  ```