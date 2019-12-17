# Tensorflow_Api_Docker_Files

To build the docker file navigate to each folder and type:

```
docker build -t tensorflow .
```

After building start:
```
docker run --name tensorflow -p 8888:8888 -d tensorflow
And open http://localhost:8888
```

To stop the docker file type:

```
docker rm -f tensorflow
```

To copy files from localhost to docker 
```
docker cp <local_folder> <docker_container_name>:<full_path of folder inside docker>
```

note <docker_container_name>: can be got by command : ```docker ps -a```

To copy files from docker to localhost 
```
docker cp <docker_container_name>:<full_path of folder inside docker> <local_folder>
```
