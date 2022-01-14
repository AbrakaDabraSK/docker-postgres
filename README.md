# docker-postgres
Example for postgresql server via docker

## Make .env file

```shell
cp .env.example .env
```


## Edit .env file

```shell
POSTGRES_USER=username
POSTGRES_PASSWORD=password
POSTGRES_DB=default_database
```

## Run

```shell
docker-compose --env-file ./.env up -d
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
