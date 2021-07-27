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
