FROM golang:1.14
#ARG TARGETPLATFORM
# don't place it into $GOPATH/bin because Drone mounts $GOPATH as volume
#COPY /home/runner/work/golangci-lint/golangci-lint/dist/golangci-lint_linux_arm64/golangci-lint /usr/bin
RUN go build
#RUN go build ./cmd/golangci-lint/main.go
COPY golangci-lint /usr/bin/
#COPY /usr/bin tar xf /build/dist/golangci-lint_*_$(echo ${TARGETPLATFORM} | tr '/' '_' | sed -e 's/arm_/arm/').tar.gz
#RUN --mount=target=/usr/bin tar xf /build/dist/golangci-lint_*_$(echo ${TARGETPLATFORM} | tr '/' '_' | sed -e 's/arm_/arm/').tar.gz
#RUN ./cmd/golangci-lint/main.go
#COPY golangci-lint /usr/bin/
#RUN wget -O- -nv https://raw.githubusercontent.com/golangci/golangci-lint/master/install.sh |sh -s -- -b /usr/bin
CMD ["golangci-lint"]
