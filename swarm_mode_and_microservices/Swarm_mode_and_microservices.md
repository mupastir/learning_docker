# Swarm mode and microservices

##Terminology##

- A cluster = A swarm

Engines in a swarm run in **swarm mode**

**Manager nodes** maintain the swarm (
	- H/A - recommended 3 or 5
	- Only one is **leader**
)

**Worker nodes** execute tasks

**Services**
	- Declarative & scalable

**Tasks**
	- Assigned to workers
	- <-> containers
___

## Configuring swarm mode
___

`docker swarm init --advertise-addr <ip>:<port> --listen-addr <ip>:<port>`

![](/swarm_mode_and_microservices/img/swarm-ports.png)

`docker swarm join-token manager`
`docker swarm join-token worker`

The Docker swarm is a collection of one or more machines (physical or virtual, called nodes) that can run your containers as services. Nodes in the swarm can be managers or workers. Only on manager nodes can you see/modify the swarm status. Worker nodes only run containers. In order to run a container in the swarm you must create a service; that service will have zero or more containers depending on the scale that you set for the service.

To create a swarm, you run the docker swarm init on the machine that will be a manager node. Then, on the other machines that you own you run the docker swarm join command in order to add them to the swarm. 

___

## Services

- Declarative
- Desired state
- Actual state

![](/swarm_mode_and_microservices/img/services-managing.png)

`docker service inspect <service_name>`

`docker service create --update-parallelism 2 --update-delay 10s`

___

## Stacks and Bundels (DABs)

Stack ~ application comprising multiple services
(deployed from distributed application bundles (DAB)

`docker stack`

- `docker-compose build`
- `docker-compose bundle` (to get <app>.dab)
- `docker stack deploy <app>
- `docker service ls`
- `docker stack tasks services

**Check latest docs of Docker stack**

___

## Recap

![](/swarm_mode_and_microservices/img/swarm-recap.png)

