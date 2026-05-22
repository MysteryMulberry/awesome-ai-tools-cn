# LLM模型部署指南

## 部署方案对比

| 方案 | 适用场景 | GPU需求 | 延迟 |
|------|---------|---------|------|
| vLLM | 高吞吐推理 | A100/H100 | 低 |
| TGI | HuggingFace生态 | A100 | 低 |
| Ollama | 本地开发 | 消费级GPU | 中 |
| llama.cpp | CPU推理 | 可选GPU | 中 |
| TensorRT-LLM | NVIDIA优化 | A100/H100 | 极低 |

## vLLM部署示例
```bash
pip install vllm
python -m vllm.entrypoints.openai.api_server \
  --model meta-llama/Llama-3-8B \
  --tensor-parallel-size 1 \
  --max-model-len 4096
```

## Ollama部署示例
```bash
ollama pull llama3
ollama run llama3
curl http://localhost:11434/api/generate -d '{
  "model": "llama3",
  "prompt": "Hello world"
}'
```

---
*更新时间: {DATETIME_STR}*
