# RLHF训练流程

## 三阶段流程

### 阶段1: SFT (监督微调)
```python
# 用高质量指令数据微调基础模型
trainer = SFTTrainer(
    model=base_model,
    train_dataset=sft_data,
    max_seq_length=2048,
)
trainer.train()
```

### 阶段2: RM (奖励模型训练)
```python
# 用人类偏好数据训练奖励模型
# 数据格式: (prompt, chosen_response, rejected_response)
rm_trainer = RewardModelTrainer(
    model=rm_model,
    train_dataset=preference_data,
)
rm_trainer.train()
```

### 阶段3: PPO (强化学习优化)
```python
# 用奖励模型指导策略优化
ppo_trainer = PPOTrainer(
    model=actor_model,
    ref_model=ref_model,
    reward_model=rm_model,
)
ppo_trainer.train()
```

## 替代方案
- **DPO**: 直接偏好优化，无需奖励模型
- **ORPO**: 无需参考模型的偏好优化

---
*更新时间: {DATETIME_STR}*
