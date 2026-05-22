# 流式输出详解

## 为什么用流式
- 降低首字延迟(TTFT)
- 提升用户体验(打字机效果)
- 支持长文本生成(避免超时)

## SSE协议
```
data: {"choices":[{"delta":{"content":"Hello"}}]}
data: {"choices":[{"delta":{"content":" World"}}]}
data: [DONE]
```

## Python实现
```python
stream = client.chat.completions.create(
    model='gpt-4o',
    messages=[...],
    stream=True
)
for chunk in stream:
    if chunk.choices[0].delta.content:
        print(chunk.choices[0].delta.content, end='', flush=True)
```

## 异步流式
```python
async for chunk in await client.chat.completions.create(..., stream=True):
    process(chunk)
```
