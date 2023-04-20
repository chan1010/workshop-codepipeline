---
title: "Check the operation of pipeline."
date: "`r Sys.Date()`"
weight: 4
chapter: false
pre: " <b> 3.4 </b> "
---

1. Go to [EC2 service management console](https://ap-southeast-1.console.aws.amazon.com/ec2/home)

- Go to instance **Linux Instance**

![TEST](/images/3.createpipeline/007-createpipeline.png)

- Coppy **Public IPv4 DNS** or **Public IPv4 address** go to browser and observe.

![TEST](/images/3.createpipeline/008-createpipeline.png)


2. Go to folder app_lab in local

- update content file **src/App.vue**

```
        <vue3-flip-countdown countdownSize="5rem" mainColor="pink" deadline="2024-01-01 00:00:00"/>
```

```
git add -A
git commit -m "change date countdown"
git push origin master
```
![TEST](/images/3.createpipeline/009-createpipeline.png)

2. Go to [giao diện quản trị dịch vụ Codecommit](https://ap-southeast-1.console.aws.amazon.com/codesuite/codecommit/repositories)
- Click **Repositories** **app_lab**
- Click **Commits**

![TEST](/images/3.createpipeline/010-createpipeline.png)

3. Go to [giao diện quản trị dịch vụ CodePipeline](https://ap-southeast-1.console.aws.amazon.com/codesuite/codepipeline/pipelines)

- Click **pipeline** **app_lab_pipeline**
- Click **History**

![TEST](/images/3.createpipeline/011-createpipeline.png)

4. Coppy **Public IPv4 DNS address**  go to browser and observe.

![TEST](/images/3.createpipeline/012-createpipeline.png)