# Ollama

本地LLM运行框架，一键拉取运行模型。

## 常用命令
```bash
ollama run llama3
ollama run qwen2:7b
ollama run deepseek-coder
ollama list
ollama pull mistral
```

## 特性
- 一键模型管理
- OpenAI兼容API
- 多模态支持
- GPU/CPU自动检测

## Modelfile自定义
```dockerfile
FROM llama3
SYSTEM 你是一个专业的中文助手
PARAMETER temperature 0.7
```
