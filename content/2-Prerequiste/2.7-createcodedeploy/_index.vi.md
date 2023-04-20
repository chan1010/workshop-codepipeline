---
title : "Tạo Codedepoy"
date :  "`r Sys.Date()`" 
weight : 7 
chapter : false
pre : " <b> 2.7 </b> "
---

1. Thực hiện kết nối với EC2 với MobaXterm hoặc putty

![CODEDEPLOY](/images/2.prerequisite/001-connectec2.png)

2. Caì đặt CodeDeploy Agent
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

Thay đổi permistion của trình cài đặt
```
sudo chmod +x ./install
```
```
sudo ./install auto
```
Kiểm tra CodeDeploy
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

3. Truy cập [giao diện quản trị dịch vụ Codedeploy](https://ap-southeast-1.console.aws.amazon.com/codesuite/codedeploy/deployments)
- Chọn **Applications**
- Chọn **Create application**
![CODEDEPLOY](/images/2.prerequisite/001-createcodedeploy.png)

4. Trong giao diện **Create application**
- **Application name** nhập **codedeploy_app_lab**
- **Compute platform** nhập **EC2/On-premises**
- Chọn **Create application**
![CODEDEPLOY](/images/2.prerequisite/002-createcodedeploy.png)

5. Sau khi tạo thành công CodeDeploy
- Chọn **Create deployment group**

![CODEDEPLOY](/images/2.prerequisite/003-createcodedeploy.png)

6. Tại trang **Create deployment group**
- **Deployment group name** nhập **codedeploy-group**
- **Service role** chọn **CodeDeploy-Role**

![CODEDEPLOY](/images/2.prerequisite/004-createcodedeploy.png)

7. 
- **Deployment type** chọn **In-place**
- **Environment configuration** chọn **Amazon EC2 instances**
- **Tag group 1** chọn **key** là **Name**, **value** là **Linux Instance**

![CODEDEPLOY](/images/2.prerequisite/005-createcodedeploy.png)

8. 
- **Install AWS CodeDeploy Agent** chọn **Never**
- **Load balancer** bỏ chọn **Enable load balancing**
- Chọn **Create deployment group**
![CODEDEPLOY](/images/2.prerequisite/006-createcodedeploy.png)