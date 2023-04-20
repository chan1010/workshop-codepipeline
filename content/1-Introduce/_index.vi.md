---
title : "Giới thiệu"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
### Giới thiệu
Đề tài "Tự động hóa quá trình phát triển ứng dụng với CodePipeline trên AWS" nhằm giúp hiểu về quy trình phát triển ứng dụng tự động với các dịch vụ của AWS. Cụ thể sẽ được hướng dẫn cách thiết lập và sử dụng CodePipeline để tự động hoá quá trình phát triển ứng dụng.

Qua đó, hiểu được cách sử dụng CodePipeline để xây dựng một luồng công việc phát triển hoàn chỉnh trên AWS, bao gồm: quản lý mã nguồn, kiểm tra mã nguồn, đóng gói, triển khai và kiểm thử. Ngoài ra, người tham gia cũng sẽ được giới thiệu các công cụ và tài nguyên hỗ trợ quá trình phát triển tự động trên AWS.

### Codepipeline
CodePipeline là một dịch vụ của AWS cung cấp giải pháp tự động hóa quy trình phát triển phần mềm (CI/CD) từ quá trình xây dựng, kiểm tra, phê duyệt cho đến triển khai và phát hành ứng dụng. CodePipeline cho phép tạo và quản lý các luồng công việc phát triển phần mềm (pipeline) bằng cách liên kết các công cụ khác nhau như CodeCommit, CodeBuild, CodeDeploy, Elastic Beanstalk, Lambda, ECS, EKS, và các công cụ CI/CD khác nhau. CodePipeline cung cấp một trình quản lý pipeline trực quan và dễ sử dụng giúp người dùng có thể dễ dàng tạo, sửa đổi, thêm, xóa các stage hoặc các action trong pipeline một cách nhanh chóng và dễ dàng.

