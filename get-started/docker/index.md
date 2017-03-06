# Get Started with Docker

> 6th March, 2017, 21:45.

Simple notes for references.

## Basic

Docker Images

- `docker search <name>`: Search for images.
- `docker pull <name>:<tag>`: Pull images.
	- `docker pull ubuntu:latest`
- `docker images`: List local images.
- `docker rmi <image-name>`: Remove specified image.
	- `docker rmi ubuntu:latest`
- `docker history <image-name>:<tag>`: Show history of image.
	- `docker history hello:0.1`
- `docker build --tag <image-name>:<tag>`: Build a docker image based on Dockerfile.
	- `docker build --tag hello:0.1`

Docker Containers 101

- `docker run <options> <image-name> <commands-to-be-run>`
	- `docker run -i -t --name hello ubuntu /bin/bash`
		- `-i`(Interactive) & `-t`(Pseudo-tty): Interactive mode.
		- `--name`: Set the container name.
- `docker ps`: List running containers
	- `docker ps -a`: List all containers
- `docker start <container-name>`: Start container.
	- `docker start hello`
- `docker restart <container-name>`: Restart container.
	- `docker restart hello`
- `docker stop <container-name>`: Stop container.
	- `docker stop hello`
- `docker attach <container-name>`: Attach container.
	- `docker attach hello`
	- `Ctrl + P, Ctrl + Q`: Detach container.
- `docker exec <container-name> <commands-to-be-run>`: Run commands directly.
	- `docker exec hello echo "Hello World"`
- `docker rm <container-name>`: Remove container.

Integrated Operations

- `docker cp <container-name>:<container-path> <local-path>`: Copy container file to local.
- `docker commit -a "<Some Message>" -m "<Some Message>" <container-name> <image-name>:<tag>`: Commit changes in container into image.
	- `docker commit -a "Berton Fisher <berton.fisher@gmail.com>" -m "Added hello.txt" helloNginx <image-name>:<tag>`
		- `-a`: Set author.
		- `-m`: Set comment.
- `docker diff <container-name>`: Show changes of container.
	- `docker diff helloNginx`
- `docker inspect <container-name>`: Inspect container.

Run containers

- `docker run <options>`
	- `docker run --name <container-name> -d -p 80:80 -v /root/data:/data hello:0.1`
	- Options
		- `-i`(Interactive) & `-t`(Pseudo-tty): Interactive mode.
		- `--name`: Set the container name.
		- `-d`: Run container in background.
		- `-p <local-port>:<container-port>`: Bind port 80 of localhost with port 80 of container.
		- `-v <local-directory>:<container-directory>`: Bind local directory with container directory.
		- `--volumes-from <container-name>`: Share the same volume from the specified container.
- `docker run <options> --link <container-name>:<container-alias> <image>`
	- `docker run --name web -d -p 80:80 --link db:db nginx`

## Publish An Image

0. `docker pull registry:latest`: Get the image for registry.
0. `docker run -d -p 3333:3333 --name registry-server -v /tmp/registry:/tmp/registry registry`: Run the registry server.
0. `docker tag hello-nginx:0.1 localhost:3333/hello-nginx:0.1`: Tag the image.
0. `docker push localhost:3333/hello-nginx:0.1`: Push the image.
0. `docker pull 127.0.0.1:3333/hello-nginx:0.1`: Pull the image.


## Docker Images

- `docker pull mongo`
- `docker pull ubuntu`
- `docker pull redis`
