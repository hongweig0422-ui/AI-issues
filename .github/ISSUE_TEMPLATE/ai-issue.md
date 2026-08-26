---
name: AMD AI 问题反馈
about: 提交 AMD GPU 上的 AI 框架、模型、兼容性或性能问题
title: "[框架名] [模型名] "
labels: ""
assignees: ""
---

## 问题概述
<!-- 用 1～3 句话描述你遇到的问题和期望行为 -->

## 环境信息

| 字段 | 内容 |
|------|------|
| **硬件** | <!-- 例：AMD AI Max 395 / Radeon RX 7900 XTX / Instinct MI300X --> |
| **CPU** | <!-- 例：AMD Ryzen 9 9950X --> |
| **内存** | <!-- 例：128 GB DDR5 --> |
| **操作系统** | <!-- 例：Ubuntu 22.04 / RHEL 9.4 --> |
| **ROCm 版本** | <!-- `rocminfo` 或 `hipconfig` 输出中的版本 --> |
| **驱动版本** | <!-- `rocm-smi` 或 `amdgpu-pro --version` --> |

## 软件栈

| 字段 | 内容 |
|------|------|
| **推理/训练框架** | <!-- 例：vLLM / llama.cpp / PyTorch / TensorRT-LLM / SGLang --> |
| **框架版本** | <!-- 例：vLLM 0.6.3 / llama.cpp b4123 / PyTorch 2.4.0+rocm6.1 --> |
| **后端** | <!-- 例：ROCm / HIP / Vulkan / CPU --> |
| **相关依赖版本** | <!-- 例：transformers 4.44.0, flash-attn 2.6.0 --> |
| **安装方式** | <!-- 例：pip / docker / 源码编译 / 官方 wheel --> |

## 模型信息

| 字段 | 内容 |
|------|------|
| **模型名称** | <!-- 例：Qwen3-8B-Instruct / Geneformer / Llama-3-8B --> |
| **模型来源** | <!-- HuggingFace 链接或本地路径 --> |
| **量化方式** | <!-- 例：FP16 / BF16 / INT8 / AWQ / GGUF Q4_K_M / 无量化 --> |
| **模型规模** | <!-- 例：8B / 70B --> |

## 问题详情

### 复现步骤
<!-- 按顺序列出操作步骤，越具体越好 -->
1.
2.
3.

### 实际行为
<!-- 描述实际发生了什么 -->

### 期望行为
<!-- 描述你期望发生什么 -->

### 相关算子 / API（如有）
<!-- 例：FlashAttention / paged_attention / custom_op::xxx / torch.compile -->
<!-- 如有报错中提到的 kernel 名、算子名、Python 函数名，请一并写出 -->

## 错误信息

### 完整错误日志
<!-- 请粘贴完整 traceback 或终端输出，不要只截一行 -->
```text
在此粘贴日志
```

### 截图
<!-- 拖拽上传终端报错、rocm-smi、性能对比等截图 -->

## 复现脚本（强烈建议）

<!-- 提供最小可复现示例（MWE），可以是：-->
<!-- - 完整的 Python 脚本 -->
<!-- - Docker Compose / Dockerfile -->
<!-- - 启动命令 + 配置文件 -->
<!-- - GitHub 仓库或 Gist 链接 -->

```bash
# 启动命令示例
python -m vllm.entrypoints.openai.api_server --model Qwen/Qwen3-8B ...
```

## 补充信息（可选）

- **对比环境**：如在 NVIDIA GPU 上是否正常？Vulkan 后端是否正常？
- **性能数据**：如有 benchmark 数字（tokens/s、latency），请附上
- **已尝试的 workaround**：换版本、换后端、降精度等
- **相关链接**：原帖链接、上游 Issue、文档链接

## 提交前自查

- [ ] 标题包含框架、模型和硬件
- [ ] 已填写具体硬件型号
- [ ] 已填写操作系统、ROCm/驱动和框架版本
- [ ] 已提供可执行的复现步骤
- [ ] 已提供完整错误日志
- [ ] 已搜索已有 Issues，确认不是重复问题
