### Build Docker image
Usage:

**docker build [options] [context]**

Example:
```
docker build -f my-dockerfile --build-arg API_URL=http://localhost:3333 --tag=myapp .
```
-f : Dockerfile to build

--build-arg : Arguments to pass as environment variables during the build process. Must be defined inside Dockerfile using the ARG directive.

--tag : Tag (name) of Docker image to build

[context] (dot) : build context to use for building Docker image (i.e. folder which contains assets to be copied).

### Run Docker image
Usage:

**docker run [options] [image] [command] [arg...]**

Example:
```
docker run --rm -d -p 8085:8080 -e HOST=0.0.0.0 -v my-volume:/slek-server/build/db.sqlite3 --name=myapp myapp:latest
```
--rm : Delete container upon container exit / Daemon termination.

-d : Detached mode (container runs in the background)

-p : Port range mapping. <HOST_PORTS>:<CONTAINER_PORTS>

-e : Enviornment variable to inject. <KEY_>:<VALUE_>

-v : Mount docker volume / bind-mount path on local filesystem. <HOST_PATH>:<CONTAINER_PATH>

--name : Name of the newly created container.

[image]:latest : image to be run at revision (latest)

### Execute into Docker image
Usage:

**docker exec [options] [container] [command] [arg...]**

Example:
```
docker exec -it myapp /bin/bash
```
-it : Interactive mode (useful for opening interactive command prompt with shell, e.g. bash)

[command] : command to run inside the container. In this case, we open interactive bash command prompt.

### Alter Docker container's state
Usage:

**docker restart / start / stop / pause [options] [container]**

Example:
```
docker restart myapp
```
stop : Stop container using SIGKILL signal.

pause : Stop container using SIGSTOP signal.

### Clean-up Docker
Usage:

**docker system / container / image / volume prune [options]**

Example:
```
docker system prune
```
system : Delete all stopped containers, dangling / unreferenced images, unused networks, optionally unmounted volumes (--volumes argument).

volune : Delete all volumes not attached to a container.

image : Delete all dangling and unreferenced images.

### Docker-compose
Usage:

**docker-compose [options] [command] [arg...]**

Example:
```
docker-compose -f my-app-compose.yml up / down
```
-f : Docker Compose YAML file to use (default: docker-compose.yml).