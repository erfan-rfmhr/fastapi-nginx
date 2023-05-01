# fastapi-nginx
Run fastapi app with nginx.

# Installation
Build images:
```docker build -t myapp -f app.Dockerfile .```
```docker build -t mynginx -f nginx.Dockerfile .```
Create a network:
```docker network create fastapi-nginx-net```
Run containers:
```docker run -d --network fastapi-nginx-net --name fastapi-app -p 8000:8000 myapp```
```docker run -d --network fastapi-nginx-net --name nginx-server -p 80:80 mynginx```
Enter your ip address in browser and see the result!
