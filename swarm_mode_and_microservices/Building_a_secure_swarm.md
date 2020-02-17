# Building a Secure Swarm

![](/swarm_mode_and_microservices/img/swarm-cluster.png)

## Swarm Clustering Deep Dive

![](/swarm_mode_and_microservices/img/swarm-raft-consensus-group.png)

## Building a Secure Swarm

**Create a Swarm**

- Create a Swarm manager
	- Assign it a crypto
	- Elect is as the Swarm leader
- Create a Swarm config DB
	- Encrypt it
	- Configure it to automatically replicate with all Swarm managers
- Create a Swarm join token for new workers
- Create a Swarm join token for new manager
- Configure a new Root CA on the leader
	- Configure a 90 day certificate rotation period

**Lock your Swarm wiyh Autolock**

`docker swarm update --autolock=true`

## Orchestaration 

![](/swarm_mode_and_microservices/img/swarm-orchestration.png)

## Recap

![](/swarm_mode_and_microservices/img/swarm-secure-recap.png)



