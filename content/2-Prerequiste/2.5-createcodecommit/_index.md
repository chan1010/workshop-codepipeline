---
title : "Create AWS Codecommit"
date :  "`r Sys.Date()`" 
weight : 5 
chapter : false
pre : " <b> 2.5 </b> "
---

1. Go to [giao diện quản trị dịch vụ Codecommit](https://ap-southeast-1.console.aws.amazon.com/codesuite/codecommit/repositories)

- Click **Repositories**.
- Click **Create repository**.

![CODECOMMIT](/images/2.prerequisite/001-createcodecommit.png)

2. At the **Create repository** page

- In the **Repository name** enter **app_lab**.
- Click **Create**.

![CODECOMMIT](/images/2.prerequisite/002-createcodecommit.png)

### Installation and configuration AWS CLI

You can find more hands-on tutorials on installing and configuring the AWS CLI [tại đây](https://000011.awsstudygroup.com/).

- Run the command below in Command Prompt
```
  aws configure
```
- In step create [Create IAM user](2.1-createami/) open file .csv downloaded when Create **Create access key**.
- Enter **Access Key ID**
- Enter **Secret Access Key**

![CODECOMMIT](/images/2.prerequisite/001-configaws.png)

### Install and configuration Git

[Install Git](https://git-scm.com/downloads)
  
### Credential Helper Setup

- Run the command below in Command Prompt
```
  git config --global credential.helper '!aws codecommit credential-helper $@'
  git config --global credential.UseHttpPath true
```

### Clone project from CodeCommit

1. Go to [giao diện quản trị dịch vụ Codecommit](https://ap-southeast-1.console.aws.amazon.com/codesuite/codecommit/repositories)

- Click **Repository**.
- Click **app_lab**.

![CODECOMMIT](/images/2.prerequisite/003-createcodecommit.png)

2. At the repository **app_lab** page

- Click **Clone URL**
- Click **clone HTTPS**
After getting the git link, clone it to your computer
![CODECOMMIT](/images/2.prerequisite/004-createcodecommit.png)

3. Run the command below in Command Prompt
```
git clone https://git-codecommit.ap-southeast-1.amazonaws.com/v1/repos/app_lab
```

- **User name** enter **user-commit**
- enter **Password**

![CODECOMMIT](/images/2.prerequisite/001-useriam.png)

![CODECOMMIT](/images/2.prerequisite/001-doneclone.png)

4. Go to folther **app_lab**
- Unzip and paste the content [folther](/app_lab/app_lab.zip) in folder **app_lab**

5. Push content repository app_lab.
```
git add -A
git commit -m "update file"
git push origin master
```
6. After completing Go to [Codecommit service management console](https://ap-southeast-1.console.aws.amazon.com/codesuite/codecommit/repositories)
- Click Repository **app_lab**.
- Click **Code**
![CODECOMMIT](/images/2.prerequisite/004-doneclone.png)