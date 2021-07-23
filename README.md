# SCA-Cloud-School-Application
# Steps Taken to deploy a static website with Docker and Nginx
##### I created a directory for the website and inside that directory i created and index.html file where i put my text inside,
##### After i created a Dockerfile and i put some lines of code inside
``` 
FROM nginx:alpine
COPY . /usr/share/nginx/html 
```
##### These lines of code represent the image i use along to copy the contents of the current directory into the container.
##### I then built a docker image for the html server using the command 
```
docker build -t html-server-image:v1 . 
```
##### Then after i ran the docker container using 
```
docker run -d -p 80:80 html-server-image:v1 
```
##### After this i test the port using curl
```
curl localhost:80 
```
##### and it can also be viewed on the browser on localhost:80
## Docker repository
[Docker repository](https://hub.docker.com/r/lontchi12/html-server-image/)


