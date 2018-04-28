https://stackoverflow.com/questions/37966552/what-is-the-difference-between-docker-and-docker-compose

The`docker`cli is used when managing individual containers on a docker engine. It is the client command line to access the docker daemon api.

The`docker-compose`cli can be used to manage a multi-container application. It also moves many of the options you would enter on the`docker run`cli into the`docker-compose.yml`file for easier reuse. It works as a front end "script" on top of the same docker api used by`docker`, so you can do everything`docker-compose`does with`docker`commands and a lot of shell scripting.

**Update for Swarm Mode**

Since this answer was posted, docker has added a second use of docker-compose.yml files. Starting with the[version 3 yml format](https://docs.docker.com/compose/compose-file/compose-versioning/)and docker 1.13, you can use the yml with docker-compose and also to define a stack in docker's swarm mode. To do the latter you need to use`docker stack deploy -c docker-compose.yml $stack_name`instead of`docker-compose up`and then manage the stack with`docker`commands instead of`docker-compose`commands. The mapping is a one for one between the two uses:

* Compose Project -
  &gt;
   Swarm Stack: A group of services for a specific purpose
* Compose Service -
  &gt;
   Swarm Service: One image and it's configuration, possibly scaled up.
* Compose Container -
  &gt;
   Swarm Task: A single container in a service

  


