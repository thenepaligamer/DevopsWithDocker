```
❯ docker build -t frontend .
Sending build context to Docker daemon  729.1kB
Step 1/12 : FROM ubuntu:18.04
 ---> 3941d3b032a8
Step 2/12 : WORKDIR /usr/src/app
 ---> Using cache
 ---> 0ad73de93ae8
Step 3/12 : EXPOSE 5000
 ---> Using cache
 ---> 341176665ed7
Step 4/12 : ENV REACT_APP_BACKEND_URL=http://localhost:8080
 ---> Using cache
 ---> 7fd884515b70
Step 5/12 : RUN apt-get update && apt-get install -y curl
 ---> Using cache
 ---> 8f0d7ff71b09
Step 6/12 : RUN curl -sL https://deb.nodesource.com/setup_16.x | bash
 ---> Using cache
 ---> 135135026e9c
Step 7/12 : RUN apt install -y nodejs
 ---> Using cache
 ---> f1270f1d9442
Step 8/12 : COPY . .
 ---> Using cache
 ---> 2f2f68c88cd4
Step 9/12 : RUN npm install
 ---> Using cache
 ---> 31e2efbcf218
Step 10/12 : RUN npm run build
 ---> Using cache
 ---> 4f345d7903d9
Step 11/12 : RUN npm install -g serve
 ---> Using cache
 ---> 4eb46b631996
Step 12/12 : CMD [ "serve", "-s", "-l", "5000", "build" ]
 ---> Using cache
 ---> ede2a6279ac2
Successfully built ede2a6279ac2
Successfully tagged frontend:latest

❯ docker run -p 5000:5000 frontend
 INFO  Accepting connections at http://localhost:5000
 HTTP  5/6/2023 6:37:31 AM 172.17.0.1 GET /
 HTTP  5/6/2023 6:37:31 AM 172.17.0.1 Returned 200 in 34 ms
 HTTP  5/6/2023 6:37:31 AM 172.17.0.1 GET /static/css/main.eaa5d75e.chunk.css
 HTTP  5/6/2023 6:37:31 AM 172.17.0.1 GET /static/js/2.43ca3586.chunk.js
 HTTP  5/6/2023 6:37:31 AM 172.17.0.1 GET /static/js/main.667b6e84.chunk.js
 HTTP  5/6/2023 6:37:31 AM 172.17.0.1 Returned 200 in 10 ms
 HTTP  5/6/2023 6:37:31 AM 172.17.0.1 Returned 200 in 9 ms
 HTTP  5/6/2023 6:37:31 AM 172.17.0.1 Returned 200 in 15 ms
 HTTP  5/6/2023 6:37:31 AM 172.17.0.1 GET /static/media/toskalogo.c0f35cf0.svg
 HTTP  5/6/2023 6:37:31 AM 172.17.0.1 Returned 200 in 4 ms
 HTTP  5/6/2023 6:37:31 AM 172.17.0.1 GET /favicon.ico
 HTTP  5/6/2023 6:37:31 AM 172.17.0.1 Returned 200 in 2 ms
```