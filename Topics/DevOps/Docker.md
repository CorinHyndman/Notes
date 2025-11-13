___
## What is Docker

Docker is an open-source platform that enables developers to build, deploy, run, update, and manage containers.

## What is a Container

A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. Containers isolate the software from the environment, ensuring consistency. In this instance, this is done using a Docker image.

## What is a Docker Image

A Docker image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries, and settings. A Docker image is the blueprint or template, while a container is the running instance of that image.

## From Image to Container

Container images become containers at runtime. In the case of Docker, images become containers when they run on the Docker Engine. The Docker Engine will always run the same regardless of the underlying infrastructure.

## Deeper Look at Containers

Containers are an abstraction at the application layer that packages code and dependencies together. Multiple containers can run on the same machine and share the OS kernel with other containers, each running as isolated processes in user space. Containers take up less space than virtual machines (container images are typically tens of MBs in size), can handle more applications, and require fewer VMs and operating systems.

## Docker Components

- **Docker file**: A text file containing instructions to build a Docker image (e.g., base image, dependencies, commands).
- **Docker Registry**: A public or private registry used to store and share Docker images. 
- **Docker Hub**: It is the official cloud-based Docker Registry service provided by Docker Inc. It is the default registry where Docker looks for images when you run `docker pull` or `docker run` without specifying a registry.
- **Docker Engine / Host**: The runtime that builds and runs Docker containers.

## Key Benefits of Docker

- **Portability**: Runs the same across any system.
- **Efficiency**: Lightweight and uses fewer resources than VMs.
- **Scalability**: Works well with orchestration tools such as Kubernetes.
- **Speed**: Faster startup compared to virtual machines.

## Docker vs Virtual Machines

- **Virtual Machines** run a full guest operating system on top of a hypervisor.
- **Containers** share the host OS kernel, making them lighter, faster, and more efficient.
___
![[how-does-docker-work.png]]
![[must-know-docker-concepts.png]]
___
## Flashcards
#flashcards
What is Docker? :: Docker is an open-source platform that enables developers to build, deploy, run, update, and manage containers.

What is a container? :: A container is a standard unit of software that packages code and all its dependencies so the application runs reliably across different computing environments; containers isolate the software from the environment.

What is a Docker image? :: A Docker image is a lightweight, standalone, executable package that includes everything needed to run an application (code, runtime, system tools, libraries, and settings).

What is the difference between an image and a container? :: An image is the immutable blueprint or template; a container is the running instance created from that image.

How do you build a Docker image? :: Use `docker build -t image_name .` to build an image from a Dockerfile.

How do you run a container from an image? :: Use `docker run -p host:container image_name` to start a container and map ports.

How do you see running containers? :: Use `docker ps` to list running containers.

How do you see all containers (including stopped ones)? :: Use `docker ps -a`.

How do you list all Docker images? :: Use `docker images`.

How do you remove a container? :: Use `docker rm container_name_or_id`.

How do you remove an image? :: Use `docker rmi image_name_or_id`.

How do you open an interactive shell in a running container? :: Use `docker exec -it container_name /bin/sh`.

How do you view logs from a container? :: Use `docker logs container_name`.

How do you inspect a container or image for details? :: Use `docker inspect container_or_image_name`.

What is the Docker Engine? :: The runtime that builds and runs containers, ensuring consistency across any system.

What is a Dockerfile? :: A text file with instructions to build a Docker image, including base image, dependencies, and commands.

What is a Docker Registry? :: A public or private registry used to store and share Docker images.

Why are containers more efficient than virtual machines? :: Containers share the host OS kernel, take up less space, start faster, and can run more applications per system.

What are the main benefits of Docker? :: Portability, efficiency, scalability, and speed.

How do containers differ from virtual machines? :: Virtual machines run a full guest OS on a hypervisor; containers share the host OS kernel, making them

