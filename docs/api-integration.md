# API集成指南

## OpenAI兼容API
大多数工具支持OpenAI格式调用：

```python
from openai import OpenAI
client = OpenAI(base_url='http://localhost:8000/v1', api_key='empty')
response = client.chat.completions.create(
    model='model-name',
    messages=[{'role':'user','content':'Hello'}]
)
```

## LangChain集成
```python
from langchain_openai import ChatOpenAI
llm = ChatOpenAI(base_url='http://localhost:8000/v1')
```

## 常见端口
- Ollama: 11434
- vLLM: 8000
- Open WebUI: 3000
- Dify: 80
