# Vercel AI SDK

全栈AI应用开发工具集。

## 特性
- React/Next.js/Svelte组件
- 流式UI渲染
- 工具调用支持
- 多Provider切换

## 快速开始
```bash
npm install ai @ai-sdk/openai
```

```tsx
import { generateText } from 'ai';
const { text } = await generateText({
    model: openai('gpt-4o'),
    prompt: 'Hello!'
});
```
