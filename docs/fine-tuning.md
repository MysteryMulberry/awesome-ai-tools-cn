# 模型微调指南

## 方法对比
| 方法 | 显存需求 | 数据量 | 效果 |
|------|---------|--------|------|
| Full Fine-tune | 高 | 多 | 最好 |
| LoRA | 低 | 少 | 好 |
| QLoRA | 极低 | 少 | 较好 |
| P-Tuning | 极低 | 少 | 一般 |

## LoRA微调步骤
1. 准备数据集(JSONL格式)
2. 配置训练参数
3. 使用PEFT库训练
4. 合并LoRA权重
5. 部署推理

## 工具
- unsloth: 快速微调
- LLaMA-Factory: WebUI微调
- axolotl: 配置驱动训练
