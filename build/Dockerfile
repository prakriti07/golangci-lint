FROM golang:1.14

# don't place it into $GOPATH/bin because Drone mounts $GOPATH as volume
RUN ./cmd/golangci-lint/main.go
COPY golangci-lint /usr/bin/
#RUN wget -O- -nv https://raw.githubusercontent.com/golangci/golangci-lint/master/install.sh |sh -s -- -b /usr/bin
CMD ["golangci-lint"]
