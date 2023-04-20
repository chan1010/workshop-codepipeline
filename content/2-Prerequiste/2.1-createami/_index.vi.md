---
title : "Tạo IAM user"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b>2.1 </b> "
---

### Tạo IAM user

1. Truy cập [giao diện quản trị dịch vụ IAM](https://us-east-1.console.aws.amazon.com/iamv2/home)

- Chọn **Users**.
- Chọn **Add Users**.

![IAM](/images/2.prerequisite/001-createuser.png)

2. Tại trang **Create User**.

- Tại mục **User name** điền **user-commit**.
- Chọn **Provide user access to the AWS Management Console** và chọn **I want to create an IAM user**.
- Chọn **Next**.

![IAM](/images/2.prerequisite/002-createuser.png)

3. Tại trang **Set permissions**

- Tại mục **Permissions options** chọn **Attach policies directly**
- Tại mục **Permissions policies** chọn  **AWSCodeCommitFullAccess**
- Chọn **Next**.

![IAM](/images/2.prerequisite/003-createuser.png)

4. Tại trang **Review and create**

- Chọn **Create user**.

![IAM](/images/2.prerequisite/004-createuser.png)

5. Tại trang **Retrieve password**

- Chọn **Dowload .csv file**.

![IAM](/images/2.prerequisite/005-createuser.png)

6. Tại **Access keys**

- Chọn **Create access key**.

![IAM](/images/2.prerequisite/001-createaccesskey.png)

7. Tại trang **Create access key**

- Chọn **Command Line Interface (CLI)**.
- Chọn **Next**.

![IAM](/images/2.prerequisite/002-createaccesskey.png)

8. Tại trang **Set description tag - optional**

- Chọn **Create access key**.

![IAM](/images/2.prerequisite/003-createaccesskey.png)

9. Tại trang **Retrieve access keys**

- Chọn **Dowload .csv file**.

![IAM](/images/2.prerequisite/004-createaccesskey.png)

### Tạo Role
#### Tạo role cho codedeploy
1. Truy cập [giao diện quản trị dịch vụ IAM](https://us-east-1.console.aws.amazon.com/iamv2/home)

- Chọn **Role**.
- Chọn **Create role**.

![IAM](/images/2.prerequisite/001-createiam.png)

2. Tại trang **Create role** mục **Select trusted entity**.

- Tại mục **Trusted entity type** chọn **AWS service**.
- Tại mục **Use case** chọn **EC2**.
- **Use cases for other AWS services** chọn **CodeDeploy**
- Chọn **Next**.

![IAM](/images/2.prerequisite/002-createiam.png)

3. Tại mục **Add permissions**.

- Chọn **AWSCodeDeployRole**.
- Chọn **Next**.

![IAM](/images/2.prerequisite/003-createiam.png)

4. Mục **Name, review and create**.

- Tại mục **Role name** nhập **CodeDeploy-Role**.

![IAM](/images/2.prerequisite/004-createiam.png)

- Kiêm tra **Add permissions**
- Chọn **Create role**.

![IAM](/images/2.prerequisite/005-createiam.png)

#### Tạo role codedeploy cho EC2
1. Truy cập [giao diện quản trị dịch vụ IAM](https://us-east-1.console.aws.amazon.com/iamv2/home)

- Chọn **Role**.
- Chọn **Create role**.

2. Tại trang **Create role** mục **Select trusted entity**.

- Tại mục **Trusted entity type** chọn **AWS service**.
- Tại mục **Use case** chọn **EC2**.
- Chọn **Next**.

3. Tại mục **Add permissions**.

- Chọn **AmazonS3FullAccess, AWSCodeDeployFullAccess**.
- Chọn **Next**.
4. Mục **Name, review and create**.

- Tại mục **Role name** nhập **CodeDeploy_Role_EC2**.
- Kiêm tra **Add permissions**
- Chọn **Create role**.

![IAM](/images/2.prerequisite/009-createiam.png)

