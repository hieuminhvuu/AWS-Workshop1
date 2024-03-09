---
title : "Application Tier"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.2. </b> "
---

1. Đầu tiên, ta cần zip code lại và copy tới EC2 Public

![EC2](/images/302/001.png)

2. Kiểm tra xem đã nhận được chưa

![EC2](/images/302/002.png)

3. Copy backend.zip tới EC2 Private - Application

![EC2](/images/302/003.png)

4. SSH tới EC2 Private - Application và kiểm tra

![EC2](/images/302/004.png)

5. Install unzip sau đó giải nén backend.zip

![EC2](/images/302/005.png)
![EC2](/images/302/006.png)

6. Tạo user backend, tạo thư mục /projects và chuyển thư folder backend tới

![EC2](/images/302/008.png)

7. chown, chmod folder backend, kiểm tra

![EC2](/images/302/009.png)

8. Cài đặt python, pip, venv

![EC2](/images/302/010.png)
![EC2](/images/302/011.png)
![EC2](/images/302/012.png)

9. Tạo virtualenv - môi trường cho python để chạy dự án, sau đó activate môi trường đó

![EC2](/images/302/014.png)

10. Cài đặt các dependencies của dự án 

```
pip install -r requirements.txt
```

![EC2](/images/302/015.png)


11. Sửa ip database thành ip của Database tier

![EC2](/images/302/017.png)
![EC2](/images/302/016.png)


12. Run dự án, gặp lỗi với database

![EC2](/images/302/018.png)

13. Sửa Security Group của Private Subnet, thêm rule TCP cổng 27017 của MongoDB

![EC2](/images/302/025.png)

14. Khởi động lại dự án, thành công 

![EC2](/images/302/019.png)

15. Tiếp theo, ta sẽ dùng nginx để làm revert proxy cho backend, install

![EC2](/images/302/020.png)

16. Tạo 1 file mới có tên là fastapi_nginx ở đường dẫn /etc/nginx/sites-enabled/ có nội dung như sau :

![EC2](/images/302/021.png)

17. Kiểm tra syntax của nginx và restart 

![EC2](/images/302/022.png)

18. Khởi động lại dự án, giờ nginx sẽ làm nhiệm vụ revert proxy, chuyển các request ở cổng 80 tới cổng 8000.

![EC2](/images/302/024.png)