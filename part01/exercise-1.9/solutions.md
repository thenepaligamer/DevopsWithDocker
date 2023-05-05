```
❯ touch text.log

❯ ls
solutions.md  text.log

❯ docker run -d -v "$(pwd)/text.log://usr/src/app/text.log" devopsdockeruh/simple-web-service:alpine
46ef3e119ebea1e6a6518130317e665bd584424bf8185cb239638b7976bd5178

❯ tail -f ./text.log
2023-05-05 14:50:19 +0000 UTC
2023-05-05 14:50:21 +0000 UTC
2023-05-05 14:50:23 +0000 UTC
2023-05-05 14:50:25 +0000 UTC
2023-05-05 14:50:27 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2023-05-05 14:50:29 +0000 UTC
2023-05-05 14:50:31 +0000 UTC
2023-05-05 14:50:33 +0000 UTC
^C

❯ docker ps
CONTAINER ID   IMAGE                                      COMMAND                  CREATED          STATUS          PORTS                                               NAMES
46ef3e119ebe   devopsdockeruh/simple-web-service:alpine   "/usr/src/app/server"    23 seconds ago   Up 20 seconds                                                       thirsty_lamarr
3995b3b2a2e3   app                                        "/docker-entrypoint.…"   2 months ago     Up 14 minutes   80/tcp, 0.0.0.0:8088->8088/tcp, :::8088->8088/tcp   app
```