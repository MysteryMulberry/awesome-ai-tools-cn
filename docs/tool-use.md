# 工具调用(Function/Tool Calling)

## 核心流程
1. 定义工具schema
2. 模型决定是否调用
3. 执行工具获取结果
4. 将结果返回模型
5. 模型生成最终回复

## 工具定义
```python
tools = [{
    'type': 'function',
    'function': {
        'name': 'get_weather',
        'description': '获取指定城市天气',
        'parameters': {
            'type': 'object',
            'properties': {
                'city': {'type': 'string', 'description': '城市名称'}
            },
            'required': ['city']
        }
    }
}]
```

## 多轮工具调用
模型可连续调用多个工具完成复杂任务

## 并行工具调用
GPT-4o支持一次调用多个独立工具
