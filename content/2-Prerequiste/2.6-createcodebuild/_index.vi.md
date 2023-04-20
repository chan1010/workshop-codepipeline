---
title : "Tạo Codebuild"
date :  "`r Sys.Date()`" 
weight : 6 
chapter : false
pre : " <b> 2.6 </b> "
---

1. Truy cập [giao diện quản trị dịch vụ CodeBuild](https://ap-southeast-1.console.aws.amazon.com/ec2/home)

- Chọn **Build projects**.
- Chọn **Create build project**.

![CODEBUILD](/images/2.prerequisite/001-createcodebuild.png)

2. Project name, nhập **app_lab_build**

![CODEBUILD](/images/2.prerequisite/002-createcodebuild.png)

3. Tại mục **Source**
- **Source provider** chọn **AWS CodeCommit**.
- **Repository** chọn **app_lab**.
- **Reference type** chọn **Branch**.
- **Branch** chọn **master**.

![CODEBUILD](/images/2.prerequisite/003-createcodebuild.png)

4. Tại mục **Environment**.
- **Environment image** chọn **Managed image**.
- **Operating system** chọn **Amazon Linux 2**.
- **Runtime(s)** chọn **Standar**.
- **Image** chọn **aws/codebuild/amazonlinux2-aarch64-standard:2.0**.
- **Image version** chọn **Always use the latest image for this runtime version**.
- **Service role** chọn **New service role**.

![CODEBUILD](/images/2.prerequisite/004-createcodebuild.png)

5. Tại mục **Buildspec** chọn **Use a buildspec file**.

![CODEBUILD](/images/2.prerequisite/005-createcodebuild.png)

6. Tại mục **Artifacts**.

- **Type** chọn **Amazon S3**.
- **Bucket name** chọn **app-lab-s3**.
- **Name** nhập **app_lab**.
- **Artifacts packaging** chọn **None**.
- Chọn **Create build project**

![CODEBUILD](/images/2.prerequisite/004-createcodebuild.png)




