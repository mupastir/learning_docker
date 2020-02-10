# Docker install
___

## Docker install for Windows

**Pre-reqs**:

- Windows 10
- 64-bit
- Clean (ish) install


**Use cases**:

- Test
- Dev
- ~~Production~~

1. `Turn on features on or off:`
	- Turn on Hyper-V
	- Turn in BIOS `Intel VT/VT-x` or `AMD-V`
1. Download Docker for Windows
1. Install Docker
1. Go to `cmd`:
	- Check docker version (`docker version`)
	- Check docker info (`docker info`)

## Docker install for Mac

**Pre-reqs**

- Mac hardware from 2010 or newer
- OS X 10.10.3 or newer

1. Download Docker for Mac
1. Open Docker.dmg and follow instructions
1. Check installed app:
	- Open terminal and check `docker version`

## Docker install on Windows Server 2016

1. Run PowerShell as Adminitrator
1. `Install-WindowsFeature containers`
1. `Restart-Computer`
1. Create dir in `Program Files` `docker`
1. Download from [https://aka.ms/tp5/b/dockerd](https://aka.ms/tp5/b/dockerd) and [https://aka.ms/tp5/b/docker](https://aka.ms/tp5/b/docker)
1. Copy downloaded files to created folder
1. Add path of Docker
1. Open PowerShell:
	- `dockerd --register-service`
	- `Start-Service docker`
	- Check instakked docker (`Get-Service docker`)
	- `docker version`
	- `docker info`
	- Install-PackageProvider ContainerImage -Force
	- Find-ContainerImage
	- Install-ContainerImage WindowaServerCore
	- Restart-Service docker
	- docker images
	- docker tag <image ID> <name>:latest
	- hostname (for example we will get `docker-win`)
	- docker run -it windowsservercore cmd
	- check hostname (its differ from previous cause we are inside docker container)
	- docker ps

## Install Docker in Linux (Ubuntu)

**Check docs**

1. Download script `wget -qO- [https://get.docker.com/](https://get.docker.com/) | sh`
1. run `sudo usermod -aG docker <your-user>

___

**Not all Dockers are equal!!!**
