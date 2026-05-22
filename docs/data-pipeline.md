# AI数据管线

## 数据准备流程
1. 数据采集(API/爬虫/上传)
2. 清洗去重(格式/语言/质量)
3. 分块切分(语义/固定/递归)
4. 嵌入向量化(Embedding模型)
5. 索引存储(向量数据库)
6. 检索重排(相似度/MMR)

## 分块策略
| 策略 | 优点 | 缺点 |
|------|------|------|
| 固定长度 | 简单 | 可能截断语义 |
| 递归字符 | 灵活 | 需调参 |
| 语义分块 | 语义完整 | 计算量大 |
| 句子窗口 | 上下文丰富 | 存储翻倍 |

## 常用工具
- Unstructured: 文档解析
- LangChain TextSplitters
- LlamaIndex NodeParsers
- ChunkingbySentenceTransformers
