Docker Up And running -

**Docker client  
**

The docker command used to control most of the Docker workflow and  
  talk to remote Docker servers.

**Docker server  
**

It is nothing but a docker daemon , typically started using docker -d command , then the daemon will start and will be in listeing mode waiting for incoming requests from the docker client .The docker command run in daemon mode. This turns a Linux system into  a Docker server that can have containers deployed, launched, and torn  down via a remote client.

**Docker images  
**

Docker images consist of one or more filesystem layers and some important  metadata that represent all the files required to run a Dockerized  application. A single Docker image can be copied to numerous hosts. A  container will typically have both a name and a tag. The tag is generally  used to identify a particular release of an image.

**Docker container  
**

A Docker container is a Linux container that has been instantiated from a  Docker image. A specific container can only exist once; however, you can  easily create multiple containers from the same image.

**Atomic host  
**

An atomic host is a small, finely tuned operating system image, like  CoreOS and Project Atomic, that supports container hosting and atomic OS  upgrades.

