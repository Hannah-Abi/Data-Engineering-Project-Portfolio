# Basic concepts 
## What is DevOps?
- The term itself consists of two parts, Dev and Ops. Dev refers to the development of software and Ops to operations. Simple definition for **DevOps** would be that it means the **release, configuring, and monitoring of software** is in the hands of the very people who develop it.
- During this course we will focus mainly on the packaging, releasing and configuring of the applications.

## What is Docker?
"Docker is **a set of platform as a service (PaaS)** products that use OS-level virtualization to deliver software in packages called containers." - from Wikipedia.
- Docker is a set of tools to deliver software in containers.
- Containers are packages of software.
- Illustration of a container

## Benefits from Containers
Containers play a crucial role in application packaging, offering various advantages in different scenarios.

### **Scenario 1: "Works on my machine"**
- The 'works on my machine' issue occurs when software is developed on a personal machine but encounters issues when deployed on server computers.
- Containers address this problem by enabling developers to run the application personally within a container. This container encapsulates all the dependencies necessary for the application to function.

### **Scenario 2: Isolated Environments**
- Imagine having 5 different Python applications that need to be deployed to a server requiring Python 2.7, while none of your applications are compatible with this version.
- Containers resolve this challenge by packaging each software along with its dependencies. This way, you package the existing app and the 5 new ones with their respective Python versions.

### **Scenario 3: Development**
- Joining a development team working on a web app with multiple dependencies (e.g., Postgres database, MongoDB, Redis) used to be a complex setup process.
- Containers simplify this process. With a single command, you can have an isolated application, such as Postgres or Mongo, running on your machine.

### **Scenario 4: Scaling**
- Initiating and stopping a Docker container involves minimal overhead. However, when dealing with large-scale applications like Netflix or Facebook, meeting changing demand becomes crucial.
- Advanced tooling, covered in parts 2 and 3, allows the instant creation of multiple containers and efficient load balancing to handle increased traffic.



