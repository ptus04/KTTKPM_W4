# Docker

## Phần 1: Các lệnh cơ bản thao tác với Docker

1. docker --version

   ![](images/docker_1/1.png)

2. docker run hello-world

   ![](images/docker_1/2.png)

3. docker pull nginx

   ![](images/docker_1/3.png)

4. docker images

   ![](images/docker_1/4.png)

5. docker run -d nginx

   ![](images/docker_1/5.png)

6. docker ps

   ![](images/docker_1/6.png)

7. docker ps -a

   ![](images/docker_1/7.png)

8. docker logs <container_id>

   ![](images/docker_1/8.png)

9. docker exec -it <container_id> /bin/sh

   ![](images/docker_1/9.png)

10. docker stop <container_id>

    ![](images/docker_1/10.png)

11. docker restart <container_id>

    ![](images/docker_1/11.png)

12. docker rm <container_id>

    ![](images/docker_1/12.png)

13. docker container prune

    ![](images/docker_1/13.png)

14. docker rmi <image_id>

    ![](images/docker_1/14.png)

15. docker image prune -a

    ![](images/docker_1/15.png)

16. docker run -d -p 8080:80 nginx

    ![](images/docker_1/16.png)

17. docker inspect <container_id>

    ![](images/docker_1/17.png)

18. docker run -d -v mydata:/data nginx

    ![](images/docker_1/18.png)

19. docker volume ls

    ![](images/docker_1/19.png)

20. docker volume prune

    ![](images/docker_1/20.png)

21. docker run -d --name my_nginx nginx

    ![](images/docker_1/21.png)

22. docker stats

    ![](images/docker_1/22.png)

23. docker network ls

    ![](images/docker_1/23.png)

24. docker network create my_network

    ![](images/docker_1/24.png)

25. docker run -d --network my_network --name my_container nginx

    ![](images/docker_1/25.png)

26. docker network connect my_network my_nginx

    ![](images/docker_1/26.png)

27. docker run -d -e MY_ENV=hello_world nginx

    ![](images/docker_1/27.png)

28. docker logs -f my_nginx

    ![](images/docker_1/28.png)

29. Dockerfile
    ```docker
    FROM nginx  
    COPY index.html /usr/share/nginx/html/index.html
    ```
    ![](images/docker_1/29.png)
30. docker build -t my_nginx_image .

    ![](images/docker_1/30.png)
31. docker run -d -p 8080:80 my_nginx_image

    ![](images/docker_1/31.1.png)
    ![](images/docker_1/31.2.png)

## Phần 2: Thao tác với Dockerfile

1. Tạo Dockerfile chạy một ứng dụng Node.js đơn giản
   > Yêu cầu:  
   > Viết Dockerfile để chạy một ứng dụng Node.js hiển thị "Hello, Docker!" trên cổng 3000.
   > Sử dụng node:18 làm base image.

2. Tạo Dockerfile chạy một ứng dụng Python Flask
   > Yêu cầu:  
   > Viết Dockerfile để chạy một ứng dụng Flask hiển thị "Hello, Docker Flask!" trên cổng 5000.
   > Sử dụng python:3.9 làm base image.

3. Tạo Dockerfile chạy một ứng dụng React
   > Yêu cầu:  
   > Viết Dockerfile để build và chạy một ứng dụng React.
   > Sử dụng node:18-alpine làm base image.

4. Tạo Dockerfile chạy một trang web tĩnh bằng Nginx
   > Yêu cầu:  
   > Tạo một file index.html đơn giản và sử dụng nginx:latest để phục vụ trang web.

5. Tạo Dockerfile cho ứng dụng Go
   > Yêu cầu:  
   > Viết Dockerfile để build và chạy một ứng dụng Go đơn giản.

6. Sử dụng Multi-stage Build trong Dockerfile
   > Viết Dockerfile để build một ứng dụng Node.js với hai stage:  
   > Stage 1: Dùng node:18 để build code.  
   > Stage 2: Dùng node:18-alpine để chạy ứng dụng đã build.

7. Sử dụng biến môi trường trong Dockerfile
   > Yêu cầu:  
   > Viết Dockerfile cho ứng dụng Python đọc biến môi trường APP_ENV và in ra màn hình.  
   > Sử dụng ENV APP_ENV=development trong Dockerfile.

8. Tạo Dockerfile cho PostgreSQL tùy chỉnh
   > Yêu cầu:  
   > Viết Dockerfile để chạy PostgreSQL (postgres:15).  
   > Thêm file SQL để tự động tạo database khi container chạy lần đầu tiên.

9. Tạo Dockerfile chạy Redis với cấu hình tùy chỉnh
   > Yêu cầu:  
   > Viết Dockerfile sử dụng redis:latest.  
   > Thêm file redis.conf vào container.

10. Chạy ứng dụng PHP với Apache
    > Yêu cầu:  
    > Viết Dockerfile để chạy một ứng dụng PHP đơn giản (php:8.2-apache).  
    > Mount mã nguồn từ máy host vào container.