# Answers

## 4.6 

[Docker repo](https://hub.docker.com/repository/docker/mrstaf/hello-world-docker-mrstaf)

## 5.4
```zsh
sudo docker volume create db_data
```

```zsh
docker service create -d \
  --name devtest-service \
  --mount source=db_data,target=/data \
  nginx:latest
```

## 5.9

All the data disappears because when we remove the docker, we are deleting the virtual storage. We need to store the data into a volume on our computer to ensure we are saving data.