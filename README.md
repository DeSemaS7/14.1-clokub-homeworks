# Задача 1: Работа с секретами через утилиту kubectl в установленном minikube

Повторил описанные команды, было весело.
<br>

вот список:
```shell
NAME                                            TYPE                                  DATA   AGE
default-token-mnhwx                             kubernetes.io/service-account-token   3      43d
domain-cert                                     kubernetes.io/tls                     2      25h
domain-cert-mod                                 kubernetes.io/tls                     2      25h
nfs-server-nfs-server-provisioner-token-8txnf   kubernetes.io/service-account-token   3      30d
sh.helm.release.v1.nfs-server.v1                helm.sh/release.v1                    1      30d
```
На выходе заимел yaml для деплоя tls серта:

```
apiVersion: v1
data:
  tls.crt: LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUZiVENDQTFXZ0F3SUJBZ0lVU1ZXbWFUbWFKQUNuRnluaWZBWXlrUERoRmRvd0RRWUpLb1pJaHZjTkFRRUwKQlFBd1Jq>  
  tls.key: LS0tLS1CRUdJTiBSU0EgUFJJVkFURSBLRVktLS0tLQpNSUlKSndJQkFBS0NBZ0VBM3FleGp4cTM1c09xMFcySDJMVEhKdXFDV0dLcEd3K3I4KzJiM09LejVjMG04RldOCmJJ>kind: Secret
metadata:
  creationTimestamp: "2021-11-29T10:10:12Z"
  name: domain-cert-mod
  namespace: default
  resourceVersion: "164713"
  uid: bc19a82f-f7cc-42fd-8c01-7f716549a4b2
type: kubernetes.io/tls


