# Basic concepts 
## What is DevOps?
- The term itself consists of two parts, Dev and Ops. Dev refers to the development of software and Ops to operations. Simple definition for **DevOps** would be that it means the **release, configuring, and monitoring of software** is in the hands of the very people who develop it.
- During this course we will focus mainly on the packaging, releasing and configuring of the applications.

## What is Docker?
"Docker is **a set of platform as a service (PaaS)** products that use OS-level virtualization to deliver software in packages called containers." - from Wikipedia.
- Docker is a set of tools to deliver software in containers.
- Containers are packages of software.
- Illustration of a container

## Benefits from containers
Containers package applications. Sounds simple, right? To illustrate the potential benefits let's talk about different scenarios.
### **Scenario 1: Works on my machine**
- The 'works on my machine' issue happens when the software deveoped in personal machine but not in the server's computers. 
Let's first take a closer look into what happens in web development without containers following the chain above starting from "Plan".
- Containers solve this problem by allowing the developer to personally run the application inside a container, which then includes all of the dependencies required for the app to work.
### **Scenario 2: Isolated environments**
You have 5 different Python applications. You need to deploy them to a server that already has an application requiring Python 2.7 and of course none of your applications are 2.7. What do you do? Since containers package the software with all of its dependencies, you package the existing app and all 5 new ones with their respective Python versions and that's it.

### **Scenario 3: Development**
You are brought into a dev team. They run a web app that uses other services when running: a Postgres database, MongoDB, Redis and a number of others. Simple enough, you install whatever is required to run the application and all of the applications that it depends on...
With one command you get an isolated application, like Postgres or Mongo, running in your machine.

4. **Scenario 4: Scaling**
Starting and stopping a Docker container has little overhead. But when you run your own Netflix or Facebook, you want to meet the changing demand. With some advanced tooling that we will learn about in parts 2 and 3, we can spin up multiple containers instantly and load balance traffic between them.

# Running containers 
un docker container run hello-world,



