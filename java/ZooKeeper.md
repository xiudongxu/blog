# Zookeeper

### 简介

ZooKeeper是一种为分布式应用所设计的高可用、高性能且一致的开源协调服务，是Google的Chubby一个开源的实现，它是集群的管理者，监视着集群中各个节点的状态根据节点提交的反馈进行下一步合理操作。最终，将简单易用的接口和性能高效、功能稳定的系统提供给用户

### 应用业务

1.命名服务   
2.配置管理   
3.集群管理   
4.分布式锁  
5.队列管理

### 节点类型

1、PERSISTENT-持久化目录节点 

客户端与zookeeper断开连接后，该节点依旧存在 

2、PERSISTENT_SEQUENTIAL-持久化顺序编号目录节点 

客户端与zookeeper断开连接后，该节点依旧存在，只是Zookeeper给该节点名称进行顺序编号 

3、EPHEMERAL-临时目录节点 

客户端与zookeeper断开连接后，该节点被删除 

4、EPHEMERAL_SEQUENTIAL-临时顺序编号目录节点

客户端与zookeeper断开连接后，该节点被删除，只是Zookeeper给该节点名称进行顺序编号 



### zkCli.sh

1.连接  zkCli.sh -server 192.168.255.133:2181

2.查看节点 ls /

3.查看节点内容 get /zookeeper/quota

4.创建节点 create /zookeeper/test1 1111

5.更新数据 set /zk/test1 222

6.删除节点 delete /zk

7.退出程序 quit



### java api

