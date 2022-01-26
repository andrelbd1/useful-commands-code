### [Docker](https://docs.docker.com/) commands

#### Conectar Docker daemon
- Executar docker daemon.
````bash
systemctl start docker
````

#### Permitir acesso ao docker sem usar sudo
- Criar o docker group e add usuário. É necessário fazer logoff e login.
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

#### Handle container
- Access a container by bash
````bash
docker exec -it [CONTAINER ID] bash
````
- Build, (re)creates, starts, and attaches a container
````bash
docker-compose up
````
