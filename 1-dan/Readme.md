# Cheat sheet

#### Kako prodibiti kubernetes objekte
```bash
kubectl get <resource> -n <namespace>
```

#### Kako dodati nov kubernetes objekt, ki je shranjen v datoteki?
```bash
kubectl create -f <00-pod.yaml> -n <namespace>
```
#### Kako posodobiti kubernetes objekt, ki je shranjen v datoteki?
```bash
kubectl applay -f <00-pod.yaml> -n <namespace>
```
#### Kako odstraniti kubernetes objekt, ki je shranjen v datoteki?
```bash
kubectl applay -f <00-pod.yaml> -n <namespace>
```
#### Kako vrniti deployment na stanje pred dodanimi spremembami?
Za večnjo pregldnost lahko dodamo annotation, ki doda opis nadgradnje `kubernetes.io/change-cause: <opis>`

#### Zlistamo vse zadnje deployane verzije

```bash
kubectl rollout history deployment/<ime_deploymenta> -n <namespace> 
```
#### Vrnjemo na točno določeno verzijo
```bash
kubectl rollout undo  deployment/<ime_deploymenta> -n <namespace>  --to-revision=<revision>
```

#### Helm rolleback
```bash
helm history <RELEASE>
helm rollback <RELEASE> [REVISION]
```