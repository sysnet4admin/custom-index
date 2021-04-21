# Custom kubernetes plugin 

## How to install 

### Add custome-index
```sh
[root@m-k8s]# kubectl krew index add cst https://github.com/sysnet4admin/custom-index.git
kubectl krew index add cst https://github.com/sysnet4admin/custom-index.git
WARNING: You have added a new index from "https://github.com/sysnet4admin/custom-index.git"
The plugins in this index are not audited for security by the Krew maintainers.
Install them at your own risk.
```

### Check indexes list 
```sh
[root@m-k8s]# kubectl krew index list 
INDEX    URL
cst      https://github.com/sysnet4admin/custom-index.git
default  https://github.com/kubernetes-sigs/krew-index.git
```

### Plugin install
```sh
[root@m-k8s]# kubectl krew install cst/conn
Updated the local copy of plugin index "cst".
Updated the local copy of plugin index.
  New plugins available:
    * cst/conn
Installing plugin: conn
Installed plugin: conn
\
 | Use this plugin:
 |      kubectl conn
 | Documentation:
 |      https://github.com/sysnet4admin/k8s-plugins
/
```

### need permission

```sh  
[root@m-k8s ~]# chmod +x .krew/store/conn/v0.0.1/conn.sh
```


