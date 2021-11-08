FROM golang:alpine AS builder

WORKDIR $GOPATH/src/mypackage/app

COPY . .

ENV REDIS_HOST=rediscontainer

ENV REQUEST_ORIGIN=http://localhost:5000/

RUN apk update && apk add --no-cache git && \
go get -d -v && \
go build -o /go/bin/server

FROM alpine

COPY --from=builder /go/bin/server /go/bin/server

CMD ["/go/bin/server"]
