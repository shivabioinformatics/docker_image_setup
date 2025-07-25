# docker_image_setup
---
Docker Set Up
---

1: Installed Docker Desktop for Mac (Apple chip) from: https://www.docker.com/products/docker-desktop/

2: Open a terminal, load your docker image files (for instance my_image.tar), we need to load it. 

```
docker load -i docker load -i ~/Downloads/wo1P8VqUSgCAh_WdGwmorA_b1b41be909714887a3d62de2e79387f1_gencommand_image.tar
```

output: "Loaded image: gencommand_image:v1.0.0 "



All the imgage that has been created before plus the recent ones will show up 
```
docker run -it --name gencommand_container gencommand_image:v1.0.00
```

output: "REPOSITORY"  "TAG"  "IMAGE ID" " CREATED"  "SIZE"                                                            

you might get this warning:WARNING: The requested image's platform (linux/amd64) does not match the detected host platform (linux/arm64/v8) and no specific platform was requested
When you see this, this means you are inside the contanier and it looks like this:
(base) [root@d370f096d270 /]#


Name your container, for instance : 

```
docker run -it --name gencommand_container gencommand_image:v1.0.00
```
to start docker image use
```
docekr start 
``` 

#### Summary

1. Loading the Docker Image
	```
	docker load -i <path to image tar file>/gencommand_image.tar
	```

2. Checking your Docker Images
	```
	docker images
	```

3. Creating and running the Docker Container
	```
	docker run -it --name <name of the container> gencommand_image:v1.0.0
	```
4. Checking your Docker Container
	```
	docker ps -a
	```
5. Starting (and re-starting) the Docker Container
	```
	docker start <name of the container>
	```
6. Working within the Docker Container
	```
	docker exec -it <name of the container> /bin/bash
	```
7. Stopping the Docker Container
	```
	docker stop <name of the container>
	```
8. Copying Files to and from the Docker Container
	```
	
	```
