# Codemy redis

[![Docker Repository on Quay](https://quay.io/repository/codemy/redis/status "Docker Repository on Quay")](https://quay.io/repository/codemy/redis)

This redis instance is configured to use 500mb of ram with 200 connections.

# Usage

```
docker run --name <app or env name>-redis -d -p 7000:6379 \
           -v /your/host/volume/path:/data codemy/redis:latest
```