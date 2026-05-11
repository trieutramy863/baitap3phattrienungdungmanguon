# baitap3phattrienungdungmanguon
# Môn: Phát triển ứng dụng với mã nguồn mở-TEE0421

Lớp: 58KTPM

**Bài tập 03:**  

# SỬ DỤNG WORDPRESS ĐỂ TẠO WEB SITE
## deadline : 23h59 ngày 12 tháng 5 năm 2026.

   
1. SỬ DỤNG DOCKER TRÊN UBUNTU ĐỂ TẠO docker ccompose chứa: 
- Mariadb: sử dụng **image: mariadb:latest** để làm hệ quản trị csdl cho wordpress
- Phpmyadmin: sư dụng **image: phpmyadmin:latest** để đăng nhập vào mariadb rồi tạo csdl trống (chỉ để xem, ko cần tạo bảng từ đây, wordpress sẽ làm hết)
- WordPress: Sử dụng **image: wordpress:latest**, truyền các tham số môi trường cho wordpress là các thông tin truy cập csdl mariadb, tạo bởi Phpmyadmin

2. Yêu cầu: sau khi có 3 service này trong file docker-compose.yml :
- Cấu hình để hệ thống chạy
- Sử dụng cloudflare tunnel để public web này lên 1 sub-domain
- Tạo 1 bài viết trong wordpress giới thiệu về bản thân sinh viên: thông tin cá nhân, sở thích, ... bài viết có thể chứa hình ảnh, âm thanh, video, ...
- Tạo 1 bài viết trong wordpress giới thiệu về ngành học mà em yêu thích trong trường TNUT. bài viết phải chứa hình ảnh, video, ...
- Nhận xét việc sử dụng mã nguồn mở wordpress để tạo website (tốn công sức thế nào, dễ/khó dùng ra sao, tốn kém tài nguyên(ssh/ram) của máy chủ ra sao,....)


## BÀI LÀM
1
- khởi động docker trong ubuntu
sudo systemctl enable docker
sudo systemctl start docker
- Kiểm tra:
docker --version
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/fb44ed8c-781f-442e-8a7b-e100ed0ee1c5" />
- Tạo thư mục project
mkdir wordpress-docker
cd wordpress-docker
<img width="378" height="85" alt="image" src="https://github.com/user-attachments/assets/0f069372-82f5-43cb-9557-1848bf070add" />

- Tạo file docker-compose.yml

Tạo file:
nano docker-compose.yml
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/5c817a36-35ff-4614-a95b-d7e4482a9480" />

-Chạy hệ thống
Khởi động containers
sudo docker-compose up -d
<img width="1639" height="325" alt="image" src="https://github.com/user-attachments/assets/7ed0da80-5d6e-4503-a2fb-618d8a4589a1" />
- 
4. Mở trình duyệt
WordPress
http://localhost:8080

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/06754a96-fe8e-4633-bcf3-26af2db7de88" />

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/5428fcd4-1b67-4943-8734-8c6ba991d586" />

phpMyAdmin
http://localhost:8081

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/d905c338-6266-4e6f-b38d-21cdd6244b7a" />
# Tạo bài viết trong wodpress
1. giới thiệu bản thân 
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/46831e80-bfae-4ca3-afd7-46b0b785ee5a" />
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/b67a4a1c-16f0-4f10-a4ba-9a25fc44db69" />
2. giới thiệu về ngành học mà em yêu thích trong trường tnut

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/dc87220f-e473-4951-a66d-79c4507d7222" />

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/c57991e6-cae9-4279-b135-b2e140eaecfd" /> 

Public website bằng Cloudflare Tunnel



