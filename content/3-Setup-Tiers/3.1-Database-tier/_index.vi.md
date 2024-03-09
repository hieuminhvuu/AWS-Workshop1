---
title : "Database Tier"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 3.1. </b> "
---

- SSH tới **EC2 Private - Database**, cài đặt mongodb

```
sudo apt install software-properties-common gnupg apt-transport-https ca-certificates -y
curl -fsSL https://pgp.mongodb.com/server-7.0.asc |  sudo gpg -o /usr/share/keyrings/mongodb-server-7.0.gpg --dearmor
echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-7.0.gpg ] https://repo.mongodb.org/apt/ubuntu jammy/mongodb-org/7.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-7.0.list
```

![EC2](/images/301/001.png)

```
sudo apt update
sudo apt install mongodb-org -y
mongod --version
```

![EC2](/images/301/002.png)
![EC2](/images/301/003.png)

- Khởi động MongoDB service và kiểm tra

```
sudo systemctl status mongod
sudo systemctl start mongod
sudo systemctl status mongod
```
![EC2](/images/301/004.png)
![EC2](/images/301/005.png)

```
sudo ss -pnltu | grep 27017
mongosh
```

![EC2](/images/301/006.png)
![EC2](/images/301/007.png)

- Config MongoDB cho truy cập từ xa

```
sudo nano /etc/mongod.conf  
```

- Tìm và sửa thành :

```
# network interfaces
net:
  port: 27017
  bindIp: 0.0.0.0
```

![EC2](/images/301/008.png)

```
sudo systemctl restart mongod
```

- Kiểm tra cổng 27017 đã mở chưa :

![EC2](/images/301/009.png)