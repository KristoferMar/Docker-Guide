<h1>Docker-Guide</h1>

- Containerization means that we seperate every single application into it's own mini OS (container) which gives us the oppertuinity to use applications on Mac, Windows & Linux seperatly from the individual OS of the machine. <br>
- Check if you docker is working by executing the following docker command <i> sudo docker run docker/whalesay cowsay hello-world! </i>. This will pull the docker image from https://hub.docker.com/r/docker/whalesay .. build the container and execute the script. <br>

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

<h4>Remove given container </h4>
<i>docker rm container_name</i>

<h4>Compleatly remove docker container. </h4>
<i> docker rm container_name </i>

<h4>See status list of all running containers</h4>
<i> docker container ls -a </i>

<h4>Pause docker container </h4>
<i> docker pause my_container </i>

<h4>Print content on running container</h4>
<i>docker exec 'container_name' cat /etc/hosts </i>

<h4>Get data on running containers</h4>
<i>docker inspect 'container' </i>

<h4>Get logs of a specific container</h4>
<i>docker logs 'container_id'</i>

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
The docker registry is the central repository for all containers. <br>
- The registry can be understanded like github.. We have private and public registries which are all stored on the central docker registry. <br>
- Images can be pulled aswell as pushed to a docker registry. <br>


<h1>Kubernetes</h1>

- It's an open-source system for automating deployment, scaling, and management of containerized applications.
- kubectl CLI is the interface we use 

<h2>Namespaces</h2>

- Veritulaization of phusical cluster
- Segregate cluster by team, project, etc
- Necessary with larger numbers of users

<h3>names</h3>

- Each objects has a name 
- Names are unique for a resource type within a namespace 

<h2>Pod</h2>
- Simplest unit in Kubernetes 
- Represent processes running in your cluster 
- Encapulsates a container (or sometimes multiple)
- Replciating a Pod serces to scale a application horizontally. 

<h2>Deployment</h2>
- Provides updates for Pods and ReplicaSets
- Runs multiple replicas of your application
- Suitable for stateless applications
- Update triggers a rollout

<br><br>
<h2>Commands</h2>
retrieves the Secrets in the “default” namespace <br>
- kubectl get secrets --namespace=default