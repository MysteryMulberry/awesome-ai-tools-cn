# CrewAI

多Agent协作框架，角色分工执行任务。

## 特性
- 多Agent角色定义
- 任务串行/并行
- 工具共享
- 记忆管理

```python
from crewai import Agent, Task, Crew
researcher = Agent(role='研究员', goal='深入研究主题')
writer = Agent(role='撰写者', goal='输出高质量文章')
crew = Crew(agents=[researcher, writer], tasks=[...])
result = crew.kickoff()
```
