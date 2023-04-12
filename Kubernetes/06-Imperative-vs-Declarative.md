## Imperative
+ **명령적**
+ step by step
+ 단계별 지침서
+ Create Objects : create 
+ Update Objects

## Declarative
+ **선언적**
+ 요구사항 선언
+ ex) Ansible, Puppet, Chef, Terraform
+ Create Objects : apply
+ Update Objects


## Tips!
### 1. POD
Create an NGINX Pod
```bash
kubectl run nginx --image=nginx
```
Generate POD Manifest YAML file (-o yaml). Don't create it(--dry-run)
```bash
kubectl run nginx --image=nginx --dry-run=client -o yaml
```


### 2. Deployment
Create a deployment
```bash
kubectl create deployment --image=nginx nginx
```
Generate Deployment YAML file (-o yaml). Don't create it(--dry-run)
```bash
kubectl create deployment --image=nginx nginx --dry-run=client -o yaml
```
Generate Deployment with 4 Replicas
```bash
kubectl create deployment nginx --image=nginx --replicas=4

```
You can also scale a deployment using the kubectl scale command.
```bash
kubectl scale deployment nginx --replicas=4
```
Another way to do this is to save the YAML definition to a file and modify
```bash
kubectl create deployment nginx --image=nginx --dry-run=client -o yaml > nginx-deployment.yaml
```


### 3. Service
Create a Service named redis-service of type ClusterIP to expose pod redis on port 6379
```bash
kubectl expose pod redis --port=6379 --name redis-service --dry-run=client -o yaml
```
Or
```bash
kubectl create service clusterip redis --tcp=6379:6379 --dry-run=client -o yaml (This will not use the pods labels as selectors, instead it will assume selectors as app=redis. You cannot pass in selectors as an option. So it does not work very well if your pod has a different label set. So generate the file and modify the selectors before creating the service)
```
Create a Service named nginx of type NodePort to expose pod nginx's port 80 on port 30080 on the nodes:
```bash
kubectl expose pod nginx --type=NodePort --port=80 --name=nginx-service --dry-run=client -o yaml
```