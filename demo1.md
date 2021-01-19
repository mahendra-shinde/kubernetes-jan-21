## Docker demo1

How to fetch base images from docker-hub and create and launch containers!

Syntax Used Image-TAG

    registry-url/repository-name:TAG

example:
    myacr101.azurecr.io/myapp:1

    Registry URL: myacr101.azurecr.io
    Repository:   myapp
    Tag:          1 

Images on default registry do not require registry

example:
    nginx:latest

    Registry URL: docker.io
    Repository:   library/nginx
    TAG:          latest

docker pull IMAGE-TAG

1. Download the NGINX image

    `$ docker pull nginx`

2.  Verify if any container is RUNNING !

    `$ docker ps`

3.  List STOPPED containers

    `$ docker ps -a `

4.  Create and Start a new container (with locally unqiue container name) [Run with output terminal]

    `$ docker run --name c1 nginx:latest`

5.  Create and Start additional container using command prompt 

    `$ docker run --name c2 nginx:latest`

6.  Using Third command prompts, check details of RUNNING

    ```
    $ docker ps
    $ docker top c1
    $ docker top c2
    $ docker inspect c1
    $ docker inspect c2
    ```

7.  The default network "bridge" is used by both container c1 and c2

    `$ docker network inspect bridge`

