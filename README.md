# docker-postgres
Example stack.yml for postgres

How to use this image
start a postgres instance

$ docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres

The default postgres user and database are created in the entrypoint with initdb.

    The postgres database is a default database meant for use by users, utilities and third party applications.

    postgresql.org/docs

... or via psql

$ docker run -it --rm --network some-network postgres psql -h some-postgres -U postgres
psql (9.5.0)
Type "help" for help.

postgres=# SELECT 1;
 ?column? 
----------
        1
(1 row)

... via docker stack deploy or docker-compose

Example stack.yml for postgres:

# Use postgres/example user/password credentials
version: '3.1'

services:

  db:
    image: postgres
    restart: always
    environment:
      POSTGRES_PASSWORD: example

  adminer:
    image: adminer
    restart: always
    ports:
      - 8080:8080
