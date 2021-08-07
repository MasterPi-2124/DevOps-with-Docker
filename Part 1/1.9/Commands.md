```
$ touch text.log
```
```
$ docker run -dv "$(pwd)/text.log:/usr/src/app/text.log" devopsdockeruh/simple-web-service

3efe585f347d9e1bdf678b3c0bebd53edb8bd659873983e4b1499392cef0cbfa
```

## Issue
I want to bind `/usr/src/app` within the directory, but it doesn't work and I don't know why:

```
$ docker run -dv "$(pwd):/usr/src/app" devopsdockeruh/simple-web-service

79ba73cc4f4ab437e44ae46cfe732d802275a06bcc3da1a82e6314590972c1bf
docker: Error response from daemon: OCI runtime create failed: container_linux.go:380: starting container process caused: exec: "/usr/src/app/server": stat /usr/src/app/server: no such file or directory: unknown.
```

So the only way I can do is binding a file instead, as in the solution. If you see this message, please let me know via email, or [create](https://github.com/MasterPi-2124/DevOps-with-Docker/issues/new) an issue on GitHub. Thank you!

My email: minh.vln140501@gmail.com