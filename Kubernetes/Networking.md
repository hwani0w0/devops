## 1. Namespaces
```
ip link/route/arp
ip netns exec {namespace} ip link
ip -n {namespace} link
```
   
## 2. Docker
### 2.1 none
- 
### 2.2 host
```
docker run --network host nginx
```

### 2.3 bridge
```bash 
docker network ls
ip link
```


## 3. Pod




















