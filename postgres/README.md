# Postgres

[![Docker Repository on Quay](https://quay.io/repository/codemy/postgres/status "Docker Repository on Quay")](https://quay.io/repository/codemy/postgres)

This is Codemy's Postgres with PgTune configs

see the config files for different settings used

## Usage

By default it will use the 1gb-ram.conf file

```shell
docker run --name <name>-postgres \
           --volume /host/data/path:/var/lib/postgresql/data \
           --publish 5432:5432 \
           --detach \
           codemy/postgres:latest \
           postgres -c config_file=/configs/1gb-ram.conf
```


