# AI成本优化

## API调用优化
- 缓存重复请求
- 合理设置max_tokens
- 使用流式输出减少超时
- 选择适合任务的模型

## 模型选择策略
| 任务 | 推荐模型 | 原因 |
|------|---------|------|
| 简单分类 | GPT-3.5 | 成本低 |
| 复杂推理 | GPT-4 | 能力强 |
| 代码 | DeepSeek-Coder | 性价比高 |
| 中文 | Qwen | 中文优化 |

## 本地替代
- 对话: Ollama + Qwen2
- 代码: Ollama + DeepSeek-Coder
- 嵌入: 本地Sentence-Transformers
