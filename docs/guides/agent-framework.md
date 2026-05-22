# AI Agent框架对比

## 主流框架

| 框架 | 语言 | 特点 | 适用场景 |
|------|------|------|---------|
| LangChain | Python | 链式调用，生态丰富 | 通用Agent开发 |
| CrewAI | Python | 多Agent协作 | 团队任务分配 |
| AutoGen | Python | 对话式多Agent | 研究讨论 |
| Dify | TypeScript | 可视化编排 | 低代码开发 |
| MetaGPT | Python | 角色扮演 | 软件工程 |

## Agent设计模式

### ReAct模式
```
思考 → 行动 → 观察 → 思考 → ...
```

### Plan-and-Execute模式
```
规划完整步骤 → 逐步执行 → 检查结果 → 调整
```

### 多Agent协作
```
Agent1(研究) → Agent2(编码) → Agent3(测试) → Agent4(审查)
```

---
*更新时间: {DATETIME_STR}*
