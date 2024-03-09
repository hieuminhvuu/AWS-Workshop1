---
title : "Kiểm tra kết nối"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2.2. </b> "
---

1. Truy cập vào trang EC2

    - Chọn Instances
    - Chọn EC2 Public
    - Chọn Connect

![EC2](/images/202/001.png)

2. Trong tab **Connect to instance** :
    - Chọn **SSH Client**
    - Sao chép địa chỉ ssh mẫu

![EC2](/images/202/002.png)

3. Chuẩn bị key
    - Chuyển key đã download về vào **~/.ssh** , đây là thư mục chuyên lưu trữ key ssh

![EC2](/images/202/003.png)

4. Trước khi connect, cần chmod 400 cho key, sau đó dựa vào địa chỉ ssh mẫu ở bước 2, thay đổi địa chỉ key local để ssh tới EC2 Public

![EC2](/images/202/004.png)

5. Thử ping tới internet, ping tới 2 EC2 ở Private Subnet

![EC2](/images/202/005.png)
![EC2](/images/202/006.png)

6. Copy key từ local tới EC2 Public bằng lệnh scp, dùng để ssh tới EC2 Private

![EC2](/images/202/007.png)

7. Kiểm tra đã nhận được key ở EC2 public chưa

![EC2](/images/202/008.png)

8. Trước khi ssh nhớ chmod 400 cho key

![EC2](/images/202/009.png)

9. Dùng key ssh tới 2 instance Private

![EC2](/images/202/010.png)
![EC2](/images/202/011.png)

10. Thử ping tới internet từ EC2 Private

![EC2](/images/202/012.png)

11. Kết quả là không thể ping được, ở bước sau chúng ta sẽ config.