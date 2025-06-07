screenshots :
![Screenshot (272)](https://github.com/user-attachments/assets/761a462a-653b-47ff-bc18-6db0ad365e5a)
![1](https://github.com/user-attachments/assets/20875d84-7ea6-4dc5-bd5d-a30cb29bae50)

list of the Docker commands:

#docker pull nginx

#docker images

#start containers:
docker run --name firstContainer -p 80:80 nginx
docker ps -a
docker run --name secondContainer -p 80:80 nginx
docker ps -a

#View the container’s logs:
docker logs firstContainer
docker logs secondContainer

#Stoping the containers:
docker stop firstContainer
docker stop secondContainer

#cleaning up the stopped containers:
docker rm firstContainer
docker rm secondContainer


Reflection Questions:
1. What is the difference between a Docker image and a Docker container? Explain in your own words.
Images in Docker contain all the files, libraries, and settings that a program needs to run and cannot be changed, but containers in Docker are responsible for running images, meaning that when we run an image, a container is actually created from that image that can work independently of other containers.
2. Why might you see an error like “port already in use” when running a container, and how can you fix it?
When we encounter this message(port already in use), it means that our container is trying to connect to the port we requested, but the port is currently in use by another application or container.
We can check the status of running containers using the # docker ps -a # command, and then stop the containers using the port  with the # docker stop # command.
Or remove them entirely using the # docker rm # command.
3. How does the docker logs command help you when working with containers?
Overall, the docker logs command is a very useful tool that helps us monitor errors and application behavior in containers. It makes it easier to troubleshoot and maintain containers and can help improve the stability and performance of your applications.

Challenges Faced:
When I created the first container in order, I stopped it with the control-c command to create the second container if it was not necessary. So when I wanted to view the two containers on the specific ports that I had written for each, I encountered a problem in the browser and when I checked the status of the containers with the #docker ps -a# command, I saw that the status of both was Exited. I had to completely delete both and create them again yo fix the problem.
