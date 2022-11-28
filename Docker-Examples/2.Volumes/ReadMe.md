### Docker-Volume [Writing Data To File]
---
> Dockerfile
```
FROM ubuntu:latest
RUN mkdir /data
WORKDIR /data
RUN echo "Hello from Volume" > test
VOLUME /data
```

#### Execute following steps.

1. `docker build -t volume-example:latest .`
2. `docker run volume-example-1:latest`
3. `docker volume ls `
4. Go to location `cd /var/lib/docker/volumes`
5. `ls -lrt`
6. `cd ./<FOLDER_NAME_WITH_RANDOM_NUMBERS_&_CHARACTERS>`
7. `cd ./_data`
8. `cat test`
https://docs.docker.com/storage/#:~:text=Volumes%20are%20the%20preferred%20way,is%20mounted%20into%20a%20container.


<details>
<summary>References</summary>
1. Docker-Volumes https://earthly.dev/blog/docker-volumes/ <br>
</details>
