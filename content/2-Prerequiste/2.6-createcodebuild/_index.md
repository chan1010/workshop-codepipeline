---
title : "Create AWS Codebuild"
date :  "`r Sys.Date()`" 
weight : 6 
chapter : false
pre : " <b> 2.6 </b> "
---

1. Go to [CodeBuild service management console](https://ap-southeast-1.console.aws.amazon.com/ec2/home)

- Click **Build projects**.
- Click **Create build project**.

![CODEBUILD](/images/2.prerequisite/001-createcodebuild.png)

2. Project name, nhập **app_lab_build**

![CODEBUILD](/images/2.prerequisite/002-createcodebuild.png)

3. At the **Source** section
- **Source provider** Click **AWS CodeCommit**.
- **Repository** Click **app_lab**.
- **Reference type** Click **Branch**.
- **Branch** Click **master**.

![CODEBUILD](/images/2.prerequisite/003-createcodebuild.png)

4. At the **Environment** section
- **Environment image** Click **Managed image**.
- **Operating system** Click **Amazon Linux 2**.
- **Runtime(s)** Click **Standar**.
- **Image** Click **aws/codebuild/amazonlinux2-aarch64-standard:2.0**.
- **Image version** Click **Always use the latest image for this runtime version**.
- **Service role** Click **New service role**.

![CODEBUILD](/images/2.prerequisite/004-createcodebuild.png)

5. At the **Buildspec** Click **Use a buildspec file**.

![CODEBUILD](/images/2.prerequisite/005-createcodebuild.png)

6. At the **Artifacts** section.

- **Type** Click **Amazon S3**.
- **Bucket name** Click **app-lab-s3**.
- In the **Name** enter **app_lab**.
- **Artifacts packaging** Click **None**.
- Click **Create build project**

![CODEBUILD](/images/2.prerequisite/004-createcodebuild.png)




