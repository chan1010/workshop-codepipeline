---
title : "Clean up resources"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 4. </b> "
---

We will proceed with the following steps to delete the resources we have created in this hands-on:

#### EC2 Instance

1. Go to [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)
- Click **Instances**.
- Click instance **Linux Instance**.
- Click **Instance state**.
- Click **Terminate instance**, after then Click **Terminate** confirm.

![CLEAR](/images/4.clean/001-clean.png)

#### CodePipeline
1. Go to [CodePipeline service management console](https://ap-southeast-1.console.aws.amazon.com/codesuite/codepipeline/pipelines)
- Click **pipeline**
- Click pipeline **app_lab_pipeline**
- Click **Delete pipeline**.

![CLEAR](/images/4.clean/002-clean.png)

2. At the input confirm, enter **delete**, Click **Delete** to perform delete.

#### CodeDeploy
1. Go to [CodeDeploy service management console](https://ap-southeast-1.console.aws.amazon.com/codesuite/codedeploy/applications)
- Click **Applications**
- Go to application **codedeploy_app_lab**
- Click **Delete application**.

![CLEAR](/images/4.clean/003-clean.png)

2. At the input confirm, enter **delete**, Click **Delete** to perform delete.
#### CodeBuild
1. Go to [CodeBuild service management console](https://ap-southeast-1.console.aws.amazon.com/codesuite/codebuild/start)
- Click **Build projects**
- Click **app_lab_build**
- Click **Delete build project**.

![CLEAR](/images/4.clean/004-clean.png)

2. At the input confirm, enter **delete**, Click **Delete** to perform delete.

#### CodeCommit
1. Go to [CodeCommit service management console](https://ap-southeast-1.console.aws.amazon.com/codesuite/codecommit/repositories)
- Click **repositories**
- Click repository **app_lab**
- Click **Delete repository**.

![CLEAR](/images/4.clean/005-clean.png)

2. At the input confirm, enter **delete**, Click **Delete** to perform delete.

#### S3
1. Go to [S3 service management console](https://s3.console.aws.amazon.com/s3/buckets)
- Click **Buckets**
- Click buckets được sinh ra
- Click **Delete**.

![CLEAR](/images/4.clean/006-clean.png)

2. At the input confirm, enter name **bucket**, Click **Delete bucket** to perform delete.

#### IAM

1. Go to [IAM service management console](https://console.aws.amazon.com/iamv2/home#/home)
- Click **Roles**.
- Click **AWSCodePipelineServiceRole-ap-southeast-1-app_lab_pipeline, CodeDeploy-Role-EC2** và **CodeDeploy-Role**.
- Click **Delete**

![CLEAR](/images/4.clean/007-clean.png)

2. Click **Users**.
- Click user **user-commit**.
- Click **Delete**, sau đó enter tên user **user-commit** và Click **Delete** để xóa user.

![CLEAR](/images/4.clean/008-clean.png)

#### Xóa Keypair
1. Go to [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)
- Click **Key Pairs**
- Click **Actions**
- Click **Delete**

![CLEAR](/images/4.clean/009-clean.png)

#### Xóa VPC
1. Go to vào [VPC service management console](https://console.aws.amazon.com/vpc/home)
- Click **Your VPCs**.
- Click **VPC_CodePipeline**.
- Click **Actions**.
- Click **Delete VPC**.
![CLEAR](/images/4.clean/010-clean.png)
2. At the input confirm, enter **delete**, Click **Delete** to perform delete **VPC_CodePipeline** and related resources.

