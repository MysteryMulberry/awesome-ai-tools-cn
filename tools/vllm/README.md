# vLLM

高性能LLM推理和服务引擎。

## 特性
- PagedAttention技术
- 连续批处理
- 张量并行支持
- OpenAI兼容API

## 快速启动
```bash
python -m vllm.entrypoints.openai.api_server --model meta-llama/Llama-3-8B
```

## 性能
- 比HuggingFace快24x
- 支持A100/H100 GPU
