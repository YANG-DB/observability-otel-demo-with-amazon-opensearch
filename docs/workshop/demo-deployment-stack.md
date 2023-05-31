## Explore the OTEL Demo Architecture Stack

In this section we will explore our infrastructure in the cloud that has been created. If you're attending AWS hosted event, infrastructure is created in the AWS account for you already. If you are using your own account, we assume you have completed the instructions in Using your[ own AWS account page](https://catalog.us-east-1.prod.workshops.aws/workshops/1abb648b-2ef8-442c-a731-efbcb69c1e1e/en-US/020-getting-started/02-aws-owner-account) to create the required infrastructure.

The infrastructure that has been provisioned includes the following

 - An Virtual Private Cloud (VPC) network and other networking components to secure infrastructure in the cloud.
 - An Amazon OpenSearch Service domain as our data store for observability signals.
 - An Nginx proxy to access OpenSearch dashboards
 - Amazon Elastic Kubernetes cluster where we will deploy our application and signal collectors (OpenTelemetery collector, Fluentbit, and OpenSearch Data Prepper)

1. Navigate to Amazon CloudFormation console and click on 'main' stack. The stack should show 'CREATE_COMPLETE' status.