## kubectl 명령어

pod 생성 `create`  `apply` 둘다 가능
```
kubectl apply -f pod.yaml
```

pod 목록 호출
```
kubectl get pods
```

pod 정보
```
kubectl describe pod myapp-pod
```

pod 생성 후 yaml 파일 저장
```
kubectl run redis --image-redis --dry-run -o yaml
kubectl run test --image=redis --dry-run=client -o yaml
kubectl run test --image=redis --dry-run=client -o yaml > test.yaml
```

pod yaml 파일 예시
```yaml
apiVersion : v1
kind : Pod
metatdata :
  name : nginx
  labels :
    app : nginx
    tier : frontend
spec :
  containers :
  - name : nginx
    image : nginx
  - name : busybox
    image : busybox
```
