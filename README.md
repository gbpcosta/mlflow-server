# MLFlow Dockerised Server using NGINX basic auth

Based on: https://github.com/ymym3412/mlflow-docker-compose

## Add user/password

```
echo "{USER_NAME}:$(openssl passwd -apr1 {PASSWORD})" >> ${HOST}
```

## Build

```
docker-compose build
```

## Run

```
docker-compose up -d
```

## Stop

```
docker-compose down
```
