# 向量嵌入模型

## 模型选择

| 模型 | 维度 | 性能 | 适用场景 |
|------|------|------|---------|
| text-embedding-3-large | 3072 | 优秀 | 高精度检索 |
| bge-large-zh | 1024 | 优秀 | 中文检索 |
| mxbai-embed-large | 1024 | 优秀 | 英文通用 |
| all-MiniLM-L6-v2 | 384 | 良好 | 快速检索 |

## 使用示例
```python
from sentence_transformers import SentenceTransformer

model = SentenceTransformer('BAAI/bge-large-zh-v1.5')
embeddings = model.encode(["你好世界", "Python编程"])
```

## 相似度计算
```python
from sklearn.metrics.pairwise import cosine_similarity

sim = cosine_similarity([emb1], [emb2])[0][0]
```

## 优化技巧
- 批量编码提升吞吐
- 量化压缩减少存储
- HNSW索引加速检索

---
*更新时间: {DATETIME_STR}*
