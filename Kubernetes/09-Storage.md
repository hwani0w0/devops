```yaml
apiVersion: v1
kind: Pod
metadata:
name: random-number-generator
spec:
containers:
- image: alpine
name: alpine
command: ["/bin/sh","-c"]
args: ["shuf -i 0-100 -n 1 >> /opt/number.out;"]
56
volumes:
- name: data-volume
/data
volumeMounts:
- mountPath: /opt
name: data-volume
56
56
hostPath:
path: /data
type: Directory
```

## Persistent Volume
- accessModes: `ReadOnlyMany` / `ReadWirteOnce` / `ReadWriteMany`

## Persistent Volume Claim
