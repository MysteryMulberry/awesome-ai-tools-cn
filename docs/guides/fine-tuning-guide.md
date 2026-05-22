# 模型微调指南

## 微调方法对比

| 方法 | 参数量 | GPU内存 | 效果 |
|------|--------|---------|------|
| Full Fine-tuning | 100% | 高 | 最佳 |
| LoRA | 0.1-1% | 低 | 良好 |
| QLoRA | 0.1-1% | 极低 | 良好 |
| Prefix Tuning | <0.1% | 低 | 中等 |

## 使用LlamaFactory微调
```bash
llamafactory-cli train \
  --model_name_or_path meta-llama/Llama-3-8B \
  --dataset alpaca_zh \
  --finetuning_type lora \
  --lora_rank 8 \
  --output_dir ./output
```

## 数据准备
- 确保数据质量和多样性
- 使用Alpaca格式: instruction/input/output
- 数据清洗: 去重、过滤低质量样本
- 数据增强: 同义改写、回译

---
*更新时间: {DATETIME_STR}*
