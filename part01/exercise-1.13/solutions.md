```
❯ docker build -t backend .
Sending build context to Docker daemon   42.5kB
Step 1/6 : FROM golang:1.16
1.16: Pulling from library/golang
e4d61adff207: Pull complete 
4ff1945c672b: Pull complete 
ff5b10aec998: Pull complete 
12de8c754e45: Pull complete 
8c86ff77a317: Pull complete 
0395a1c478ba: Pull complete 
245345d44ed8: Pull complete 
Digest: sha256:5f6a4662de3efc6d6bb812d02e9de3d8698eea16b8eb7281f03e6f3e8383018e
Status: Downloaded newer image for golang:1.16
 ---> 972d8c0bc0fc
Step 2/6 : WORKDIR /usr/src/app
 ---> Running in f78afbe1f3b5
Removing intermediate container f78afbe1f3b5
 ---> bffe5a6b6fc0
Step 3/6 : EXPOSE 8080
 ---> Running in 5277939e61d6
Removing intermediate container 5277939e61d6
 ---> 460eab03c927
Step 4/6 : COPY . .
 ---> ee64338a1b08
Step 5/6 : RUN go build
 ---> Running in a3f9839a9159
go: downloading github.com/gin-contrib/cors v1.3.1
go: downloading github.com/gin-gonic/gin v1.6.3
go: downloading github.com/go-redis/redis/v8 v8.4.2
go: downloading github.com/go-pg/pg/v10 v10.7.3
go: downloading github.com/gin-contrib/sse v0.1.0
go: downloading github.com/mattn/go-isatty v0.0.12
go: downloading github.com/go-playground/validator/v10 v10.2.0
go: downloading github.com/golang/protobuf v1.4.3
go: downloading github.com/ugorji/go v1.1.7
go: downloading gopkg.in/yaml.v2 v2.3.0
go: downloading github.com/cespare/xxhash/v2 v2.1.1
go: downloading github.com/ugorji/go/codec v1.1.7
go: downloading github.com/dgryski/go-rendezvous v0.0.0-20200823014737-9f7001d12a5f
go: downloading go.opentelemetry.io/otel v0.14.0
go: downloading mellium.im/sasl v0.2.1
go: downloading github.com/go-pg/zerochecker v0.2.0
go: downloading github.com/jinzhu/inflection v1.0.0
go: downloading github.com/vmihailenco/msgpack/v5 v5.0.0
go: downloading github.com/vmihailenco/tagparser v0.1.2
go: downloading golang.org/x/sys v0.0.0-20201119102817-f84b799fce68
go: downloading github.com/go-playground/universal-translator v0.17.0
go: downloading github.com/leodido/go-urn v1.2.0
go: downloading google.golang.org/protobuf v1.25.0
go: downloading github.com/tmthrgd/go-hex v0.0.0-20190904060850-447a3041c3bc
go: downloading github.com/vmihailenco/bufpool v0.1.11
go: downloading golang.org/x/crypto v0.0.0-20201117144127-c1f2f97bffc9
go: downloading github.com/go-playground/locales v0.13.0
Removing intermediate container a3f9839a9159
 ---> 365e71bd270d
Step 6/6 : CMD ./server
 ---> Running in bf9f565f3d69
Removing intermediate container bf9f565f3d69
 ---> c9170f39df62
Successfully built c9170f39df62
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
[GIN] 2023/05/06 - 06:13:16 | 200 |      69.192µs |      172.17.0.1 | GET      "/ping"
[GIN] 2023/05/06 - 06:13:16 | 404 |      22.907µs |      172.17.0.1 | GET      "/favicon.ico"
```