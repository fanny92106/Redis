# Redis - 为性能而生


0. NoSQL (Not Only SQL)

        - key-value模式进行存储, 大大增加了数据库的扩展能力
        - 不遵循SQL标准
        - 不支持事务ACID
        - 性能远超SQL (内存 vs 磁盘)
        
        NoSQL应用场景: 
            - 数据高并发读写
            - 海量数据读写
            - 数据高可扩展性
        
        NoSQL不适用场景:
            - 需要事务支持
            - 基于sql的结构化查询存储, 处理复杂的关系 (关联), 或条件查询
       
       
1. Redis

        - key-value存储系统, 数据缓存在内存中
        - 支持多种数据类型: string, list, set, zset, hash
        - 支持多种排序, push/pop, add/remove, 以及交集并集差集等丰富的操作
        - 周期性地将数据写入磁盘或把修改操作写入追加的记录文件
        - 可实现master-slave主从同步
        - 默认有16个数据库
        
        
        Redis使用场景:
            - 配合关系型数据库做告诉缓存
                * 高频词, 热门访问的数据, 降低数据库IO
                * 分布式架构, 做session共享
    
    
2. Linux 编译&安装 Redis
        
        - 解压缩文件
        - make (编译)
        - make install (安装)
        
        默认安装目录: /usr/local/bin
        Redis目录:
            - redis-benchmark: 性能测试工具, 在服务启动后执行可以查看运行主机的性能
            - redis-check-aof: 修复有问题的AOF文件
            - redis-check-dump: 修复有问题的dump.rdb文件
            - redis-sentinel: Redis集群使用
            - redis-server: Redis服务器启动命令
            - redis-cli: 客户端, 操作入口


3. 启动Redis服务器和Redis客户端

        - copy一份redis.conf到另一个目录
        - 修改redis.conf中的daemonize no为yes, 使Redis可以在后台运行, 而不占用操作界面
        - 启动redis-server /dir/redis.conf
        - 启动redis-cli
        - 测试: ping ---> PONG (Redis默认端口号为6379)



