# krew custom plugins

## Installation procedure 

### Add custom-index
```sh
[root@m-k8s]# kubectl krew index add cix https://github.com/sysnet4admin/custom-index.git
kubectl krew index add cix https://github.com/sysnet4admin/custom-index.git
WARNING: You have added a new index from "https://github.com/sysnet4admin/custom-index.git"
The plugins in this index are not audited for security by the Krew maintainers.
Install them at your own risk.
```

### Check indexes list 
```sh
[root@m-k8s]# kubectl krew index list 
INDEX    URL
cix      https://github.com/sysnet4admin/custom-index.git
default  https://github.com/kubernetes-sigs/krew-index.git
```

### Plugin install thru adding index 
```sh
[root@m-k8s ~]# kubectl krew install cix/ctxon
Updated the local copy of plugin index "cix".
Updated the local copy of plugin index.
Installing plugin: ctxon
Installed plugin: ctxon
\
 | Use this plugin:
 |      kubectl ctxon
 | Documentation:
 |      https://github.com/sysnet4admin/kubectxon
/
```

