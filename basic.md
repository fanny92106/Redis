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
        
        
        Redis使用场景:
            - 配合关系型数据库做告诉缓存
                * 高频词, 热门访问的数据, 降低数据库IO
                * 分布式架构, 做session共享
    
    
    
