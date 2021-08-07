```
$ docker run -dit --rm devopsdockeruh/simple-web-service:ubuntu

586c84d3dccadfb85bdc459627babecc40d6bb1439274b967f9d89b3804eb96a
```
```
$ docker ps -a

CONTAINER ID   IMAGE                                      COMMAND                 CREATED          STATUS         PORTS     NAMES
586c84d3dcca   devopsdockeruh/simple-web-service:ubuntu   "/usr/src/app/server"   11 seconds ago   Up 9 seconds             youthful_maxwell
```
```
$ docker exec -it youthful_maxwell tail -f ./text.log

2021-08-05 16:35:57 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
...
```

