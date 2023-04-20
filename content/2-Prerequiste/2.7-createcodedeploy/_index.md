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
Nếu đầu ra là **Tác nhân AWS CodeDeploy đang chạy dưới dạng PID 4562** hoặc bất kỳ PID nào khác. Điều đó có nghĩa là tác nhân triển khai mã đang chạy tốt.
{{%/notice%}}

{{%notice warning%}}

Nếu đầu ra cho biết **error: No AWS CodeDeploy agent running**, thì hãy khởi động tác nhân bằng cách chạy lệnh bên dưới và kiểm tra lại trạng thái.

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

5. Sau khi tạo thành công CodeDeploy
- Click **Create deployment group**

![CODEDEPLOY](/images/2.prerequisite/003-createcodedeploy.png)

6. Tại trang **Create deployment group**
- In the **Deployment group name** enter **codedeploy-group**
- **Service role** Click **CodeDeploy-Role**

![CODEDEPLOY](/images/2.prerequisite/004-createcodedeploy.png)

7. 
- **Deployment type** Click **In-place**
- **Environment configuration** Click **Amazon EC2 instances**
- **Tag group 1** Click **key** is **Name**, **value** is **Linux Instance**

![CODEDEPLOY](/images/2.prerequisite/005-createcodedeploy.png)

8. 
- **Install AWS CodeDeploy Agent** Click **Never**
- **Load balancer** bỏ Click **Enable load balancing**
- Click **Create deployment group**
![CODEDEPLOY](/images/2.prerequisite/006-createcodedeploy.png)