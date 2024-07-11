# ByteTalk
基于Mprpc的分布式集群聊天系统  
技术架构：C++,vscode远程Ubuntu开发，cmake构建集成编译环境，linux shell输出项目编译脚本，MySQL数据库，Protobuf，ZooKeeper，Muduo网络库,Nginx  
项目描述：   
● 使用基于Reactor模型的muduo网络库作为项目的网络核心模块，提供高并发网络IO服务，解耦网络和业务模块代码。  
● 实现基于Protobuf和zookeeper的RPC框架，提高聊天服务器的并发性与可扩展性。  
● 使用Protobuf序列化和反序列化消息作为私有通信协议，使用zookeeper 作为配置注册中心。  
● 配置nginx基于权重的tcp负载均衡，实现聊天服务器的集群功能，提高后端服务的并发能力。   
● 基于发布-订阅(观察者模式)的服务器中间件消息队列redis解决集群环境中跨服务器聊天通信。   
● 使用mysql关系型数据库作为项目数据的落地存储，并引入数据库连接池提高数据库的数据存取性能。  
