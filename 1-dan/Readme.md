<h1>Cheat sheet</h1>

<h4>Kako prodibiti kubernetes objekte</h4>
```
kubectl get <resource> -n <namespace>
```

<h4>Kako dodati nov kubernetes objekt, ki je shranjen v datoteki?</h4>
```
kubectl create -f <00-pod.yaml> -n <namespace>
```
<h4>Kako posodobiti kubernetes objekt, ki je shranjen v datoteki?</h4>
```
kubectl applay -f <00-pod.yaml> -n <namespace>
```
<h4>Kako odstraniti kubernetes objekt, ki je shranjen v datoteki?</h4>
```
kubectl applay -f <00-pod.yaml> -n <namespace>
```
<h4>Kako vrniti deployment na stanje pred dodanimi spremembami?</h4>
Za večnjo pregldnost lahko dodamo annotation, ki doda opis nadgradnje `kubernetes.io/change-cause: <opis>`
```
#Zlistamo vse zadnje deployane verzije

```
kubectl rollout history deployment/<ime_deploymenta> -n <namespace> 
```
#Vrnjemo na točno določeno verzijo
```
kubectl rollout undo  deployment/<ime_deploymenta> -n <namespace>  --to-revision=<revision>
```

Helm rolleback
```
helm history <RELEASE>
helm rollback <RELEASE> [REVISION]