# AI工具部署指南

## 云服务部署
### OpenAI API
```python
import openai
client = openai.OpenAI(api_key='sk-xxx')
```

### 阿里云百炼
适合Qwen系列模型部署

## 本地部署
### Ollama
```bash
ollama run llama3
ollama run qwen2
```

### vLLM
适合高吞吐量生产环境

### Docker
大部分工具提供Docker镜像

## 硬件需求
| 模型规格 | 最低GPU | 推荐GPU |
|---------|---------|--------|
| 7B | RTX 3060 12GB | RTX 4070 |
| 13B | RTX 3090 24GB | RTX 4090 |
| 70B | 2×A100 80GB | 4×A100 |
