# Day 6: AWS Basics – IAM, EC2, S3, VPC

## 📌 Overview
Today, I focused on **AWS Basics**, covering fundamental services essential for DevOps:
- **IAM (Identity and Access Management)**: User access control
- **EC2 (Elastic Compute Cloud)**: Virtual servers
- **S3 (Simple Storage Service)**: Object storage
- **VPC (Virtual Private Cloud)**: Network isolation in AWS

## 🔹 IAM (Identity and Access Management)
### **Concepts:**
- **Users**: Individual AWS accounts
- **Groups**: Collection of users with similar permissions
- **Roles**: Temporary permissions assigned to AWS services
- **Policies**: JSON-based permission rules

### **Hands-on Tasks:**
✅ Created an IAM user and assigned policies
✅ Attached AdministratorAccess policy to a user
✅ Explored AWS IAM console and policy simulator

### **AWS CLI Commands:**
```sh
# Create an IAM user
aws iam create-user --user-name DevOpsUser

# Attach a policy to the user
aws iam attach-user-policy --user-name DevOpsUser --policy-arn arn:aws:iam::aws:policy/AdministratorAccess

# List IAM users
aws iam list-users
```

---
## 🚀 EC2 (Elastic Compute Cloud)
### **Concepts:**
- **Instance Types**: General-purpose, compute-optimized, memory-optimized, etc.
- **Security Groups**: Firewall rules controlling traffic
- **Elastic IPs**: Static IPs for instances
- **EBS (Elastic Block Store)**: Persistent storage for EC2

### **Hands-on Tasks:**
✅ Launched a t2.micro EC2 instance using AWS CLI
✅ Connected to the instance via SSH
✅ Created a Security Group and allowed SSH (port 22)

### **AWS CLI Commands:**
```sh
# Launch an EC2 instance
aws ec2 run-instances --image-id ami-0abcdef1234567890 --count 1 --instance-type t2.micro --key-name MyKeyPair --security-groups MySecurityGroup

# Describe EC2 instances
aws ec2 describe-instances --query "Reservations[*].Instances[*].[InstanceId,State.Name,PublicIpAddress]"

# Terminate an EC2 instance
aws ec2 terminate-instances --instance-ids i-1234567890abcdef0
```

---
## 📦 S3 (Simple Storage Service)
### **Concepts:**
- **Buckets**: Containers for storing objects
- **Objects**: Files stored in S3
- **Storage Classes**: Standard, IA (Infrequent Access), Glacier
- **Versioning**: Track object modifications

### **Hands-on Tasks:**
✅ Created an S3 bucket
✅ Uploaded files and enabled versioning
✅ Configured public access settings

### **AWS CLI Commands:**
```sh
# Create an S3 bucket
aws s3 mb s3://my-devops-bucket

# Upload a file to S3
aws s3 cp myfile.txt s3://my-devops-bucket/

# List S3 buckets
aws s3 ls
```

---
## 🌐 VPC (Virtual Private Cloud)
### **Concepts:**
- **Subnets**: Public and private sub-networks
- **Route Tables**: Defines network traffic flow
- **Internet Gateway**: Provides internet access
- **NAT Gateway**: Allows private instances to access the internet

### **Hands-on Tasks:**
✅ Created a custom VPC
✅ Launched EC2 instances inside private and public subnets
✅ Configured an Internet Gateway

### **AWS CLI Commands:**
```sh
# Create a VPC
aws ec2 create-vpc --cidr-block 10.0.0.0/16

# List available VPCs
aws ec2 describe-vpcs --query "Vpcs[*].VpcId"
```

---
## 🛠 Additional Hands-on Challenges
🔹 Create an IAM role and assign it to an EC2 instance
🔹 Enable S3 bucket encryption using AWS CLI
🔹 Set up a VPC with multiple subnets and a NAT gateway

---
## 🔗 References
- [AWS IAM Documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/)
- [AWS EC2 Documentation](https://docs.aws.amazon.com/ec2/)
- [AWS S3 Documentation](https://docs.aws.amazon.com/s3/)
- [AWS VPC Documentation](https://docs.aws.amazon.com/vpc/)

---
🔗 **GitHub Repository**: [https://github.com/someshwarborse/100-Days-of-DevOps](https://github.com/someshwarborse/100-Days-of-DevOps)
