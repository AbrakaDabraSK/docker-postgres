# Docker postgresql server with pgadmin4
Example for postgresql server via docker on ubuntu server.

## Make .env file

```shell
cp .env.example .env
```


## Edit .env file (vim, nano.. your favorite choice)

Open enviroment file

```shell
vim .env
```

Edit default enviroment file if u need

```shell
POSTGRES_USER=root
POSTGRES_PASSWORD=12345
POSTGRES_DB=root

PGADMIN_DEFAULT_EMAIL=root@localhost
PGADMIN_DEFAULT_PASSWORD=12345
PGADMIN_LISTEN_PORT=80
```

Quit and save + ENTER

```shell
wq!
```

## Run

```shell
docker-compose up -d
```

## Down

```shell
docker-compose down
```

## Check

```shell
docker-compose ps
```

## Visit 

```shell
http://host-ip:8080
```
