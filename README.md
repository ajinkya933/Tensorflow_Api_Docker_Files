# Tensorflow-Object-Detection-Api Docker Files

![](https://github.com/ajinkya933/Tensorflow_Api_Docker_Files/blob/master/imgs/puddle_jumper_octodex.jpg) 


With Github and Docker's help, I solve a really frustating problem, my problem was each time I make some changes to a library or tensorflow version the tensorflow object detection API didnt produce any output. There were n number of errors and it wasted alot of my time to fix them each time. Finally I made a Docker container whos instructions are given in nice details below, and now whenever I have a trained model from object detection API. I just build docker image and test it and it tests models with good consistency. . Note I use ```object_detection2.ipynb``` from research/object-detection directory (which is inside the docker container) to test my retrained models.


#### To build the docker file navigate to tensorflow1.14_cpu_p36 folder and type:

```
docker build -t tensorflow .
```
#### After building start: (without assigning IP):
```
docker run <container name>
```

#### After building start: (with assinment of IP):
```
docker run --name tensorflow -p 8888:8888 -d tensorflow
```
And open http://localhost:8888
Password: root

#### To ssh into a docker container 
```
docker exec -it <container name> /bin/bash
```
another way to login

```
sudo docker run -i -t <container id> /bin/bash
```


#### To stop the docker container:

```
docker container stop <container name>
```


#### To remove the docker container:

```
docker container rm <container name>
```


#### To copy files from localhost to docker 
```
docker cp <local_folder> <docker_container_name>:<full_path of folder inside docker>
```

note <docker_container_name>: can be got by command : ```docker ps -a```

#### To copy files from docker to localhost 
```
docker cp <docker_container_name>:<full_path of folder inside docker> <local_folder>
```
