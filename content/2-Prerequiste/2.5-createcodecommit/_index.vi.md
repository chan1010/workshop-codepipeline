---
title : "Tạo Codecommit"
date :  "`r Sys.Date()`" 
weight : 5 
chapter : false
pre : " <b> 2.5 </b> "
---

1. Truy cập [giao diện quản trị dịch vụ Codecommit](https://ap-southeast-1.console.aws.amazon.com/codesuite/codecommit/repositories)

- Chọn **Repositories**.
- Chọn **Create repository**.

![CODECOMMIT](/images/2.prerequisite/001-createcodecommit.png)

2. Trong trang **Create repository**

- Tại mục **Repository name** nhập **app_lab**.
- Chọn **Create**.

![CODECOMMIT](/images/2.prerequisite/002-createcodecommit.png)

### Cài đặt và cấu hình AWS CLI

Bạn có thể tham khảo thêm bài thực hành về cài đặt và cấu hình AWS CLI [tại đây](https://000011.awsstudygroup.com/).

- Chạy command dưới đây trong Command Prompt trên máy của bạn
```
  aws configure
```
- Tại bước tạo [Tạo IAM user](2.1-createami/) mở file .csv được tải xuống khi tạo **Create access key**.
- Nhập thông tin **Access Key ID**
- Nhập thông tin **Secret Access Key**

![CODECOMMIT](/images/2.prerequisite/001-configaws.png)

### Cài đặt và cấu hình Git

[Cài đặt Git](https://git-scm.com/downloads)
  
### Thiết lập trình trợ giúp thông tin xác thực

- Chạy command dưới đây trong Command Prompt trên máy của bạn
```
  git config --global credential.helper '!aws codecommit credential-helper $@'
  git config --global credential.UseHttpPath true
```

### Clone project từ CodeCommit

1. Truy cập [giao diện quản trị dịch vụ Codecommit](https://ap-southeast-1.console.aws.amazon.com/codesuite/codecommit/repositories)

- Chọn **Repository**.
- Chọn **app_lab**.

![CODECOMMIT](/images/2.prerequisite/003-createcodecommit.png)

2. Tại trang repository **app_lab**

- Chọn **Clone URL**
- Chọn **clone HTTPS**
sau khi có link git tiến hành clone về máy
![CODECOMMIT](/images/2.prerequisite/004-createcodecommit.png)

3. Chạy command dưới đây trong Command Prompt trên máy của bạn

```
git clone https://git-codecommit.ap-southeast-1.amazonaws.com/v1/repos/app_lab
```

- Nhập **User name** là **user-commit**
- Nhập **Password** của bạn đã cập nhật lại cho tài khoản **user-commit**

![CODECOMMIT](/images/2.prerequisite/001-useriam.png)

![CODECOMMIT](/images/2.prerequisite/001-doneclone.png)

4. Truy cập vào thư mục **app_lab**
- Giả nén và dán nội dung [thư mục](/app_lab/app_lab.zip) vào folder **app_lab**

5. Đẩy nội dung lên repository app_lab.
```
git add -A
git commit -m "update file"
git push origin master
```
6. Sau khi hoàn thành truy cập [giao diện quản trị dịch vụ Codecommit](https://ap-southeast-1.console.aws.amazon.com/codesuite/codecommit/repositories)
- Chọn Repository **app_lab**.
- Chọn **Code**
![CODECOMMIT](/images/2.prerequisite/004-doneclone.png)