---
title: "Create AWS EC2"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 2.3 </b> "
---

### Create EC2

1. Go to [EC2 service management console](https://ap-southeast-1.console.aws.amazon.com/ec2/home)

- Click **Instances**.
- Click **Launch instances**.

![EC2](/images/2.prerequisite/001-createec2.png)

2. In the name and tags of instance, enter **Linux Instance**

![EC2](/images/2.prerequisite/002-createec2.png)

3. At the **Amazon Machine Image (AMI)** section

- Click **Quick Start**.
- Click **Amazon Linux**.
- Click **Amazon Linux 2 AMI**.

![EC2](/images/2.prerequisite/003-createec2.png)

4. Click **Instance type** Click **t2.micro**.

![EC2](/images/2.prerequisite/004-createec2.png)

5. At the **Key pair** section Click **Create new key pair**.

![EC2](/images/2.prerequisite/001-createkeypair.png)

6. At the **Create key pair** page.

- Key pair name, enter **lab-codepipeline**.
- Key pair type, **Click RSA**
- Private key file format, Click **.pem**

![EC2](/images/2.prerequisite/002-createkeypair.png) 7. Thực hiện cấu hình Network

- VPC, Click **VPC_CodePipeline**
- Subnet, Click **Public Subnet**
- Auto-assign public IP, Click **Enable**
- Firewall (Security Group), Click **Select existing security group**
- Click VPC_CodePipeline_SG
- Click Launch instance

![EC2](/images/2.prerequisite/005-createec2.png)

8. Make a connection to EC2 with MobaXterm or putty

![EC2](/images/2.prerequisite/001-connectec2.png)

### Update IAM Role

1. Go to [EC2 service management console](https://ap-southeast-1.console.aws.amazon.com/ec2/home)

- Click **Instances**.
- Click **Linux Instance**.
- Click **Actions**
- Click **Security**
- Click **Modify IAM role**
  ![EC2](/images/2.prerequisite/001-updateiamec2.png)

2. At the **Modify IAM role** page

- **IAM role** Click **CodeDeploy_Role_EC2**
- Click **Update IAM role**
  ![EC2](/images/2.prerequisite/002-updateiamec2.png)
