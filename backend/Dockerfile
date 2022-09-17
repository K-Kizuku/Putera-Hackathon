
#FROM arm64v8/golang:1.19.1-alpine3.16
FROM golang:1.19.1-alpine3.16

RUN mkdir -p /go/src/PuteraAPI/
COPY . /go/src/PuteraAPI/
WORKDIR /go/src/PuteraAPI/

RUN go install

RUN go get -u github.com/cosmtrek/air && \
    go build -o /go/bin/air github.com/cosmtrek/air

CMD ["air"]