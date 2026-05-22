# RAG检索增强生成

## 什么是RAG
RAG结合检索与生成，让LLM利用外部知识。

## 核心流程
1. 文档加载与分块
2. 向量嵌入与索引
3. 相似度检索
4. 上下文注入生成

## 框架对比
| 框架 | 特点 |
|------|------|
| LangChain | 生态丰富，链式调用 |
| LlamaIndex | 数据索引专精 |
| Haystack | 生产级管道 |
| RAGFlow | 开源，文档解析强 |

## 向量数据库
- Chroma: 轻量级本地
- FAISS: Meta开源高性能
- Milvus: 分布式云原生
- Qdrant: Rust高性能
