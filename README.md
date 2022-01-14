# docker-postgres
Example for postgresql server via docker.

## Make .env file

```shell
cp .env.example .env
```


## Edit .env file (vim, nano.. your favorite choice)

Open enviroment file

```shell
vim .env
```

Edit variables

```shell
POSTGRES_USER=username
POSTGRES_PASSWORD=password
POSTGRES_DB=default_database
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
