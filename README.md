# ElasticSearch入门教程By Gary

## ES CURL常用命令：
> 1. 检查ES集群健康状态：curl 'localhost:9200/_cat/health?v&pretty'
> 2. 查看ES集群所有节点信息：curl 'localhost:9200/_cat/nodes?v&pretty'
> 3. 查找别名为Alias_name的Index：curl 'localhost:9200/_alias/Alias_name?pretty'
> 4. 查询Index下的所有数据（默认返回10条结果）：curl 'localhost:9200/Index/_search?q=*&pretty'
> 5. 设置查询返回结果的数量（设置返回1000000条结果）：curl -XPUT 'localhost:9200/Index/_settings' -d '{"index":{"max_result_window":1000000}}'
> 6. 根据Id查询单条数据：curl 'localhost:9200/Index/Type/Id?pretty'
> 7. 删除Index：curl -XDELETE 'localhost:9200/Index?pretty'
> 8. 新建Index：curl -XPUT 'localhost:9200/Index?pretty'
> 9. 插入单条数据：curl -XPUT 'localhost:9200/Index/Type/Id?pretty' -d '{"name":"gary"}'
> 10. 删除单条数据：curl -XDELETE 'localhost:9200/Index/Type/Id?pretty'
> 11. 查看ES集群所有Index：curl 'localhost:9200/_cat/indices?v&pretty'
