---
title : "Session Management"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
---
# Deploy three-tier web app chỉ với EC2

### Tổng quan

Trong bài Workshop này, mình sẽ chia sẻ cách chỉ sử dụng EC2 ở trong các Subnet Public và Private deploy một three-tier website. Chi tiết về công nghệ các tier như sau :

- Database Tier : MongoDB
- Application Tier : Fastapi - Python
- Web Tier : React - JavaScript

Bài viết chia sẻ từ tạo các tài nguyên trên AWS cho tới chi tiết cách deploy ở từng EC2 như thế nào.

Đây là hình ảnh kiến trúc bài Workshop :

![Architecture](/images/001.png) 

### Nội dung

 1. [Chuẩn bị](1-Preparation) \
 2. [Tạo EC2](2-Create-EC2) \
 3. [Setup Tiers](3-Setup-Tiers) \
 4. [Dọn dẹp](4-Clean-up)
