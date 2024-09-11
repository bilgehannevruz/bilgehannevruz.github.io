# Introduction to Cloud Computing

## Overview
Cloud computing provides on-demand delivery of computing resources over the internet. It allows users to access and use IT resources without owning and managing physical hardware.

## Key Concepts
- **Infrastructure as a Service (IaaS)**: Provides virtualized computing resources over the internet.
- **Platform as a Service (PaaS)**: Provides a platform allowing customers to develop, run, and manage applications.
- **Software as a Service (SaaS)**: Delivers software applications over the internet.

## Benefits
- **Scalability**: Easily scale resources up or down based on demand.
- **Cost Efficiency**: Pay only for the resources you use.
- **Flexibility**: Access resources from anywhere with an internet connection.

## Example: Deploying a Virtual Machine on AWS
Here is an example of how to deploy a virtual machine on AWS using the AWS CLI.

### Prerequisites
- AWS CLI installed and configured with your credentials.

### Commands
1. Create a key pair:
    ```sh
    aws ec2 create-key-pair --key-name MyKeyPair --query 'KeyMaterial' --output text > MyKeyPair.pem
    ```

2. Launch an EC2 instance:
    ```sh
    aws ec2 run-instances --image-id ami-0abcdef1234567890 --count 1 --instance-type t2.micro --key-name MyKeyPair --security-group-ids sg-0123456789abcdef0 --subnet-id subnet-0123456789abcdef0
    ```

## Additional Resources
- [AWS Documentation](https://docs.aws.amazon.com/)
- [Azure Documentation](https://docs.microsoft.com/en-us/azure/)
- [Google Cloud Documentation](https://cloud.google.com/docs)