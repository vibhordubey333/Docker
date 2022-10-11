### Dockerize Go Application
1. Docker file
```
# Build Stage
# First pull Golang image
FROM golang:1.17-alpine as build-env
 
# Set environment variable
ENV APP_NAME 1.Containerise_Go 
ENV CMD_PATH main.go
 
# Copy application data into image
COPY . $GOPATH/src/$APP_NAME
WORKDIR $GOPATH/src/$APP_NAME
 
# Build application
RUN CGO_ENABLED=0 go build -v -o /$APP_NAME $GOPATH/src/$APP_NAME/$CMD_PATH
 
# Run Stage
FROM alpine:3.14
 
# Set environment variable
ENV APP_NAME 1.Containerise_Go
 
# Copy only required data into this image
COPY --from=build-env /$APP_NAME .
 
# Expose application port
EXPOSE 8081
 # Start app
CMD ./$APP_NAME
```
2. Now, update dependencies `go mod tidy`
3. Build docker image `docker build --rm -t 1.containerize_go .`
   `--rm` flag it used to remove any running existing container. Like below
   `-t` flag is for tagging with our custom name
   `.` implies Dockerfile exist in current dir. Otherwise we would've to use `-f` with dir path.

```
osboxes@osboxes:~$ sudo docker container ls
[sudo] password for osboxes:
CONTAINER ID   IMAGE               COMMAND                  CREATED              STATUS              PORTS                                       NAMES
9f45ac3c187f   1.containerise_go   "/bin/sh -c ./$APP_N…"   About a minute ago   Up About a minute   0.0.0.0:8081->8081/tcp, :::8081->8081/tcp   thirsty_lamport
```

4. To run `docker run -p 8081:8081 1.containerize_go`
   `-p` flag is for publishing port. In other words we're mapping our container port
    to the external port so we can access the container.
