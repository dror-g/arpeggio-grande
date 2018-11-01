FROM golang

WORKDIR /go/src/app
COPY . .

RUN apt-get update && apt-get install -y liblmdb-dev

RUN go get -d -v ./...
RUN go install -v ./...

CMD ["go", "run", "backend.go"]
