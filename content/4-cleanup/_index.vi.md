---
title : "Dọn dẹp tài nguyên"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 4. </b> "
---

Chúng ta sẽ tiến hành các bước sau để xóa các tài nguyên chúng ta đã tạo trong bài thực hành này.

#### EC2 Instance

1. Truy cập [giao diện quản trị dịch vụ EC2](https://console.aws.amazon.com/ec2/v2/home)
- Chọn **Instances**.
- Chọn instance **Linux Instance**.
- Chọn **Instance state**.
- Chọn **Terminate instance**, sau đó Chọn **Terminate** để xác nhận.

![CLEAR](/images/4.clean/001-clean.png)

#### CodePipeline
1. Truy cập [giao diện quản trị dịch vụ CodePipeline](https://ap-southeast-1.console.aws.amazon.com/codesuite/codepipeline/pipelines)
- Chọn **pipeline**
- Chọn pipeline **app_lab_pipeline**
- Chọn **Delete pipeline**.

![CLEAR](/images/4.clean/002-clean.png)

2. Tại ô confirm, điền **delete** để xác nhận, Chọn **Delete** để thực hiện xóa.

#### CodeDeploy
1. Truy cập [giao diện quản trị dịch vụ CodeDeploy](https://ap-southeast-1.console.aws.amazon.com/codesuite/codedeploy/applications)
- Chọn **Applications**
- Truy cập application **codedeploy_app_lab**
- Chọn **Delete application**.

![CLEAR](/images/4.clean/003-clean.png)

2. Tại ô confirm, điền **delete** để xác nhận, Chọn **Delete** để thực hiện xóa.
#### CodeBuild
1. Truy cập [giao diện quản trị dịch vụ CodeBuild](https://ap-southeast-1.console.aws.amazon.com/codesuite/codebuild/start)
- Chọn **Build projects**
- Chọn **app_lab_build**
- Chọn **Delete build project**.

![CLEAR](/images/4.clean/004-clean.png)

2. Tại ô confirm, điền **delete** để xác nhận, Chọn **Delete** để thực hiện xóa.

#### CodeCommit
1. Truy cập [giao diện quản trị dịch vụ CodeCommit](https://ap-southeast-1.console.aws.amazon.com/codesuite/codecommit/repositories)
- Chọn **repositories**
- Chọn repository **app_lab**
- Chọn **Delete repository**.

![CLEAR](/images/4.clean/005-clean.png)

2. Tại ô confirm, điền **delete** để xác nhận, Chọn **Delete** để thực hiện xóa.

#### S3
1. Truy cập [giao diện quản trị dịch vụ S3](https://s3.console.aws.amazon.com/s3/buckets)
- Chọn **Buckets**
- Chọn buckets được sinh ra
- Chọn **Delete**.

![CLEAR](/images/4.clean/006-clean.png)

2. Tại ô confirm, điền name **bucket** để xác nhận, Chọn **Delete bucket** để thực hiện xóa.

#### IAM

1. Truy cập [giao diện quản trị dịch vụ IAM](https://console.aws.amazon.com/iamv2/home#/home)
- Chọn **Roles**.
- Chọn **AWSCodePipelineServiceRole-ap-southeast-1-app_lab_pipeline, CodeDeploy-Role-EC2** và **CodeDeploy-Role**.
- Chọn **Delete**

![CLEAR](/images/4.clean/007-clean.png)

2. Chọn **Users**.
- Chọn user **user-commit**.
- Chọn **Delete**, sau đó điền tên user **user-commit** và Chọn **Delete** để xóa user.

![CLEAR](/images/4.clean/008-clean.png)

#### Xóa Keypair
1. Truy cập [giao diện quản trị dịch vụ EC2](https://console.aws.amazon.com/ec2/v2/home)
- Chọn **Key Pairs**
- Chọn **Actions**
- Chọn **Delete**

![CLEAR](/images/4.clean/009-clean.png)

#### Xóa VPC
1. Truy cập vào [giao diện quản trị dịch vụ VPC](https://console.aws.amazon.com/vpc/home)
- Chọn **Your VPCs**.
- Chọn **VPC_CodePipeline**.
- Chọn **Actions**.
- Chọn **Delete VPC**.
![CLEAR](/images/4.clean/010-clean.png)
2. Tại ô confirm, điền **delete** để xác nhận, Chọn **Delete** để thực hiện xóa **VPC_CodePipeline** và các tài nguyên liên quan.

