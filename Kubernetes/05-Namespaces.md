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
