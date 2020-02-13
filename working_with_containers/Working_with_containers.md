# What is container
______

![](/working_with_containers/img/container-desc.png)
![](/working_with_containers/img/container-depth-desc.png)

______

**Main commands list:**

- `docker version`
- `docker info`
- `docker images` - to see info about images
- `docker run` - to run a container
- `docker ps` - to see running and stopped containers

______

Installing Docker gives you the **client** and **daemon**

Client makes API calls to daemon

Daemon implements the Docker Remote API

`docker run` starts a new container

**Docker Hub** is the default public registry

The daemon will `pull` images that it doesn't already have

Images <-> Stopped containers
Containers <-> Running Images

To remove containren - `docker rmi <container-name>`

## Docker container **LIFECYCLE**

- `docker start <cintainer>`
- `docker stop <container>`
- `docker rm <container>`


![](/working_with_containers/img/containers-lifecycle.png)
![](/working_with_containers/img/container-ports.png)
**Images level**
![](/working_with_containers/img/container-images-level.png)

Container often is single process constructs.

Stop all docker containers: `docker stop $(docker ps -aq)`
Remove all containers: `docker rm $(docker ps -aq)`
Remove all images: `docker rmi $(docker images -q)`

______

![](/working_with_containers/img/container-modernize-apps.png)

Stoping and restarting container don't destroy any data

`CTRL+P+Q` - exit without destroying the main process

## Logging

Linux:
- systemd:
	- journalctl -u docker.service
- Non-systemd:
	Try /var/log/messages

Windows:
	~/AppData/Local/Docker


![](/working_with_containers/img/container-logging.png)



