---
title : "Web Tier"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3.3. </b> "
---

1. Cài đặt unzip và giải nén code từ file zip frontend.zip

![EC2](/images/303/001.png)
![EC2](/images/303/002.png)

2. Tương tự với Application Tier, ta cũng tạo thư mục và user sử dụng cho dự án frontend

![EC2](/images/303/003.png)
![EC2](/images/303/004.png)

3. Sửa url của backend thành ip của Application tier EC2

![EC2](/images/303/005.png)
![EC2](/images/303/006.png)

4. Install node, npm

5. Install nginx

![EC2](/images/303/007.png)
![EC2](/images/303/008.png)

6. Build dự án, sau khi build xong 1 thư mục tên là **build** sẽ được tạo ra

```
npm run build
```

![EC2](/images/303/009.png)

7. Dùng nginx làm web server : tạo ra 1 file nginx có tên là react.conf ở đường dẫn **/etc/nginx/conf.d/**. Thêm nội dung (như ảnh). Sau đó restart lại nginx

![EC2](/images/303/010.png)
![EC2](/images/303/011.png)
![EC2](/images/303/012.png)


8. Dùng nginx để revert proxy : tạo ra 1 file có tên là react_nginx ở đường dẫn **/etc/nginx/sites-enabled/ với nội dung :

![EC2](/images/303/013.png)

9. Mở thêm cổng 80 HTTP của Security Group - Public subnet

![EC2](/images/303/018.png)

10. nginx sẽ chuyển các request từ cổng 80 tới cổng 3000 đang chạy dự án, giờ hãy truy cập vào dự án bằng chính ip của EC2 Public

![EC2](/images/303/014.png)

11. Lỗi 500. Lỗi này xảy ra vì chúng ta chưa cấp phép cho user khác (other) truy cập vào folder **build**. Ta chỉ cần kiểm tra nginx là user nào, ở đây chính là www-data, sau đó thêm vào group **frontend**

![EC2](/images/303/015.png)
![EC2](/images/303/016.png)

12. Done, web của chúng ta đã hoạt động qua ip của EC2 cổng 80 rồi.

![EC2](/images/303/017.png)