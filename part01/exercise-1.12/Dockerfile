FROM ubuntu:18.04

WORKDIR /usr/app/src

EXPOSE 5000

RUN apt-get update && apt-get install -y curl

RUN curl -sL https://deb.nodesource.com/setup_16.x | bash
RUN apt install -y nodejs

COPY . .

RUN npm install

RUN npm run build
RUN npm install -g serve

CMD ["serve","-s","-l","5000","build"]