---
title: "Create pipeline"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 3.1 </b> "
---

1. Go to [CodePipeline service management console](https://ap-southeast-1.console.aws.amazon.com/codesuite/codepipeline/pipelines)

- Click **Pipelines**
- Click **Create pipeline**

![CODEPIPELINE](/images/3.createpipeline/001-createpipeline.png)

2. At the **Create pipeline** section

- In the **Pipepline name** nhập **app_lab_pipeline**
- In the **Service role** click **New service role**
- Click **Next**

![CODEPIPELINE](/images/3.createpipeline/002-createpipeline.png)

3. At the **Add source stage** section

- In the **Source provider** click **app_lab_pipeline**
- In the **Repository name** click **app_lab**
- In the **Branch name** click **master**
- In the **Change detection options** click **AWS CodePipeline**
- Click **Next**

![CODEPIPELINE](/images/3.createpipeline/003-createpipeline.png)

4. At the **Add build stage** section

- In the **Build provider** click **AWS CodeBuild**
- In the **Region** click **Asia Pacific (Singapore)**
- In the **Project name** click **app_lab_build**
- In the **Build type** click **Single build**
- Click **Next**

![CODEPIPELINE](/images/3.createpipeline/004-createpipeline.png)

5. At the **Add deploy stage** section

- In the **Deploy provider** click **AWS CodeDeploy**
- In the **Region** click **Asian Pacific (Singapore)**
- In the **Application name** click **codedeploy_app_lab**
- In the **Deployment group** click **codedeploy-group**
- Click **Next**

![CODEPIPELINE](/images/3.createpipeline/005-createpipeline.png)

6. At the **Review Info** section

- Click **Create pipeline**

![CODEPIPELINE](/images/3.createpipeline/005-1-createpipeline.png)

- CodePipeline has started running after 4-10 minutes will be successful

![CODEPIPELINE](/images/3.createpipeline/006-createpipeline.png)


