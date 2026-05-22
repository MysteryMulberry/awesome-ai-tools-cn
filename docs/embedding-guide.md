# 向量嵌入(Embedding)指南

## 什么是Embedding
将文本映射为高维向量，语义相似的文本向量距离近。

## 模型选择
| 模型 | 维度 | 最大输入 | 性能 |
|------|------|---------|------|
| text-embedding-3-large | 3072 | 8191 | 最优 |
| text-embedding-3-small | 1536 | 8191 | 均衡 |
| bge-large-zh-v1.5 | 1024 | 512 | 中文优 |
| bge-m3 | 1024 | 8192 | 多语言 |

## 使用示例
```python
response = client.embeddings.create(
    model='text-embedding-3-small',
    input='你好世界'
)
embedding = response.data[0].embedding  # 1536维向量
```

## 相似度计算
- 余弦相似度: 最常用
- 欧氏距离: 考虑向量大小
- 点积: 简单高效
