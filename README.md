# tani-cloud(自宅鯖)

- 本来は色々載せるつもり
- 今はKubernetesメイン

## 現状

- NextCloudを動かそうとしてる
- うごかん

```
tani@k8s-master:~/k8s$ tree
.
├── ens18.md
├── ingress
│   └── ingress.yaml
├── install.md
├── kube-flannel.yml
├── metallb
│   ├── install.md
│   ├── metallb-config.yaml
│   ├── metallb.yaml
│   └── namespace.yaml
├── nextcloud
│   ├── nextcloud.yaml
│   ├── pv.yaml
│   └── service.yaml
└── README.md

3 directories, 12 files
tani@k8s-master:~/k8s$ k apply -f nextcloud/pv.yaml -f nextcloud/nextcloud.yaml -f nextcloud/service.yaml
persistentvolume/nextcloud created
statefulset.apps/nextcloud created
service/nextcloud created
tani@k8s-master:~/k8s$
```