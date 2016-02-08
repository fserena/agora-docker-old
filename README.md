# agora-docker
Compose file and resources to deploy Agora in a Docker host.

## Requirements
* Docker > 1.7.0
* Docker-compose > 1.3.1

##Containers
The  main container here is the one that hosts Agora. Two more are included in order to provide a Redis DB for Agora and a nginx.

|Container|Image|Ports|
|:---------|:----------|:----------|
|redis|redis|
|core|smartdeveloperhub/agora|
|nginx|xdrum/nginx-extras|80 -> **9002**|

Once everything is up and running, Agora will listen on port 9002.

##Commands
Docker-compose provides the following commands to enable interaction with all containers:

|Action|Command|
|:---------|:----------|
|Build|```docker-compose build```|
|Create|```docker-compose up -d```|
|Start|```docker-compose start```|
|Stop|```docker-compose stop```|
|Delete|```docker-compose rm -f```|

Of course, container-based commands (selective) are also available (see https://docs.docker.com/compose/overview/).




