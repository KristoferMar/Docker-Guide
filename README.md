# Docker-Guide

- Containerization means that we seperate every single application into it's own mini OS (container) which gives us the oppertuinity to use applications on Mac, Windows & Linux seperatly from the individual OS of the machine. 
- Check if you docker is working by executing the following docker command <i> sudo docker run docker/whalesay cowsay hello-world! </i>. This will pull the docker image from https://hub.docker.com/r/docker/whalesay .. build the container and execute the script. 

## Commonly used docker dommands 

Run given container <br>
<i>docker run 'your_docker_image'</i>

Stop given container <br>
<i>docker stop container_name</i>

Compleatly remove docker container. 
<i> docker rm container_name </i>

See all running containers <br>
<i> docker container ls -a </i>

Pause docker container <br>
<i> docker pause my_container </i>

Print content on running container <br>
<i>docker exec 'container_name' cat /etc/hosts </i>

### Images

See list of docker images <br>
<i>docker images </i>

Pull an image without running container <br>
<i>docker pull 'image_name' </i>

Remove docker image <br>
<i> docker rmi 'Your_Image' </i>
