## Docker Learning

#### Create Image from docker file and run

Package the spring boot application into jar file (or any other deployment package file) and add the docker file then go to the root of the folder. 

```bash
docker build -t 'image-name'
```

Verify if docker image has been created : 

```shell
docker image ls
```

Run the container :

```shell
docker run -rm -p 5000:8080 'image-name'
```

To run the container with name : 

```shell
docker run -d -rm -p 5000:8080 'image-name' 'user-name'/'image-name':'tag'
```

To stop the container : 

```shell
docker stop 'container-id'
```





















