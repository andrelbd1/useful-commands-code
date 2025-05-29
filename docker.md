### [Docker](https://docs.docker.com/) commands

#### General
- Run docker daemon.
````bash
    systemctl start docker
````
- Download image from docker hub
````bash
    docker pull <NAME:TAG>
    docker pull httpd:latest
````
- Build a Dockerfile
````bash
    docker build -t <TAG> <DOCKERFILE PATH>
    docker build -t meu-app .
````

#### Allowing access to docker without use sudo
- Creating a docker group and adding user. It is required to do logoff and login.
````bash
    sudo groupadd docker
    sudo usermod -aG docker $USER
````

#### Images
- List all images
````bash
    docker image ls -a
    docker images -a
````
- Remove an image
````bash
    docker image rm <IMAGE IDs>
    docker rmi <IMAGE IDs>
````
- Exports a Docker image, including layers, history, and metadata.
````bash
    docker save <IMAGE ID> -o <PATH FILE>.tar
````
- Load an image
````bash
    docker load -i <PATH FILE>.tar
````

#### Containers
- Create a container assigning name (--name) and port (-p), running in background (-d) and enabling interactive mode (-it)
````bash
    docker run -d --name <CONTAINER-NAME> -it -p <PORT>:<PORT> <IMAGE:TAG or IMAGE ID>
    docker run -d --name isi-httpd -it -p 8083:80 httpd:latest
````
- Create a container assigning name, port and env var file (--env-file)
````bash
    docker run --env-file <PATH FILE> -d --name <CONTAINER-NAME> -it -p <PORT>:<PORT> <IMAGE:TAG or IMAGE ID>
    docker run --env-file .env -d --name isi-httpd -it -p 8083:80 httpd:latest
````
- Create a container assigning name, port and removing container after stopping (--rm)
````bash
    docker run -d --name <CONTAINER-NAME> -it -p <PORT>:<PORT> --rm <IMAGE:TAG or IMAGE ID>
    docker run -d --name isi-httpd -it -p 8083:80 --rm httpd:latest
````
- Create a container limiting to 512MB of memory (-m)
````bash
    docker run -d --name <CONTAINER-NAME> -it -m <MEMORY> -p <PORT>:<PORT> --rm <IMAGE:TAG or IMAGE ID>
    docker run -d --name isi-httpd -it -m 512M -p 8083:80 --rm httpd:latest
````
- Create a container limiting to 0.5 of cpu (--cpus)
````bash
    docker run -d --name <CONTAINER-NAME> -it --cpus=<CPU> -p <PORT>:<PORT> --rm <IMAGE:TAG or IMAGE ID>
    docker run -d --name isi-httpd -it --cpus=0.5 -p 8083:80 --rm httpd:latest
````
- List all containers
````bash
    docker ps -a
    docker container ls -a
````
- List running containers
````bash
    docker ps
````
````bash
    docker stats
````
- Start containers
````bash
    docker container start <CONTAINER IDs or NAME>
````
- Stop containers
````bash
    docker container stop <CONTAINER IDs or NAME>
````
- Kill containers
````bash
    docker container kill <CONTAINER IDs>
````
- Restart containers
````bash
    docker restart <CONTAINER IDs>
````
- Remove containers
````bash
    docker rm <CONTAINER IDs>
````
- Update container's cpu (--cpu) and memory (-m)
````bash
    docker container update -m <MEMORY> --cpus=<CPU> <CONTAINER IDs or NAME>
    docker container update -m 256m --cpus=1 test1
````
- Copying file to the container
````bash
    docker cp foo.txt <CONTAINER ID>:/foo.txt
````
- Copying file from the container
````bash
    docker cp <CONTAINER ID>:/foo.txt foo.txt
````
- Access a container by bash
````bash
    docker exec -it <CONTAINER ID or NAME> bash
````
- See process in execution in the container
````bash
    docker container top <CONTAINER ID or NAME>
````
- See logs in execution in the container
````bash
    docker container logs <CONTAINER ID or NAME>
````
- Export a container's filesystem, excluding image history
````bash
    docker export <CONTAINER ID or NAME> -o <PATH FILE>.tar
````
- Import a container's filesystem, excluding image history
````bash
    docker import <CONTAINER ID or NAME> -o <PATH FILE>.tar
````
- See container settings
````bash
    docker container inspect  <CONTAINER ID or NAME>
````
- See memory allocated to a container
````bash
    docker container inspect  <CONTAINER ID or NAME> | grep -i mem
````
- List all containers using an image
````bash
    docker container ls --all --filter=ancestor=<IMAGE ID> --format "{{.ID}}"
````

#### Volume
- List volume
````bash
    docker volume ls
````

- Remove unused volumes
````bash
    docker volume prune
````

#### Compose
- Build, (re)creates, starts, and attaches a container from a docker-compose.yaml
````bash
    docker compose up
    docker compose --env-file .env up
````
- Show logs from a service
````bash
    docker compose logs -f -t <service>
    docker compose logs -f -t -worker
````
- Scale a service
````bash
    docker compose scale <service>=<number>
    docker compose scale worker=3
````
