ip link/route/arp
ip netns exec {namespace} ip link
ip -n {namespace} link

## docker network 
### none
- 
### host
```
docker run --network host nginx
```
### bridege
```bash 
docker network ls
ip link
```

