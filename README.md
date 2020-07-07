# high-availability-webapp

Deployment

Run the following commands to deploy the web app. AWS CLI has to be congifgured before this will work. For more info on configuring AWS CLI please see https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html. Wait until the network stack is complete before deploying the webapp.

<code> aws cloudformation create-stack --stack-name network --template-body file://network.yml --parameters file://network-params.json --region=us-east-1 --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" </code>

<code> aws cloudformation create-stack --stack-name webapp --template-body file://webapp.yml --parameters file://parameters.json --region=us-east-1 --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" </code>