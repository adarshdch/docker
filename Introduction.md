
## Docker Concepts

Docker is a platform for developers and sysadmins to develop, deploy, and run applications with containers. The use of Linux containers to deploy applications is called containerization. Containers are not new, but their use for easily deploying applications is.

Containerization is increasingly popular because containers are:

- Flexible: Even the most complex applications can be containerized.
- Lightweight: Containers leverage and share the host kernel.
- Interchangeable: You can deploy updates and upgrades on-the-fly.
- Portable: You can build locally, deploy to the cloud, and run anywhere.
- Scalable: You can increase and automatically distribute container replicas.
- Stackable: You can stack services vertically and on-the-fly.

Docker is:

- Lighweight alternative of VMs
- No need to allocate RAM or disk space.
- Uses host operating system but guest os

## Docker Image

- Read Only template used to create Docker container
- Built by Docker users
- Stored in Docker hub or private repository


## Docker Images and containers

- A container is launched by running an image.
- An image is an executable package that includes everything needed to run an application--the code, a runtime, libraries, environment variables, and configuration files.

- A container is a runtime instance of an image--what the image becomes in memory when executed (that is, an image with state, or a user process). 
- You can see a list of your running containers with the command, ```docker ps```, just as you would in Linux.

## Containers and virtual machines

- A container Isolated application platform
- A container contains everything needed to run application
- A container is built by layering multiple Docker images

- A container runs natively on Linux and shares the kernel of the host machine with other containers. 
- It runs a discrete process, taking no more memory than any other executable, making it lightweight.

- By contrast, a virtual machine (VM) runs a full-blown “guest” operating system with virtual access to host resources through a hypervisor.
- In general, VMs provide an environment with more resources than most applications need.

# Docker Registry

- A storge component for Docker Images
- It can be public / private
- <a href="https://hub.docker.com">Docker Hub</a> is Docker's cloud repository for Docker Images.

## Prepare your Docker environment

- Install Docker from <a href="https://docs.docker.com/engine/installation/">https://docs.docker.com/engine/installation/</a>
- Test Docker Version using ```docker version``` and ```docker --version```
- Run ```docker info``` to know more details
- Test Docker installation by running command ```docker run hello-world```
- List the local images ```docker image ls```
- List the containers ```docker container ls --all```

## Docker Cheat Sheet 

```
## List Docker CLI commands
docker
docker container --help

## Display Docker version and info
docker --version
docker version
docker info

## Execute Docker image
docker run hello-world

## List Docker images
docker image ls

## List Docker containers (running, all, all in quiet mode)
docker container ls
docker container ls --all
docker container ls -aq
```

## What problem Docker tries to solve?

An application might work in Dev environment but not in other environments like QA, UAT, or PROD. What might be the reason? Obviously, the difference between environment configurations.

## How Docker helps with Microservices? 

For a particular application, there may be n number of microservices. It is not possible to create that many VMs.

## What are main advantage of Microservice?

- Maintenability
- Easy to update particular application/microservice environment
- Application down risk

##  How Docker solves the problem?

- You can run multiple microservices in the same VM by running multiple docker container for the microservices.

- Consistent computing environment

## Docker Lifecycle

- Docker file builds a docker image
- Docker image contains all the project's codebase
- Docker image can be used to create multiple copy of Docker container
- Docker image is uploaded to Docker hub
- Anyone can pull image from Docker hub and build the container



| References

- https://docs.docker.com/get-started/