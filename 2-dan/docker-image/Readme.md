1. Kreiramo Dockerfile
2. Zbuildamo sliko z komando:
```
docker build -t <registry>/<image_name>:<tag> <pot>/<do>/<dockerfila/.
```
3. Se prijavimo v registry
```
docker login <registry>
```
4. Dodamo sliko v repozitorij
```
docker push <registry>/<image_name>:<tag>
```

Primer:
```
docker build -t harbor.src.si/hit-izobrazevanje/nginx:1.0 2-dan/docker-image/.  
docker login harbor.src.si
docker push  harbor.src.si/hit-izobrazevanje/nginx:1.0 
```