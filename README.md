# MLFlow Dockerised Server

MLFlow Server dockerised setup using NGINX as basic authentication and PostgreSQL for entity storage (artifacts are stored locally)

Based on: https://github.com/ymym3412/mlflow-docker-compose

## Add user/password

```
echo "{USER_NAME}:$(openssl passwd -apr1 {PASSWORD})" >> ${HOST}
```

`${HOST}` as defined in your `.env` file

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

## TODOs

- Include DVC for data versioning
- Include Kubeflow for 
- Improve artifact storage
- Make ports more flexible (currently fixed due to `acme-companion`, including `MLFLOW_PORT` in env)
- Add GoogleCloud and AWS setups
