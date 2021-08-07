Add all commands into one
```
$ docker run -it --rm ubuntu sh -c 'apt update; apt install curl; echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website'
```
