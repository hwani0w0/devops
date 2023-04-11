## Namespaces
`dev`환경과 `prod`환경을 구별할 수 있음
```bash
kubectl get pods --namespace=dev
kubectl create pod-definition.yml --namespace=dev  # 혹은 yaml파일에 추가
```

```bash
kubectl create namespace dev

kubectl config set-context $(kubectl config current-context) --namespcae=dev  # default 네임스페이스 변경
kubectl get pods

kubectl get pods --all-namepasces
```
## Resource Quota
Namepace 리소스 제한
리소스에 용량 할당
```bash
kubectl create -f compute-quota.yaml
```
```yaml
apiVersion: v1
kind: ResourceQuota
meatadata:
  name: compute-quota
  namespace: dev
spec:
  hard:
    pods: "10"
    requests.cpu: "4"
    requests.memory: 5Gi
    limits.cpu: "10"
    limits.memory: 10Gi
```
