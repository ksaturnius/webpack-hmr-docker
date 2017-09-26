# How to start
### Clone repository
```bash
git clone git@github.com:szujak/webpack-hmr-docker.git
```
### Go to the folder
```bash
cd webpack-hmr-docker
```
### Run docker
```bash
docker-compose up
docker-compose up --build # if you want to rebuild image from tools/docker/Dockerfile
```
### Shoutdown
```bash
docker-compose down -v
```

# Modyfications
### Changing PORT
```yml
# docker-compose.yml
services:
    app:
        ports:
            - 4444:4444
```
```bash
# tools/docker/Dockerfile
ENV PORT=4444
```

### Changing destination folder in docker
```yml
# docker-compose.yml
services:
    app:
        volumes:
            - .:/my/own/path
```
```bash
# tools/docker/Dockerfile
ENV APP_PATH=/my/own/path
```

### Changing container name
```yml
# docker-compose.yml
services:
    app:
        container_name: my_awesome_name
```
