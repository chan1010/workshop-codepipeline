---
title: "Create AWS VPC"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 2.2 </b> "
---

### Create VPC

1. Go to [VPC service management console](https://console.aws.amazon.com/vpc/home)

- Click **Your VPC**.
- Click **Create VPC**.

![VPC](/images/2.prerequisite/001-createvpccodepipeline.png)

2. At the **Create VPC** page.

- In the **Name tag** enter **VPC_CodePileline**.
- In the **IPv4 CIDR** enter : **10.10.0.0/16**.
- Click **Create VPC**.

![VPC](/images/2.prerequisite/002-createvpccodepipeline.png)

### Create Subnet

1. Go to [VPC service management console](https://console.aws.amazon.com/vpc/home)

- Click **Subnets**.
- Click **Create Subnet**.

![VPC](/images/2.prerequisite/001-createsubnet.png)

2. At the **VPC ID** Click **VPC_CodePipeline**

![VPC](/images/2.prerequisite/002-createsubnet.png)

3. At the **Subnet setting** page.
- In the **Subnet name** enter **Public Subnet**.
- In the **Availability Zone** Click on the first Availability zone.
- In the **IPv4 CIRD block** enter **10.10.1.0/24**.
- Click **Create Subnet**.

![VPC](/images/2.prerequisite/003-createsubnet.png)

4. Click choose subnet have name **Public Subnet**.
- Click **Actions**.
- Click **Edit subnet settings**.

![VPC](/images/2.prerequisite/004-createsubnet.png)

5. At the **Edit subnet settings** scroll to **Auto-assign IP settings**

- Click **Enable auto-assign public IPv4 address**.
- Click **Save**

![VPC](/images/2.prerequisite/005-createsubnet.png)

### Create Internet Gateways

1. Go to [VPC service management console](https://console.aws.amazon.com/vpc/home)

- Click **Internet Gateways**.
- Click **Create internet gateway**.

![VPC](/images/2.prerequisite/001-createigw.png)

2. At the **Create internet gateway** page.

- In the **Name tag** enter **Lab-IGW**.
- Click **Create internet gateway**.

![VPC](/images/2.prerequisite/002-createigw.png)


3. After creating **Create internet gateway** successfully.

- Click **Actions**.
- Click **Attach to VPC**.

![VPC](/images/2.prerequisite/003-createigw.png)

4. At the **Attach to VPC** page

- In the **Available VPCs** Click **VPC_CodePipeline**.
- Click **Attach internet gateway**.

![VPC](/images/2.prerequisite/004-createigw.png)

### Create Router Table

1. Go to [VPC service management console](https://console.aws.amazon.com/vpc/home)

- Click **Router Tables**.
- Click **Create router table**.

![VPC](/images/2.prerequisite/001-creatertb.png)

2. At the **Create router table** page.

- In the **Name** enter **Lab Publicrtb**.
- In the VPC, Click **VPC_CodePipeline**.
- Click **Create route table**.

![VPC](/images/2.prerequisite/002-creatertb.png)


3. After creating **router table** successfully.

- Click **Actions**.
- Click **Edit routes**.

![VPC](/images/2.prerequisite/003-creatertb.png)

4. At the **Edit routes** page

- Click **Add route**.
- In the **Destination** enter **0.0.0.0/0**.
- In the **Target** Click **Internet Gateway** sau đó Click **Lab-IGW**.
- Click **Save changes**.

![VPC](/images/2.prerequisite/004-creatertb.png)

5. Click tab **Subnet associations**.

- Click **Edit subnet associations**.

![VPC](/images/2.prerequisite/005-creatertb.png)

6. At the **Edit subnet associations** page.

- Click **Subnet Public**.
- Click **Save associations**.

![VPC](/images/2.prerequisite/006-creatertb.png)

### Create Security Group

1. Go to [VPC service management console](https://console.aws.amazon.com/vpc/home)

- Click **Security Group**.
- Click **Create security group**.

![VPC](/images/2.prerequisite/003-createsg.png)

2. At the **Create security group** page.

- In the **Security group name** enter **VPC_CodePipeline_SG**.
- In the **Description** enter : **SG Public**.
- In the **VPC** click dấu X để Click lại **VPC_CodePileline**.

![VPC](/images/2.prerequisite/004-createsg.png)

3. Configuration **Inbound rule** Click Add rule.

- **SSH**, port 22 to connect PuTTY.
- **HTTP**, port 80.

![VPC](/images/2.prerequisite/005-createsg.png)

4. Test **Outbound rules** và Click **Create security group**.

![VPC](/images/2.prerequisite/006-createsg.png)

5. Complete Create **Security Group**. Test information details Security Group.

![VPC](/images/2.prerequisite/007-createsg.png)