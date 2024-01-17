## Images and containers 
- Containers are instances of images. A container = a ready-to-eat meal. An image = the recipe or ingredients for that meal.
-  You need **an image** and **a container runtime (Docker engine)** to create a container. The image provides all the necessary instructions and dependencies for the container to run, just like a recipe provides the steps and ingredients to make a meal.

### Images 
- A Docker image is a file.
- An image can never be changed after they are created
- List all your images with ```docker image ls```

```$ docker image ls
  REPOSITORY      TAG      IMAGE ID       CREATED         SIZE
  hello-world     latest   d1165f221234   9 days ago      13.3kB
```

This image file is built from an instructional file named **Dockerfile** that is parsed when you run docker image build.
Dockerfile is a file named **Dockerfile**, that looks something like this:
```FROM <image>:<tag>

RUN <install some dependencies>

CMD <command that is executed on `docker container run`>
```
