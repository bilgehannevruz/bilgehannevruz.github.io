# AWS (Amazon Web Services)

## Overview
Amazon Web Services (AWS) is a comprehensive and widely adopted cloud platform, offering over 200 fully featured services from data centers globally. AWS provides a variety of services including computing power, storage options, and networking capabilities.

## Key Services
- **EC2 (Elastic Compute Cloud)**: Provides scalable computing capacity in the cloud.
- **S3 (Simple Storage Service)**: Object storage service that offers industry-leading scalability, data availability, security, and performance.
- **RDS (Relational Database Service)**: Makes it easy to set up, operate, and scale a relational database in the cloud.

## Example: Launching an EC2 Instance
Here is an example of how to launch an EC2 instance using the AWS CLI.

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

3. Describe the instance to get its public IP:
    ```sh
    aws ec2 describe-instances --instance-ids i-0123456789abcdef0 --query 'Reservations[*].Instances[*].PublicIpAddress' --output text
    ```

## Additional Resources
- [AWS EC2 Documentation](https://docs.aws.amazon.com/ec2/)
- [AWS S3 Documentation](https://docs.aws.amazon.com/s3/)
- [AWS RDS Documentation](https://docs.aws.amazon.com/rds/)