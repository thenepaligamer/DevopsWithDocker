```
❯ docker build -t backend .
Sending build context to Docker daemon   42.5kB
Step 1/7 : FROM golang:1.16
 ---> 972d8c0bc0fc
Step 2/7 : WORKDIR /usr/src/app
 ---> Using cache
 ---> bffe5a6b6fc0
Step 3/7 : EXPOSE 8080
 ---> Using cache
 ---> 460eab03c927
Step 4/7 : ENV REQUEST_ORIGIN=http://localhost:5000
 ---> Using cache
 ---> 2a49823134c4
Step 5/7 : COPY . .
 ---> Using cache
 ---> 68ee6c6f4ae2
Step 6/7 : RUN go build
 ---> Using cache
 ---> 67f314def763
Step 7/7 : CMD ./server
 ---> Using cache
 ---> 9a749aae6b84
Successfully built 9a749aae6b84
Successfully tagged backend:latest

❯ docker run -p 8080:8080 backend
[Ex 2.4+] REDIS_HOST env was not passed so redis connection is not initialized
[Ex 2.6+] POSTGRES_HOST env was not passed so postgres connection is not initialized
[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:   export GIN_MODE=release
 - using code:  gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /ping                     --> server/router.pingpong (4 handlers)
[GIN-debug] GET    /messages                 --> server/controller.GetMessages (4 handlers)
[GIN-debug] POST   /messages                 --> server/controller.CreateMessage (4 handlers)
[GIN-debug] Listening and serving HTTP on :8080
[GIN] 2023/05/06 - 06:37:43 | 200 |      82.367µs |      172.17.0.1 | GET      "/ping"
```