---
title: "Kiểm tra hoạt động của pipeline."
date: "`r Sys.Date()`"
weight: 4
chapter: false
pre: " <b> 3.4 </b> "
---

### Kiểm tra quá trình tự động CodePipeline

1. Truy cập [giao diện quản trị dịch vụ EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/home)

- Truy cập instance **Linux Instance**

![TEST](/images/3.createpipeline/007-createpipeline.png)

- Dán **Public IPv4 DNS** hoặc **Public IPv4 address** vào trình duyệt và quan sát.

![TEST](/images/3.createpipeline/008-createpipeline.png)


2. Truy cập folder app_lab ở local

- update nội dung file **src/App.vue**

```
        <vue3-flip-countdown countdownSize="5rem" mainColor="pink" deadline="2024-01-01 00:00:00"/>
```

```
git add -A
git commit -m "change date countdown"
git push origin master
```
![TEST](/images/3.createpipeline/009-createpipeline.png)

2. Truy cập [giao diện quản trị dịch vụ Codecommit](https://ap-southeast-1.console.aws.amazon.com/codesuite/codecommit/repositories)
- Click **Repositories** **app_lab**
- Click **Commits**

![TEST](/images/3.createpipeline/010-createpipeline.png)

3. Truy cập [giao diện quản trị dịch vụ CodePipeline](https://ap-southeast-1.console.aws.amazon.com/codesuite/codepipeline/pipelines)

- Click **pipeline** **app_lab_pipeline**
- Click **History**

![TEST](/images/3.createpipeline/011-createpipeline.png)

4. Dán **Public IPv4 DNS address** vào trình duyệt vào trình duyệt và quan sát.

![TEST](/images/3.createpipeline/012-createpipeline.png)