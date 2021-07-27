# Docker Learning
Docker is an open platform for developing, shipping and running applications. It makes developers control environment and version of the application.

## Installation
1. Mac and Windows is easily to install, just go to download Docker Desktop in [this website](https://www.docker.com/products/docker-desktop)
2. With Linux, you have to use command line to install which will take more step than Mac and Windows. You can visit [this website](https://docs.docker.com/get-docker/) for more information.

## Docker concept
1. image - blueprint that include essential things to create container such as ubuntu, node image. You can also pull or download image from docker hub and publish your own image to global user as well.
2. container - runnable instance of an image. It contains everything needed to run an application (code, tools, libraries, runtime and setting). When you develop your application, you can start all containers that used in your app to start developing in the same environment.
3. volume - keep container data. When delete container or image, the data will still stored in the volume.
4. network - because containers are isolated, it means they don't know how to communicate with each other. So, they need network and to enable them to communicate, you have to define port and network type.
5. registry - image repository that let you push and pull images. You can make it shows all images and choose the desired image from the output or you can go to [Docker Hub](https://hub.docker.com/search?q=&type=image) to see all images in your web browser. 

## Docker file
### Dockerfile
Dockerfile is a text document that contains all the commands to create a container. These following are Dockerfile syntax.
1. use # symbol to comment one line
2. FROM - define Docker image that you use
3. WORKDIR - change directory, define the directory you will work with
4. COPY - copy file from Docker host to Docker image. The format is COPY SRC_PATH DEST_PATH
5. RUN - run command such as installing application and packages
6. EXPOSE - define what ports should be available to communicate with a container.
7. CMD - execute command

You can create Docker image from docker file by running `docker build -t IMAGE_NAME:TAG_NAME DOCKERFILE_DIRECTORY` such as `docker build -t carlos/simple-backend .`

After that, you can run docker by using `docker run -p 4000:4000 carlos/simple-backend`. Then, go to localhost:4000

### .dockerignore
use to ignore file that you don't want to keep that files in the container such as node_module.

## docker command
1. docker ps - displays all running container
2. docker stop CONTAINER_ID - stop running container
3. docker start CONTAINER_ID - start running container
4. docker images - displays all images
5. docker pull IMAGE_NAME - download an image
6. docker 

## volume
volume keeps dynamic data and keep static data in container.

## docker compose 
docker compose is a script for defining and running multiple containers.

- docker-compose build - build containers
- docker-compose up -d - run all containers but don't show any log
- docker logs CONTAINER_ID - look the log of the container