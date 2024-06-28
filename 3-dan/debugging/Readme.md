Komanda, ki pridobi loge:
```
kubectl logs <obstojec_pod> -n <namespace> 
```
KOmanda, ki vrne določeno polje iz Yamla:
```
kubectl get deployments.apps httpd-deployment -n user1 -o jsonpath={".spec.replicas"} 
```

Komanda, ki vrne poglobljene podatke:
```
kubectl describe pod <ime_poda> -n <namespace>
```

Komanda, ki doda nov kontejner k obstoječemu z potrebnimi orodji:
```
kubectl debug <obstojec_pod> -it --image=<image> -n <namespace> 
```