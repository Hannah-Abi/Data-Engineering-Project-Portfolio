# Command lines for running and stopping containers
Command                                   | Explain                                                              | Shorthand              
-------------------------------------------|----------------------------------------------------------------------|------------------------
```docker run ubuntu```                       | Start Ubuntu container                                               | -                      
```docker run -t ubuntu```                    | Start interactive Ubuntu container with ```tty```                          | -i, -t                 
```docker run -it ubuntu```                   | Start interactive Ubuntu container with tty and pass STDIN           | -i, -t                 
```docker run -d -it --name looper ubuntu sh -c 'while true; do date; sleep 1; done'``` | Run detached interactive container with a loop    | -d, -i, -t, --name     
```docker container ls```                     | List running containers                                              | -                      
```docker logs -f looper```                   | Follow logs of the "looper" container                                 | -f                     
```docker pause looper```                     | Pause the "looper" container                                          | -                      
```docker unpause looper```                   | Unpause the "looper" container                                        | -                      
```docker attach looper```                    | Attach to the "looper" container's STDOUT                            | -                      
```docker attach --no-stdin looper```         | Attach to the "looper" container without closing from other terminal | --no-stdin              
```docker start looper```                     | Start a stopped container named "looper"                              | -                      
```docker attach --no-stdin looper```         | Attach to the running "looper" container without closing from another terminal | --no-stdin     
```docker exec -it looper bash```             | Execute bash inside the "looper" container                            | -i, -t                 

## 1. Running Ubuntu Container:
   - Executing ```docker run ubuntu``` starts an Ubuntu container, downloading the image if not available locally.
   - Adding flags, such as ```-t``` for a ```tty```, enables interaction with the container.

## 2. Interacting with Containers:
   - Using ```-i``` to pass STDIN to the container and ```-d``` to run it in detached mode.
   - Demonstrating practical examples of running a detached container named "looper" with an infinite loop.
   - Employing ```docker logs -f looper``` to follow the continuous output of the container.

## 3. Pausing and Attaching:
   - Pausing a container with ```docker pause looper``` and resuming with ```docker unpause looper```.
   - Exploring the use of ```docker attach looper``` to connect to the running container and detach with ```Ctrl+C```.

## 4. Container Execution:
   - Introducing ```docker exec -it``` to execute commands within a running container (e.g., ```docker exec -it looper bash```).

## 5. Stopping and Removing Containers:
   - Stopping and removing containers using ```docker stop looper``` followed by ```docker rm looper```.
   - Explaining that ```docker kill``` and ```docker rm``` can be combined as ```docker rm --force```.

## 6. Automated Container Removal:
   - Launching a container with ```--rm``` to automatically remove it after it exits.
   - Demonstrating how ```Ctrl+C``` sends a kill signal followed by container removal.

## 7. Ubuntu in a Container:
   - Illustrating that running an Ubuntu image in a container provides a working Ubuntu environment.
   - Installing additional tools like Nano using ```apt-get```.




```markdown
## Running and Stopping Containers

### Running Containers

To run a useful image, such as Ubuntu, use the following command:

```bash
$ docker run ubuntu
```

This downloads and runs the Ubuntu image, but it's non-interactive. To interact with it, use the following command:

```bash
$ docker run -t ubuntu
```

For an interactive and attached session, use:

```bash
$ docker run -it ubuntu
```

Now, you're inside the container and can execute commands like `ls`.

### Running in the Background

To run a container in the background and keep it running, use:

```bash
$ docker run -d -it --name looper ubuntu sh -c 'while true; do date; sleep 1; done'
```

This command creates a detached container named "looper" running a continuous date-printing script.

### Pausing and Attaching

You can pause the running container without stopping it:

```bash
$ docker pause looper
```

To unpause:

```bash
$ docker unpause looper
```

To attach to the running container and see logs:

```bash
$ docker attach looper
```

### Stopping and Restarting

To stop the container gracefully:
```
$ docker stop looper
```

If you want to attach to a running container without closing it in the other terminal:

```
$ docker attach --no-stdin looper
```

### Executing a New Process

To enter a container and start a new process:

```
$ docker exec -it looper bash
```

This opens a bash shell inside the running container.

### Killing and Removing Containers

To forcefully stop and remove a container:

```
$ docker kill looper
$ docker rm looper
```

### Automatically Removing Containers

To run a container that removes itself after exiting:

```
$ docker run -d --rm -it --name looper-it ubuntu sh -c 'while true; do date; sleep 1; done'
```

This auto-removing container ensures no leftover containers.

### Detaching from STDOUT

To detach from STDOUT without stopping the container:

```
$ docker attach looper-it
```
Press `Ctrl + P, Ctrl + Q` to detach.
```
