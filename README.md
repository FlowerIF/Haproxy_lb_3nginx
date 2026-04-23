HAProxy Lab – Cân bằng tải Nginx với Podman cơ bản

** 
Tạo 3 container chạy Nginx, mỗi container trả về một response khác nhau.
HAProxy đứng trước cân bằng tải theo thuật toán round‑robin.



** Kiểm tra
for i in {1..6}; do curl -s http://localhost:6789; done
Kết quả mong đợi
Luân phiên hiển thị NGINX 1, NGINX 2, NGINX 3.
 ```html
Ví dụ:
 [admin@localhost haproxylab]$ for i in {1..10}; do curl -s http://localhost:6789; done
<h1>Response from NGINX 1</h1>
<h1>Response from NGINX 2</h1>
<h1>Response from NGINX 3</h1>
<h1>Response from NGINX 1</h1>
<h1>Response from NGINX 2</h1>
<h1>Response from NGINX 3</h1>
<h1>Response from NGINX 1</h1>
<h1>Response from NGINX 2</h1>
<h1>Response from NGINX 3</h1>
<h1>Response from NGINX 1</h1>"
```
