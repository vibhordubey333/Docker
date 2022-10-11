clean:
	go mod tidy
build:
	sudo docker build --rm -t 1.containerise_go .
run:
	docker run -p 8081:8081 1.containerise_go
all: 
	go mod tidy
	sudo docker build --rm -t 1.containerise_go .
	sudo docker run -p 8081:8081 1.containerise_go

