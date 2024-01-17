
## Images and containers 
- Containers are instances of images. A container = a ready-to-eat meal. An image = the recipe or ingredients for that meal.
-  You need **an image** and **a container runtime (Docker engine)** to create a container. The image provides all the necessary instructions and dependencies for the container to run, just like a recipe provides the steps and ingredients to make a meal.

### Images 
- A Docker image is a file.
- An image can never be changed after they are created
- List all your images with ```docker image ls```

```
$ docker image ls

  REPOSITORY      TAG      IMAGE ID       CREATED         SIZE
  hello-world     latest   d1165f221234   9 days ago      13.3kB
```

This image file is built from an instructional file named **Dockerfile** that is parsed when you run docker image build.
Dockerfile is a file named **Dockerfile**, that looks something like this:
```
FROM <image>:<tag>

RUN <install some dependencies>

CMD <command that is executed on `docker container run`>
```
### Containers 
Containers only contain that which is required to execute an application; and you can start, stop and interact with them. They are **isolated** environments in the host machine with the ability to interact with each other and the host machine itself via defined methods (TCP/UDP).
## Docker CLI basics
The command line to interact with the **"Docker Engine"** that is made up of 3 parts: **CLI, a REST API **and Docker daemon. When you run a command, e.g. ```docker container run```
, behind the scenes the client sends a request through the REST API to the Docker daemon which takes care of images, containers and other resources.
### The most command lines 
| Command | Explain | Shorthand |
|------------------|------------------|------------------|
| ```docker image ls```  | Lists all images  | ```docker image```  |
| ```docker image rm <image>```  | Remove an image  | ```docker rmi``` |
| ```docker image pull <image>```  | Pulls images from a docker registry  | ```docker pull``` |
| ```docker container ls -a```  | Lists all containers  | ```docker rmi``` |
| ```docker container rm <container>```  | Removes a container  | ```docker run``` |
| ```docker container rm <container1> <container2>```  | Removes multiple containers  | ```docker run``` |
| ```docker container stop <container>```  | Stops a container  | ```docker stop``` |
| ```docker container exec <container>```  | Executes a command inside the container   | ```docker exec``` |
| ```docker container prune```  | Prune all containers  | ```docker container prune``` |

### Notice
#### Filter the lists of containers 
Run ```docker container ls -a``` to list all containers again.
```
$ docker container ls -a
  CONTAINER ID   IMAGE           COMMAND        CREATED          STATUS                      PORTS     NAMES
  b7a53260b513   hello-world     "/hello"       35 minutes ago   Exited (0) 35 minutes ago             brave_bhabha
  1cd4cb01482d   hello-world     "/hello"       41 minutes ago   Exited (0) 41 minutes ago             vibrant_bell
```
Containers have a **CONTAINER ID** and **NAME**. Use **grep** (or another similar utility) to filter the list:
```$ docker container ls -a | grep hello-world```

#### Remove container with the shorthand for the ID
- If a container's ID is **3d4bab29dd67**, you can use ```docker container rm 3d``` to delete the container with the ID of 3d4bab29dd67.
- If you have two IDs starting with 3d, a warning will be printed, and neither will be deleted.

### Starting a new container 
- Starting a new container with ```$ docker container run nginx```
- One can exit by pressing ```control + c``` and try again with the ```-d``` flag.
