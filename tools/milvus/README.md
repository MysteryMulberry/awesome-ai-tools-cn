# Milvus

云原生向量数据库。

## 特性
- 十亿级向量检索
- 多种索引类型
- 水平扩展
- 混合检索

## 快速开始
```bash
docker run -d --name milvus milvusdb/milvus:latest
```

## Python SDK
```python
from pymilvus import Collection
collection = Collection('my_collection')
results = collection.search(query_vector, 'embedding', param={'metric_type': 'COSINE'}, limit=10)
```
