# Docker-learning repo
Repo records the projects in [udemy course - docker and kubernetes: the complete guide](https://www.udemy.com/course/docker-and-kubernetes-the-complete-guide/learn/lecture/11437094#overview)

## Commonly Used Commands

| Commands  | Notes |
| ------------------- | ------------- |
| docker ps  |  to list running containers  |
| docker ps --all  | to list all containers  |
| docker create <image_name>  |  create container (only prepares the file system)  |
| docker start (-a) <container_id>  | run container (restart)<br /> runs the startup command<br /> `-a` indicates whether to show the output  |
| docker system prune  |  remove stopped containers  |
| docker logs <container_id>  | retrieve log outputs  |
| docker stop <container_id>  |  stop a container  |
| docker kill <container_id>  | immediately kill a container  |
| docker exec -it <container_id> command  |  execute commands in running containers <br /> `-i` attache terminal to stdin <br /> `-t` all the text entered & shows out are in well-formatted way  |
| docker exec -it <container_id> sh   | getting a command prompt in a container <br /> command processer can be [bash; powershell; zsh; sh]  |
| docker run -it <container_id> sh   | start your container with a shell  |
| docker build -t <docker_id/repor_project_name:version> .   | tag your image with a specified name  |