# docker实战

## docker使用etcd

```
docker search etcd
```

docker hub上搜索镜像，选择一个star最高的

```
docker pull bitnai/etcd
```

拉取镜像

```
docker run -d --name rpc_etcd   -p 2379:2379 -p 2380:2380   -e ALLOW_NONE_AUTHENTICATION=yes   bitnami/etcd
```

创建容器

简单复习一下这些命令  -d是指后台挂载，--name是命名 -p是设置端口 -e是设置参数，这里是不启动密码验证，最后是容器名

容器（containers），镜像（images）和卷（Volumes）：

总结来说，镜像是容器的模板，容器是镜像的运行实例，而卷是用于数据持久化和共享的存储机制。



同理安装etcdkeeper

```
docker run -d --name rpc_etcdkeeper   -p 8081:8081   -e PORT=8081 evildecay/etcdkeeper
```

为什么这里要设置一样的port呢？-p是指的将容器的某端口映射到主机，后面e中的PORT是服务运行的端口。类似redis，mysql等等，虽然有运行的端口，但是都是可以随意访问的（命令行直接mysql就能访问到），但是这个不行，得挂载到某个端口，所以这个端口必须是和主机映射的端口



无法通信，创建一个网络，将两者放入同一网络下

```
docker network create rpc-net
docker run -d --name rpc_etcd   -p 2379:2379 -p 2380:2380   --network rpc-net -e ALLOW_NONE_AUTHENTICATION=yes   bitnami/etcd
docker run -d --name rpc_etcdkeeper   -p 8081:8081   --network rpc-net -e PORT=8081 evildecay/etcdkeeper
```

还是有问题，但是是可以ping通的

docker exec  rpc_etcdkeeper ping  rpc_etcd

服了，本机使用rpc_etcdkeeper随便用，可能是rpc_etcdkeeper本身的docker版本有问题，不去纠结了