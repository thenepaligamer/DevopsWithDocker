```
❯ docker pull devopsdockeruh/simple-web-service:alpine
alpine: Pulling from devopsdockeruh/simple-web-service
ba3557a56b15: Pull complete 
1dace236434b: Pull complete 
4f4fb700ef54: Pull complete 
Digest: sha256:dd4d367476f86b7d7579d3379fe446ae5dfce25480903fb0966fc2e5257e0543
Status: Downloaded newer image for devopsdockeruh/simple-web-service:alpine
docker.io/devopsdockeruh/simple-web-service:alpine

❯ docker images
REPOSITORY                          TAG             IMAGE ID       CREATED         SIZE
devopsdockeruh/simple-web-service   ubuntu          4e3362e907d5   2 years ago     83MB
devopsdockeruh/simple-web-service   alpine          fd312adc88e0   2 years ago     15.7MB

❯ docker run -d --name alpine devopsdockeruh/simple-web-service:alpine
5ad384db885a2408826bf888c556bdeefec611bc75bcd69373459b51cc21de2a

❯ docker ps
CONTAINER ID   IMAGE                                      COMMAND                  CREATED         STATUS          PORTS                                               NAMES
5ad384db885a   devopsdockeruh/simple-web-service:alpine   "/usr/src/app/server"    2 minutes ago   Up 2 minutes                                                        alpine
3995b3b2a2e3   app                                        "/docker-entrypoint.…"   8 weeks ago     Up 50 minutes   80/tcp, 0.0.0.0:8088->8088/tcp, :::8088->8088/tcp   app
❯ docker exec -it alpine sh

/usr/src/app # ls
server    text.log
/usr/src/app # tail -f ./text.log
2023-04-22 11:42:05 +0000 UTC
2023-04-22 11:42:07 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2023-04-22 11:42:09 +0000 UTC
2023-04-22 11:42:11 +0000 UTC
2023-04-22 11:42:13 +0000 UTC
2023-04-22 11:42:15 +0000 UTC
2023-04-22 11:42:17 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2023-04-22 11:42:19 +0000 UTC
2023-04-22 11:42:21 +0000 UTC
2023-04-22 11:42:23 +0000 UTC
2023-04-22 11:42:25 +0000 UTC
^C
/usr/src/app # ^C
```