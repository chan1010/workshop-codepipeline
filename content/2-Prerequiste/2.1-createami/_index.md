---
title : "Create IAM User & Role"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b>2.1 </b> "
---

### Create IAM user

1. Go to [IAM service management console](https://us-east-1.console.aws.amazon.com/iamv2/home)

- Click **Users**.
- Click **Add Users**.

![IAM](/images/2.prerequisite/001-createuser.png)

2. At the **Create User**.

- At the  **User name** điền **user-commit**.
- Click **Provide user access to the AWS Management Console** và Click **I want to create an IAM user**.
- Click **Next**.

![IAM](/images/2.prerequisite/002-createuser.png)

3. At the **Set permissions** page

- At the  **Permissions options** Click **Attach policies directly**
- At the  **Permissions policies** Click  **AWSCodeCommitFullAccess**
- Click **Next**.

![IAM](/images/2.prerequisite/003-createuser.png)

4. At the  **Review and create** page

- Click **Create user**.

![IAM](/images/2.prerequisite/004-createuser.png)

5. At the **Retrieve password** 

- Click **Dowload .csv file**.

![IAM](/images/2.prerequisite/005-createuser.png)

6. Tại **Access keys**

- Click **Create access key**.

![IAM](/images/2.prerequisite/001-createaccesskey.png)

7. At the **Create access key**

- Click **Command Line Interface (CLI)**.
- Click **Next**.

![IAM](/images/2.prerequisite/002-createaccesskey.png)

8. At the **Set description tag - optional**

- Click **Create access key**.

![IAM](/images/2.prerequisite/003-createaccesskey.png)

9. At the **Retrieve access keys**

- Click **Dowload .csv file**.

![IAM](/images/2.prerequisite/004-createaccesskey.png)

### Create Role
#### Create role cho CodeDeploy
1. Go to [IAM service management console](https://us-east-1.console.aws.amazon.com/iamv2/home)

- Click **Role**.
- Click **Create role**.

![IAM](/images/2.prerequisite/001-createiam.png)

2. At the **Create role** mục **Select trusted entity**.

- At the **Trusted entity type** Click **AWS service**.
- At the **Use case** Click **EC2**.
- **Use cases for other AWS services** Click **CodeDeploy**
- Click **Next**.

![IAM](/images/2.prerequisite/002-createiam.png)

3. At the  **Add permissions**.

- Click **AWSCodeDeployRole**.
- Click **Next**.

![IAM](/images/2.prerequisite/003-createiam.png)

4. Section **Name, review and create**.

- At the  **Role name** nhập **CodeDeploy-Role**.

![IAM](/images/2.prerequisite/004-createiam.png)

- Kiêm tra **Add permissions**
- Click **Create role**.

![IAM](/images/2.prerequisite/005-createiam.png)

#### Create role codedeploy cho EC2
1. Go to [giao diện quản trị dịch vụ IAM](https://us-east-1.console.aws.amazon.com/iamv2/home)

- Click **Role**.
- Click **Create role**.

2. At the **Create role** mục **Select trusted entity**.

- At the  **Trusted entity type** Click **AWS service**.
- At the  **Use case** Click **EC2**.
- Click **Next**.

3. At the  **Add permissions**.

- Click **AmazonS3FullAccess, AWSCodeDeployFullAccess**.
- Click **Next**.
4. Mục **Name, review and create**.

- At the  **Role name** nhập **CodeDeploy_Role_EC2**.
- Kiêm tra **Add permissions**
- Click **Create role**.

![IAM](/images/2.prerequisite/009-createiam.png)

