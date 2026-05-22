# LangGraph

LangChain图状态机，构建复杂Agent工作流。

## 特性
- 图状态管理
- 循环与分支
- 人机协作断点
- 持久化检查点

## 核心概念
- **State**: 共享状态对象
- **Node**: 状态处理函数
- **Edge**: 条件转移

```python
from langgraph.graph import StateGraph
graph = StateGraph(AgentState)
graph.add_node('think', think_node)
graph.add_node('act', act_node)
graph.add_edge('think', 'act')
```
