FROM golang:1.16

WORKDIR /usr/src/app

COPY . .

ENV REDIS_HOST=rediscontainer

ENV REQUEST_ORIGIN=http://localhost:5000

RUN go build

RUN useradd -m backenduser

USER backenduser

CMD ./server

