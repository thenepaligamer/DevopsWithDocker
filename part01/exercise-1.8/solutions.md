```
❯ docker run devopsdockeruh/simple-web-service:alpine hello


                The application accepts 1 argument "server". Use the argument server to run the server

                If no arguments are supplied the application will output log strings to a file.


Arguments given: hello

❯ docker build . -t web-server
Sending build context to Docker daemon   2.56kB
Step 1/2 : FROM devopsdockeruh/simple-web-service:alpine
 ---> fd312adc88e0
Step 2/2 : CMD server
 ---> Running in 5d4e17299104
Removing intermediate container 5d4e17299104
 ---> a5e1a53045c4
Successfully built a5e1a53045c4
Successfully tagged web-server:latest

❯ docker images
REPOSITORY                          TAG             IMAGE ID       CREATED         SIZE
web-server                          latest          a5e1a53045c4   9 seconds ago   15.7MB
hello-world                         latest          feb5d9fea6a5   19 months ago   13.3kB
devopsdockeruh/simple-web-service   ubuntu          4e3362e907d5   2 years ago     83MB
devopsdockeruh/simple-web-service   alpine          fd312adc88e0   2 years ago     15.7MB
nginx                               1.16.0-alpine   ef04b00b089d   3 years ago     20.4MB
devopsdockeruh/pull_exercise        latest          d9854bc0e13a   4 years ago     75.3MB

❯ docker run web-server
[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:   export GIN_MODE=release
 - using code:  gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /*path                    --> server.Start.func1 (3 handlers)
[GIN-debug] Listening and serving HTTP on :8080
```