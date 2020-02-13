# Containerizing an App

`docker image build`

**Flow**
 
![](/containerizing_an_app/img/containerizing-flow.png)

**Dockergile notes:**

- Instructions for building images
- CAPITALIZE instructions
- <INSTRUCTION> <value>
- FROM always first instruction
- FROM = base image
- Good practice to list maintainer (`LABEL maintainer="mupastir@gmil.com"`)
- Run = execute command and create layer
- COPY = copy code into image as new layer
- Some instructions add metadata instead of layers
- ENTRYPOINT = default app for image/container


`docker build -t <name> <git-repo>`

When the URL parameter points to the location of a Git repository, the repository acts as the build context. The system recursively fetches the repository and its submodules. The commit history is not preserved. A repository is first pulled into a temporary directory on your local host. After that succeeds, the directory is sent to the Docker daemon as the context. Local copy gives you the ability to access private repositories using local user credentials, VPN’s, and so forth.

## Multi-stage Builds

Small = Better
**Unikernels**

Have several `FROM` instructions 

![](/containerizing_an_app/img/containerizing-build-multi-stage.png)

