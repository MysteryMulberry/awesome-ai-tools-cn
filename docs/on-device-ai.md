# 端侧AI

## 为什么端侧运行
- 隐私: 数据不出设备
- 延迟: 无网络往返
- 离线: 无网也可用
- 成本: 零API费用

## 框架
| 框架 | 平台 | 模型 |
|------|------|------|
| MLX | Apple Silicon | Llama/Qwen |
| Core ML | iOS/macOS | 优化模型 |
| TensorFlow Lite | Android | MobileBERT |
| ONNX Runtime | 全平台 | 通用 |
| llama.cpp | CPU/GPU | GGUF模型 |

## 推荐配置
| 模型 | 最低RAM | 推荐设备 |
|------|---------|----------|
| 7B Q4 | 8GB | M1/8GB PC |
| 7B Q8 | 16GB | M2/16GB PC |
| 13B Q4 | 16GB | M2 Pro |
