# kubectl

## 命令行构造
 kubectl [Command] [Type] [Name] [Flag]

 command: delete, get, describe, apply...
 type: 资源对象的类型，严格区分大小写；单数和复数都可以。比如node,pod...
 name: 资源对象的名称，严格区分大小写；
 flag: 可选参数； 如：-n指定namespace；

## 资源对象类型
 daemonsets -> ds
 deployments
 events -> ev
 endpoints -> ep
 horizonalpodautoscalers -> hpa
 ingresses -> ing
 jobs
 nodes -> no
 pods -> po
 namespace -> ns
 persistentvolumes -> pv
 persistentvolumesclaims -> pvc
 resourcequotas -> quota
 replicationcontrollers -> rc
secrets
service -> svc
serviceaccount -> sa

## 练习
同时查看多个资源对象类型
```
kubectl get pod/[pod name] svc/[service name] -n kube-system
```
## 常用command
1. annotate 添加或更新资源对象信息，少用；
2. apply： kubectl apply -f [filename] #从配置文件更新资源对象；
3. attach: kubectl attach pod -c container #连接一个正在运行的pod上；
4. cluster-info: kubectl cluster-info #显示集群信息；
5. completion: 输入shell命令的返回码；
6. config: 修改配置文件;
7. create: kubectl create -f [filename.yml] #从配置文件新增资源对象
8. delete: kubectl delete -f [filename.yml] #从配置文件删除资源对象
9. describe： kubectl describe [资源对象名称] #查看资源对象的描述信息
10. edit: kubectl edit [资源对象名称] #编辑资源对象的属性
11. exec:     #执行容器中的命令
12. label: kubectl label $资源类型 $资源名称 key=value  #打标签，为了资源对象创建标记
