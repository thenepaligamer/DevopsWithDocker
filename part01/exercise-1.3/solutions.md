```
❯ docker run -d --name exercise1.3 devopsdockeruh/simple-web-service:ubuntu
Unable to find image 'devopsdockeruh/simple-web-service:ubuntu' locally
ubuntu: Pulling from devopsdockeruh/simple-web-service
5d3b2c2d21bb: Pull complete 
3fc2062ea667: Pull complete 
75adf526d75b: Pull complete 
965d4bbb586a: Pull complete 
4f4fb700ef54: Pull complete 
Digest: sha256:d44e1dce398732e18c7c2bad9416a072f719af33498302b02929d4c112e88d2a
Status: Downloaded newer image for devopsdockeruh/simple-web-service:ubuntu
486d040b28511da52e40303a55605c55c5264abee724a2b337d31378b323ff9b
❯ docker ps
CONTAINER ID   IMAGE                                      COMMAND                  CREATED          STATUS         PORTS                                               NAMES
486d040b2851   devopsdockeruh/simple-web-service:ubuntu   "/usr/src/app/server"    11 seconds ago   Up 6 seconds                                                       exercise1.3
3995b3b2a2e3   app                                        "/docker-entrypoint.…"   4 weeks ago      Up 8 hours     80/tcp, 0.0.0.0:8088->8088/tcp, :::8088->8088/tcp   app
❯ docker exec -it exercise1.3 bash
root@486d040b2851:/usr/src/app# tail -f ./text.log
2023-03-24 18:48:57 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2023-03-24 18:48:59 +0000 UTC
2023-03-24 18:49:01 +0000 UTC
2023-03-24 18:49:03 +0000 UTC
2023-03-24 18:49:05 +0000 UTC
2023-03-24 18:49:07 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2023-03-24 18:49:09 +0000 UTC
2023-03-24 18:49:11 +0000 UTC
```