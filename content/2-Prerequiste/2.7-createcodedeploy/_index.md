---
title : "Create AWS Codedepoy"
date :  "`r Sys.Date()`" 
weight : 7 
chapter : false
pre : " <b> 2.7 </b> "
---

1. Make connection to EC2 with MobaXterm or putty

![CODEDEPLOY](/images/2.prerequisite/001-connectec2.png)

2. Install CodeDeploy Agent
```
sudo yum update -y
```
![CODEDEPLOY](/images/2.prerequisite/001-update.png)

```
sudo yum install ruby wget -y
```
```
yum install -y aws-cli
```

![CODEDEPLOY](/images/2.prerequisite/002-update.png)

```
sudo wget https://aws-codedeploy-ap-southeast-1.s3.ap-southeast-1.amazonaws.com/latest/install
```
![CODEDEPLOY](/images/2.prerequisite/003-update.png)

Change permistion install
```
sudo chmod +x ./install
```
```
sudo ./install auto
```
Check CodeDeploy Agent
```
sudo service codedeploy-agent status
```
![CODEDEPLOY](/images/2.prerequisite/004-update.png)

{{%notice info%}}
If the output is **AWS CodeDeploy agent running as PID 4562** or any other PID, it means that the deployment agent is running properly.
{{%/notice%}}

{{%notice warning%}}
If the output indicates error: No AWS CodeDeploy agent running, then start the agent by running the command below and check the status again.
{{%/notice%}}

```
sudo service codedeploy-agent start
```

3. Go to [CodeDeploy service management console](https://ap-southeast-1.console.aws.amazon.com/codesuite/codedeploy/deployments)
- Click **Applications**
- Click **Create application**
![CODEDEPLOY](/images/2.prerequisite/001-createcodedeploy.png)

4. In the interface **Create application**
- In the **Application name** enter **codedeploy_app_lab**
- In the **Compute platform** enter **EC2/On-premises**
- Click **Create application**
![CODEDEPLOY](/images/2.prerequisite/002-createcodedeploy.png)

5. After creating CodeDeploy successfully .
- Click **Create deployment group**

![CODEDEPLOY](/images/2.prerequisite/003-createcodedeploy.png)

6. At the **Create deployment group** page
- In the **Deployment group name** enter **codedeploy-group**
- In the **Service role** Click **CodeDeploy-Role**

![CODEDEPLOY](/images/2.prerequisite/004-createcodedeploy.png)

- In the **Deployment type** Click **In-place**
- In the **Environment configuration** Click **Amazon EC2 instances**
- In the **Tag group 1** Click **key** is **Name**, **value** is **Linux Instance**

![CODEDEPLOY](/images/2.prerequisite/005-createcodedeploy.png)

- In the **Install AWS CodeDeploy Agent** Click **Never**
- In the **Load balancer** bỏ Click **Enable load balancing**
- Click **Create deployment group**
![CODEDEPLOY](/images/2.prerequisite/006-createcodedeploy.png)