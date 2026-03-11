# Phần 1:	Các lệnh cơ bản thao tác với Docker		

## 1	docker --version

![](images\docker_1\1.png)

## 2	docker run hello-world

![](images\docker_1\2.png)

## 3	docker pull nginx

![](images\docker_1\3.png)

## 4	docker images

![](images\docker_1\4.png)

## 5	docker run -d nginx

![](images\docker_1\5.png)

## 6	docker ps

![](images\docker_1\6.png)

## 7	docker ps -a

![](images\docker_1\7.png)

## 8	docker logs <container_id>

![](images\docker_1\8.png)

## 9	docker exec -it <container_id> /bin/sh

![](images\docker_1\9.png)

## 10	docker stop <container_id>

![](images\docker_1\10.png)

## 11	docker restart <container_id>

![](images\docker_1\11.png)

## 12	docker rm <container_id>

![](images\docker_1\12.png)

## 13	docker container prune

![](images\docker_1\13.png)

## 14	docker rmi <image_id>

![](images\docker_1\14.png)

## 15	docker image prune -a

![](images\docker_1\15.png)

## 16	docker run -d -p 8080:80 nginx
## 17	docker inspect <container_id>
## 18	docker run -d -v mydata:/data nginx
## 19	docker volume ls
## 20	docker volume prune
## 21	docker run -d --name my_nginx nginx
## 22	docker stats
## 23	docker network ls
## 24	docker network create my_network
## 25	docker run -d --network my_network --name my_container nginx
## 26	docker network connect my_network my_nginx
## 27	docker run -d -e MY_ENV=hello_world nginx
## 28	docker logs -f my_nginx
## 29	Dockerfile
> FROM nginx  
> COPY index.html /usr/share/nginx/html/index.html
## 30	docker build -t my_nginx_image .
## 31	docker run -d -p 8080:80 my_nginx_image