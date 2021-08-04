# dummy - image, container, pod, deployment, service

## dummy container image features

- created from Ubuntu with familiar tools for simple debugging tasks, for example ping, tcpdump
- some packages are just for convenience, for instance I prefer `ifconfig` to `ip a`
- it runs a very simple and light web server on port 80
- the webserver has support for cgi and you can access some URLs like http://<pod IP>/cgi-bin/status

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

