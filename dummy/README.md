# dummy - image, container, pod, deployment, service

## dummy container image features

- created from Ubuntu with familiar tools for simple debugging tasks, for example ping, netcat
- some client tools like mysql (client only) and redis-cli
- some packages are just for my convenience, for instance I prefer `ifconfig` to `ip a` and `netstat` to `ss`
- it runs a very simple and light web server on port 80
- the webserver has support for cgi and you can access some URLs like http://<pod IP>/cgi-bin/status 
(look into cgi-bin directory here for more)

## build and use

To build the image: 
```
docker build -t dummy-pod .
```

To use it in Docker: 
```
docker run -d  -p 6789:80 --name dummy dummy-pod
```


## Kubernetes

To use it in Kubernetes, see the pod or deployment YAMLs

TBD: note about /mnt

