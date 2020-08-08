FROM golang:1.14
#ARG TARGETPLATFORM
# don't place it into $GOPATH/bin because Drone mounts $GOPATH as volume
RUN git clone https://github.com/golangci/golangci-lint
WORKDIR golangci-lint
RUN go build -o /usr/bin/golangci-lint ./cmd/golangci-lint/main.go
CMD ["golangci-lint"]
