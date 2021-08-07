```
$ docker build . -t ubuntu:curler

Sending build context to Docker daemon   5.12kB
Step 1/6 : FROM ubuntu:18.04
 ---> 39a8cfeef173
Step 2/6 : WORKDIR /usr/src/app
 ---> Running in 830bc01a35e2
Removing intermediate container 830bc01a35e2
 ---> 35dd71b367b2
Step 3/6 : COPY script.sh .
 ---> c4102dbefc9d
Step 4/6 : RUN chmod +x script.sh
 ---> Running in 3153054dbbdb
Removing intermediate container 3153054dbbdb
 ---> f20bb870fd6c
Step 5/6 : RUN apt update; apt install curl -y
 ---> Running in 764a205e48df
...
Removing intermediate container 764a205e48df
 ---> cb57f50ee52c
Step 6/6 : CMD ./script.sh
 ---> Running in 4325b0c09727
Removing intermediate container 4325b0c09727
 ---> 3a6d41a471c0
Successfully built 3a6d41a471c0
Successfully tagged ubuntu:curler
```
```
$ docker run -it ubuntu:curler

Input website:
helsinki.fi
Searching..
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="https://www.helsinki.fi/">here</a>.</p>
</body></html>

```