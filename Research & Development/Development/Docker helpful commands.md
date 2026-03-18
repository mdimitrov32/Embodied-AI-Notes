
List all locally available images:
```
docker image ls
```

List all containers
```
docker ps -a
```

Remove image:
```
docker image rm [ID]
```

Remove container:
```
docker container rm [ID]
```

Set docker start on startup: 
```
sudo systemctl enable docker.service
sudo systemctl enable containerd.service
```

Stop docker start on startup:
```
sudo systemctl disable docker.service
sudo systemctl disable containerd.service
```
