# Docker-Guide

- Containerization means that we seperate every single application into it's own mini OS (container) which gives us the oppertuinity to use applications on Mac, Windows & Linux seperatly from the individual OS of the machine. 
- Check if you docker is working by executing the following docker command <i> sudo docker run docker/whalesay cowsay hello-world! </i>. This will pull the docker image from https://hub.docker.com/r/docker/whalesay .. build the container and execute the script. 

<h2>Commonly used docker dommands </h2>

See all running containers <br>
- Attach '-a' to see all containers <br>
<i>docker ps</i> <br>

Run given container <br>
- Attach '-d' to run container in background<br>
- Attach '-p 80:5000' to run container on specific port
<b><i>docker run 'your_docker_image'</i></b>

<p id="stopContainer"><b>Stop given container</b></p>
<i>docker stop container_name</i>
<br>

<h5>Restart docker container</h5>
<i>docker restart 'container_id'</i><br>
<p>Restart all containers</p>
<i>docker restart $(docker ps -q)</i><br><br>

<b>Remove given container <br> </b>
<i>docker rm container_name</i>

Compleatly remove docker container. 
<i> docker rm container_name </i>

See status list of all running containers <br>
<i> docker container ls -a </i>

Pause docker container <br>
<i> docker pause my_container </i>

Print content on running container <br>
<i>docker exec 'container_name' cat /etc/hosts </i>

Get data on running containers <br>
<i>docker inspect 'container' </i>

### Images

Images are used to dockerize applications so we are able to boot them up in docker inside a container.

See list of docker images <br>
<i>docker images </i>

Pull an image without running container <br>
<i>docker pull 'image_name' </i>

Remove docker image <br>
<i> docker rmi 'Your_Image' </i>

### Compose 

docker-compose-yml file is the configuration file for our docker file. 

We can make use of the docker compose file to compose multiple applications together and host an entire system with docker. This can include a DB, a front-end and back-end for instance. 

### Docker registry
The docker registry is the central repository for all containers. The registry can be understanded like github.. We have private and public registries which are all stored on the central docker registry. 
