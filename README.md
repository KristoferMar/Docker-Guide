# Docker-Guide

- Containerization means that we seperate every single application into it's own mini OS (container) which gives us the oppertuinity to use applications on Mac, Windows & Linux seperatly from the individual OS of the machine. 
- Check if you docker is working by executing the following docker command <i> sudo docker run docker/whalesay cowsay hello-world! </i>. This will pull the docker image from https://hub.docker.com/r/docker/whalesay .. build the container and execute the script. 

## Commonly used docker dommands 

See all running containers <br>
<i> docker container ls -a </i>

Pause docker container <br>
<i> docker pause my_container </i>
