Metallb repo: https://metallb.github.io/metallb

Najprej popravimo datoteko `ipAddressPool.yaml`, da ustrezno določimo IP pool. Nato dodamo IpaddressPool:
```
kubectl create -f  ipAddressPool.yaml
```

V primeru, da smo v prejšnji datoteki popravili ime resourvo moramo ustrezno prilagoditi podatke v datoteki 
`ipPoolAdvertisment.yaml`. Nato datoteko dodamo z ukazom:
```
kubectl create -f ipPoolAdvertisment.yaml
```


