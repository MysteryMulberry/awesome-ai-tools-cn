# Model Context Protocol (MCP)

## 什么是MCP
MCP是Anthropic提出的AI模型上下文协议，标准化LLM与外部工具/数据的交互。

## 核心概念
- **MCP Server**: 提供工具和资源的服务端
- **MCP Client**: 连接Server的客户端
- **Tools**: 可调用的函数
- **Resources**: 可读取的数据
- **Prompts**: 可复用的提示模板

## 已支持的客户端
- Claude Desktop
- Cursor
- Continue
- Cline (VS Code)

## 开发Server
```python
from mcp.server import Server
server = Server('my-server')

@server.tool()
def search(query: str) -> str:
    return f'Search results for: {query}'
```

## 已有Server
- filesystem: 文件系统操作
- github: GitHub API集成
- postgres: 数据库查询
- puppeteer: 浏览器自动化
- brave-search: 搜索集成
