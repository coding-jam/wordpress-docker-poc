# wordpress-docker-poc

Sample project for testing **Docker Compose** and **Docker Swarm** capabilities

## Run with Compose

Run 

```sh
docker-compose up -d
```

to build and run containers.

To stop and remove containers

```sh
docker-compose down -v
```

## Run with Swarm

Once built with Compose, enter Swarm mode if not enabled

```sh
docker swarm init
```

then

```sh
docker stack deploy -c docker-compose.yml wp
```

To remove deployed services

```sh
docker stack rm wp
```

To exit Swarm mode

```sh
docker swarm leave --force
```
