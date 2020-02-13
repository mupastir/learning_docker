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

![](/archictecture_and_theory/img/architecture-kernel-internals.png)

## The Docker Engine

![](/archictecture_and_theory/img/architecture-docker-engine.png)

## Windows Containers

![](/archictecture_and_theory/img/architecture--containers-windows.png)
![](/archictecture_and_theory/img/architecture--containers-windows-1.png)



