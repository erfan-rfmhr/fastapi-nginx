# fastapi-nginx
Run fastapi app with nginx.

# Installation
Build images:<br>
```docker build -t myapp -f app.Dockerfile .```<br>
```docker build -t mynginx -f nginx.Dockerfile .```<br>
Create a network:<br>
```docker network create fastapi-nginx-net```<br>
Run containers:<br>
```docker run -d --network fastapi-nginx-net --name fastapi-app -p 8000:8000 myapp```<br>
```docker run -d --network fastapi-nginx-net --name nginx-server -p 80:80 mynginx```<br>
Enter your ip address in browser and see the result!
