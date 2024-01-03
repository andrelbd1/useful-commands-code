### [Docker](https://docs.docker.com/) commands

#### Connecting Docker daemon
- Executar docker daemon.
````bash
systemctl start docker
````

#### Allowing access to docker without use sudo
- Creating a docker group and adding user. It is required to do logoff and login.
````bash
sudo groupadd docker
sudo usermod -aG docker $USER
````

#### General
- List all containers
````bash
docker container ls -a
````
- List running containers
````bash
docker stats
````
- Start containers
````bash
docker container start [CONTAINER IDs]
````
- Stop containers
````bash
docker container stop [CONTAINER IDs]
````
- Kill containers
````bash
docker container kill [CONTAINER IDs]
````
- Restart containers
````bash
docker restart [CONTAINER IDs]
````
- Remove containers
````bash
docker rm [CONTAINER IDs]
````

- Copying file to the container
````bash
docker cp foo.txt container_id:/foo.txt
````

- Copying file from the container
````bash
docker cp container_id:/foo.txt foo.txt
````

#### Handle container
- Access a container by bash
````bash
docker exec -it [CONTAINER ID] bash
````
- Build, (re)creates, starts, and attaches a container
````bash
docker-compose up
````
