# Architecture Big Picture

**Container** - isolated are of an OS with resources usage limits applied

![](/archictecture_and_theory/img/architecture-1.png)

___

## Kernel internals

### Namespaces

**Linux namespaces:**
- Process ID (pid)
- Network (net)
- Filesystem/mount (mnt)
- Inter-proc comms (ipc)
- UTS (uts) # hostname
- User (user)

Container - has its own group of namespaces (its secure)

### Control groups

- Grouping processes
- Imposing resource limits

![](img/architecture-kernel-internals.png)

## The Docker Engine

![](img/architecture-docker-engine.png)

## Windows Containers

![](img/architecture-containers-windows.png)
![](img/architecture-containers-windows-1.png)



