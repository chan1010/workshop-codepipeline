---
title: "Tạo Một pipeline"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 3.1 </b> "
---

### Tạo Pipeline

1. Truy cập [CodePipeline service management console](https://ap-southeast-1.console.aws.amazon.com/codesuite/codepipeline/pipelines)

- Chọn **Pipelines**
- Chọn **Create pipeline**

![CODEPIPELINE](/images/3.createpipeline/001-createpipeline.png)

2. Trong giao diện **Create pipeline**

- **Pipepline name** nhập **app_lab_pipeline**
- **Service role** chọn **New service role**
- Chọn **Next**

![CODEPIPELINE](/images/3.createpipeline/002-createpipeline.png)

3. Trong giao diện **Add source stage**

- **Source provider** chọn **app_lab_pipeline**
- **Repository name** chọn **app_lab**
- **Branch name** chọn **master**
- **Change detection options** chọn **AWS CodePipeline**
- Chọn **Next**

![CODEPIPELINE](/images/3.createpipeline/003-createpipeline.png)

4. Trong giao diện **Add build stage**

- **Build provider** chọn **AWS CodeBuild**
- **Region** chọn **Asia Pacific (Singapore)**
- **Project name** chọn **app_lab_build**
- **Build type** chọn **Single build**
- Chọn **Next**

![CODEPIPELINE](/images/3.createpipeline/004-createpipeline.png)

5. Trong giao diện **Add deploy stage**

- **Deploy provider** chọn **AWS CodeDeploy**
- **Region** chọn **Asian Pacific (Singapore)**
- **Application name** chọn **codedeploy_app_lab**
- **Deployment group** chọn **codedeploy-group**
- Chọn **Next**

![CODEPIPELINE](/images/3.createpipeline/005-createpipeline.png)

6. Trong giao diện **Review Info**

- Chọn **Create pipeline**

![CODEPIPELINE](/images/3.createpipeline/005-1-createpipeline.png)

- CodePipeline đã bắt đầu chạy sau 4-10 phút sẽ thành công

![CODEPIPELINE](/images/3.createpipeline/006-createpipeline.png)


