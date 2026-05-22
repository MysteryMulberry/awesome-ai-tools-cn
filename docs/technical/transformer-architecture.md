# Transformer架构详解

## 核心组件

### 多头注意力 (Multi-Head Attention)
```python
class MultiHeadAttention(nn.Module):
    def __init__(self, d_model, n_heads):
        super().__init__()
        self.d_k = d_model // n_heads
        self.W_q = nn.Linear(d_model, d_model)
        self.W_k = nn.Linear(d_model, d_model)
        self.W_v = nn.Linear(d_model, d_model)

    def forward(self, Q, K, V, mask=None):
        scores = torch.matmul(Q, K.transpose(-2,-1)) / math.sqrt(self.d_k)
        if mask is not None:
            scores = scores.masked_fill(mask == 0, -1e9)
        attn = F.softmax(scores, dim=-1)
        return torch.matmul(attn, V)
```

### 位置编码
```python
class PositionalEncoding(nn.Module):
    def forward(self, x):
        pe = torch.zeros(x.size(1), x.size(2))
        pos = torch.arange(0, x.size(1)).unsqueeze(1)
        div = torch.exp(torch.arange(0, x.size(2), 2) * (-math.log(10000) / x.size(2)))
        pe[:, 0::2] = torch.sin(pos * div)
        pe[:, 1::2] = torch.cos(pos * div)
        return x + pe
```

## 变体
- **GPT系列**: 仅Decoder，自回归生成
- **BERT**: 仅Encoder，双向理解
- **T5**: Encoder-Decoder，文本到文本
- **LLaMA**: 高效Decoder，分组查询注意力

---
*更新时间: {DATETIME_STR}*
