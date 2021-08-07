```
$ docker run -it ubuntu

root@248e4bbb52cf:/# apt update
root@248e4bbb52cf:/# apt install curl
root@248e4bbb52cf:/# sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'
```