---
title: "Tạo VPC"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 2.2 </b> "
---

### Tạo VPC

1. Truy cập [giao diện quản trị dịch vụ VPC](https://console.aws.amazon.com/vpc/home)

- Chọn **Your VPC**.
- Chọn **Create VPC**.

![VPC](/images/2.prerequisite/001-createvpccodepipeline.png)

2. Tại trang **Create VPC**.

- Tại mục **Name tag** điền **VPC_CodePileline**.
- Tại mục **IPv4 CIDR** điền : **10.10.0.0/16**.
- Chọn **Create VPC**.

![VPC](/images/2.prerequisite/002-createvpccodepipeline.png)

### Tạo Subnet

1. Truy cập [giao diện quản trị dịch vụ VPC](https://console.aws.amazon.com/vpc/home)

- Chọn **Subnets**.
- Chọn **Create Subnet**.

![VPC](/images/2.prerequisite/001-createsubnet.png)

2. Tại **VPC ID** chọn **VPC_CodePipeline**

![VPC](/images/2.prerequisite/002-createsubnet.png)

3. Tại **Subnet setting**.
- Tại mục **Subnet name** điền **Public Subnet**.
- Tại mục **Availability Zone** chọn Availability zone đầu tiên.
- Tại mục **IPv4 CIRD block** điền **10.10.1.0/24**.
- Chọn **Create Subnet**.

![VPC](/images/2.prerequisite/003-createsubnet.png)

4. Click chọn **Public Subnet**.
- Click **Actions**.
- Click **Edit subnet settings**.

![VPC](/images/2.prerequisite/004-createsubnet.png)

5. Tại trang **Edit subnet settings** kéo xuống phần **Auto-assign IP settings**

- Chọn **Enable auto-assign public IPv4 address**.
- Chọn **Save**

![VPC](/images/2.prerequisite/005-createsubnet.png)

### Tạo Internet Gateways

1. Truy cập [giao diện quản trị dịch vụ VPC](https://console.aws.amazon.com/vpc/home)

- Chọn **Internet Gateways**.
- Chọn **Create internet gateway**.

![VPC](/images/2.prerequisite/001-createigw.png)

2. Tại trang **Create internet gateway**.

- Tại mục **Name tag** điền **Lab-IGW**.
- Chọn **Create internet gateway**.

![VPC](/images/2.prerequisite/002-createigw.png)


3. Sau khi tạo thành công.

- Chọn **Actions**.
- Chọn **Attach to VPC**.

![VPC](/images/2.prerequisite/003-createigw.png)

4. Tại trang **Attach to VPC**

- Tại mục **Available VPCs** chọn **VPC_CodePipeline**.
- Chọn **Attach internet gateway**.

![VPC](/images/2.prerequisite/004-createigw.png)

### Tạo Router Table

1. Truy cập [giao diện quản trị dịch vụ VPC](https://console.aws.amazon.com/vpc/home)

- Chọn **Router Tables**.
- Chọn **Create router table**.

![VPC](/images/2.prerequisite/001-creatertb.png)

2. Tại trang **Create router table**.

- Tại mục **Name** điền **Lab Publicrtb**.
- Tại mục VPC, chọn **VPC_CodePipeline**.
- Chọn **Create route table**.

![VPC](/images/2.prerequisite/002-creatertb.png)


3. Sau khi tạo thành công.

- Chọn **Actions**.
- Chọn **Edit routes**.

![VPC](/images/2.prerequisite/003-creatertb.png)

4. Tại trang **Edit routes**

- Chọn **Add route**.
- Tại mục **Destination** điền **0.0.0.0/0**.
- Tại mục **Target** chọn **Internet Gateway** sau đó chọn **Lab-IGW**.
- Chọn **Save changes**.

![VPC](/images/2.prerequisite/004-creatertb.png)

5. Chọn tab **Subnet associations**.

- Chọn **Edit subnet associations**.

![VPC](/images/2.prerequisite/005-creatertb.png)

6. Tại trang **Edit subnet associations**.

- Chọn chọn **Subnet Public**.
- Chọn **Save associations**.

![VPC](/images/2.prerequisite/006-creatertb.png)

### Tạo Security Group

1. Truy cập [giao diện quản trị dịch vụ VPC](https://console.aws.amazon.com/vpc/home)

- Chọn **Security Group**.
- Chọn **Create security group**.

![VPC](/images/2.prerequisite/003-createsg.png)

2. Tại trang **Create security group**.

- Tại mục **Security group name** điền **VPC_CodePipeline_SG**.
- Tại mục **Description** điền : **SG Public**.
- Tại mục **VPC** click dấu X để chọn lại **VPC_CodePileline**.

![VPC](/images/2.prerequisite/004-createsg.png)

3. Cấu hình **Inbound rule** bằng cách chọn Add rule.

- **SSH**, cổng 22 để kết nối qua PuTTY.
- **HTTP**, cổng 80.

![VPC](/images/2.prerequisite/005-createsg.png)

4. Kiểm tra **Outbound rules** và chọn **Create security group**.

![VPC](/images/2.prerequisite/006-createsg.png)

5. Hoàn thành tạo **Security Group**. Kiểm tra thông tin chi tiết Security Group.

![VPC](/images/2.prerequisite/007-createsg.png)