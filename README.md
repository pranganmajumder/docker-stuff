## Docker Basic Command
| Commands                 |                 Use                    |
|-----------------------------|----------------------------------------|
|```ps aus```|To see which process is currently running in your pc|
|```ip addr show```|To see the ethernet card in your machine including virtual ethernet card|
|``` users``` or ```sudo users```|To see the users, user id of the root user |
|``` id -u```| To get user ID|
|``` id -g```|To get group Id|
|``` docker ps```|To see all the containers running in your machine|
|``` docker ps -a```|To see the all available docker container in your machine with specific details|
|```docker images ```|To see the all the images available in your machine|
|``` docker start container_id```|to start a container|
|```docker stop container_id ```|To stop the running container|
|```docker rm container_id ```|To remove a docker container|
|``` docker inspect container_id```|To see full information about the container, it'll return json file|
|``` docker exec -it container_id sh```|To enter a container which id is container_id in shell</br> N.B: if the container is not running then run the start command before |
|``` docker exec -it container_id bash```|To enter a container which id is container_id in bash|
|```exit ```|To exit from docker container|
|```ls -l ```||
|``` hostname```|To see the hostname/container_id|
|```route -n ```|To see the routing table of the container|
|```docker build -t <give_image_name> "location of Dockerfile" ```</br> Ex: If you are in your project directory </br>```docker build -t <give_image_name> .```|To build the docker image from the Dockerfile </br> N.B : imageName should be in lowercase|
|``` docker run -d -p 8080:8080 <given_image_name>```|To run the docker image with the port mapping and in detached mode.</br> First one is host port , second one is container port. </br> It will create container name anonymously|
|``` docker run -d -p 8080:8080 --name <give_container_name> <given_image_name>```|using name flag to give a name to the container. </br> Container name will be created as you will give here|
|``` docker image ls```|To see the list of all the available images in your machine with their tag, image id, creatiion time and size|
|```delete rm container_id ```|To delete a specific container which id container_id|
|``` delete rmi image_id```|To delete a specific image|
|``` delete rmi image_id```|To delete a specific image|
|``` delete rmi -f image_id```|force to delete a specific image|
|`docker rm -f (docker ps -a `&#124;` awk '{print $1}')` |To delete all the docker container available in your machine. </br> N.B: Works in fish, not bash|
|`docker rm -vf $(docker ps -a -q)`|To delete all containers including its volumes use|
|`docker rmi -f $(docker images -a -q)`|To delete all the images|
|`docker rmi -f (docker images `&#124;` awk '{print $3}')` |To delete all the docker images available in your machine. </br> N.B : Works in fish, not bash|
|`docker rmi -f (docker images `&#124;` grep none `&#124;` awk '{print $3}')` |To delete all the "none" docker images available in your machine. </br> N.B : Works in fish , not bash|
|`grep`|to select|
|`docker container prune`|To delete the all the stopped container available on your machine|

###### push a image : 
`docker tag <img id> pranganmajumder/customImage:1.0` </br>
`docker push pranganmajumder/customImage:1.0`



