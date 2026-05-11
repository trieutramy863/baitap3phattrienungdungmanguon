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
