# 结构化输出

## 为什么需要结构化输出
LLM原生输出为自由文本，实际应用需要JSON、XML等结构化格式。

## 方法对比
| 方法 | 可靠性 | 复杂度 | 适用模型 |
|------|--------|--------|----------|
| Function Calling | 高 | 低 | GPT/Claude/Qwen |
| JSON Mode | 中 | 低 | GPT-4o/Gemini |
| Pydantic解析 | 中 | 中 | 所有 |
| 提示工程 | 低 | 低 | 所有 |

## OpenAI Function Calling
```python
client.chat.completions.create(
    model='gpt-4o',
    messages=[...],
    response_format={'type': 'json_object'}
)
```

## Pydantic验证
```python
from pydantic import BaseModel
class Person(BaseModel):
    name: str
    age: int
    skills: list[str]

result = client.chat.completions.create(...)
person = Person.model_validate_json(result)
```
