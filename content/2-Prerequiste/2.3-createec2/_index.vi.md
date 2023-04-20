---
title: "Tạo EC2"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 2.3 </b> "
---

### Create EC2

1. Truy cập [giao diện quản trị dịch vụ EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/home)

- Chọn **Instances**.
- Chọn **Launch instances**.

![EC2](/images/2.prerequisite/001-createec2.png)

2. Name and tags của instance, nhập **Linux Instance**

![EC2](/images/2.prerequisite/002-createec2.png)

3. Tại mục **Amazon Machine Image (AMI)**

- Chọn **Quick Start**.
- Chọn **Amazon Linux**.
- Chọn **Amazon Linux 2 AMI**.

![EC2](/images/2.prerequisite/003-createec2.png)

4. Chọn **Instance type** chọn **t2.micro**.

![EC2](/images/2.prerequisite/004-createec2.png)

5. Tại mục **Key pair** chọn **Create new key pair**.

![EC2](/images/2.prerequisite/001-createkeypair.png)

6. Trong giao diện Cretae key pair.

- Key pair name, nhập **lab-codepipeline**.
- Key pair type, **chọn RSA**
- Private key file format, chọn **.pem**

![EC2](/images/2.prerequisite/002-createkeypair.png) 7. Thực hiện cấu hình Network

- VPC, chọn **VPC_CodePipeline**
- Subnet, chọn **Public Subnet**
- Auto-assign public IP, chọn **Enable**
- Firewall (Security Group), chọn **Select existing security group**
- Chọn VPC_CodePipeline_SG
- Chọn Launch instance

![EC2](/images/2.prerequisite/005-createec2.png)

8. Thực hiện kết nối với EC2 với MobaXterm hoặc putty

![EC2](/images/2.prerequisite/001-connectec2.png)

### Update IAM Role

1. Truy cập [giao diện quản trị dịch vụ EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/home)

- Chọn **Instances**.
- Chọn **Linux Instance**.
- Chọn **Actions**
- Chọn **Security**
- Chọn **Modify IAM role**
  ![EC2](/images/2.prerequisite/001-updateiamec2.png)

2. Tại trang **Modify IAM role**

- **IAM role** chọn **CodeDeploy_Role_EC2**
- Chọn **Update IAM role**
  ![EC2](/images/2.prerequisite/002-updateiamec2.png)
