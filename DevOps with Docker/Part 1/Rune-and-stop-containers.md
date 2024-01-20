
**Summary of the Lecture: Running and Stopping Containers**

This lecture focused on essential aspects of running and managing containers using Docker. Here's a breakdown of key points:

1. **Running Ubuntu Container:**
   - Executing 
   ```bash
   docker run ubuntu
   ``` 
   starts an Ubuntu container, downloading the image if not available locally.
   - Adding flags, such as `-t` for a tty, enables interaction with the container.

2. **Interacting with Containers:**
   - Using `-i` to pass STDIN to the container and `-d` to run it in detached mode.
   - Demonstrating practical examples of running a detached container named "looper" with an infinite loop.
   - Employing 
   ```bash
   docker logs -f looper
   ```
   to follow the continuous output of the container.

3. **Pausing and Attaching:**
   - Pausing a container with 
   ```bash
   docker pause looper
   ```
   and resuming with 
   ```bash
   docker unpause looper
   ```.
   - Exploring the use of 
   ```bash
   docker attach looper
   ```
   to connect to the running container and detach with `Ctrl+C`.

4. **Container Execution:**
   - Introducing 
   ```bash
   docker exec -it
   ``` 
   to execute commands within a running container (e.g., 
   ```bash
   docker exec -it looper bash
   ```).

5. **Stopping and Removing Containers:**
   - Stopping and removing containers using 
   ```bash
   docker stop looper
   ``` 
   followed by 
   ```bash
   docker rm looper
   ```.
   - Explaining that 
   ```bash
   docker kill
   ```
    and 
   ```bash
   docker rm
   ``` 
   can be combined as 
   ```bash
   docker rm --force looper
   ```.

6. **Automated Container Removal:**
   - Launching a container with 
   ```bash
   --rm
   ``` 
   to automatically remove it after it exits.
   - Demonstrating how `Ctrl+C` sends a kill signal followed by container removal.

7. **Exercise 1.3: Secret Message:**
   - Involves running a container (
   ```bash
   devopsdockeruh/simple-web-service:ubuntu
   ```) 
   that outputs logs.
   - Using 
   ```bash
   tail -f ./text.log
   ``` 
   to follow logs and receive a "secret message" every 10 seconds.

8. **Ubuntu in a Container:**
   - Illustrating that running an Ubuntu image in a container provides a working Ubuntu environment.
   - Installing additional tools like Nano using 
   ```bash
   apt-get

**Command Line Table for README.md:**

```markdown
| Command                                   | Explain                                                              | Shorthand              |
|-------------------------------------------|----------------------------------------------------------------------|------------------------|
| ```docker run ubuntu```                       | Start Ubuntu container                                               | -                      |
| ```docker run -t ubuntu```                    | Start interactive Ubuntu container with tty                          | -i, -t                 |
| ```docker run -it ubuntu```                   | Start interactive Ubuntu container with tty and pass STDIN           | -i, -t                 |
| ```docker run -d -it --name looper ubuntu sh -c 'while true; do date; sleep 1; done'``` | Run detached interactive container with a loop    | -d, -i, -t, --name     |
| ```docker container ls```                     | List running containers                                              | -                      |
| ```docker logs -f looper```                   | Follow logs of the "looper" container                                 | -f                     |
| ```docker pause looper```                     | Pause the "looper" container                                          | -                      |
| ```docker unpause looper```                   | Unpause the "looper" container                                        | -                      |
| ```docker attach looper```                    | Attach to the "looper" container's STDOUT                            | -                      |
| ```docker attach --no-stdin looper```         | Attach to the "looper" container without closing from other terminal | --no-stdin              |
| ```docker start looper```                     | Start a stopped container named "looper"                              | -                      |
| ```docker attach --no-stdin looper```         | Attach to the running "looper" container without closing from another terminal | --no-stdin     |
| ```docker exec -it looper bash```             | Execute bash inside the "looper" container                            | -i, -t                 |
| ```docker kill looper```                      | Kill the "looper" container                                           | -                      |
| ```docker rm looper```                        | Remove the "looper" container                                         | -                      |
| ```docker run -d --rm -it --name looper-it ubuntu sh -c 'while true; do date; sleep 1; done'``` | Run detached container with auto-removal  | -d, --rm, -i, -t, --name |
```
