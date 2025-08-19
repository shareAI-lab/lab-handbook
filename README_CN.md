# ShareAI Lab 实验手册

ShareAI实验室新成员入门培训资料库 - 一周内掌握大语言模型微调技术

## 快速链接

### 🚀 在 Google Colab 中运行（推荐）
- [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shareAI-lab/lab-handbook/blob/main/LLM_SFT_for_ERNIE4_5_Chinese.ipynb) **中文教程**
- [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shareAI-lab/lab-handbook/blob/main/LLM_SFT_for_ERNIE4_5_English.ipynb) **英文教程 (English)**

## 项目简介

本仓库为ShareAI实验室新成员提供系统的入门培训材料，旨在帮助新成员在一周内快速掌握大语言模型（LLM）微调的核心技术和实践方法。

## 核心内容

### LLM微调教程
本仓库包含基于百度ERNIE-4.5模型的完整微调教程，涵盖：

- **监督式微调（SFT）** - 使用标注数据对预训练模型进行任务特定优化
- **参数高效微调（PEFT）** - 采用LoRA技术实现低资源消耗的模型适配
- **量化技术应用** - 通过4-bit量化大幅降低显存占用
- **实战案例演示** - 基于实际数据集的完整训练流程

## 技术栈

- **优化框架**: Unsloth - 提供2倍训练加速和60%显存节省
- **模型基座**: 百度ERNIE-4.5系列（0.3B/21B）
- **微调方法**: LoRA/QLoRA低秩适配技术
- **训练框架**: Hugging Face Transformers + TRL
- **量化工具**: bitsandbytes 4-bit/8-bit量化

## 快速开始

### 环境要求
- Python 3.8+
- CUDA 11.8+ (推荐12.1)
- GPU显存 >= 16GB (推荐24GB+用于21B模型)

### 安装步骤
```bash
# 克隆仓库
git clone https://github.com/shareai-lab/lab-handbook.git
cd lab-handbook

# 安装依赖
pip install --upgrade git+https://github.com/unslothai/unsloth.git
pip install bitsandbytes unsloth_zoo transformers trl
```

### 运行教程
打开Jupyter Notebook运行微调教程：
```bash
jupyter notebook LLM_SFT_for_ERNIE4_5_Chinese.ipynb
```

## 学习路径

### 第1-2天：理论基础
- 理解预训练模型原理
- 掌握微调技术概念
- 学习LoRA/PEFT原理

### 第3-4天：环境搭建
- 配置开发环境
- 熟悉工具链使用
- 运行示例代码

### 第5-6天：实践训练
- 准备自定义数据集
- 执行模型微调
- 调优超参数

### 第7天：项目实战
- 完成端到端项目
- 模型评估与部署
- 总结与分享

## 文件结构

```
lab-handbook/
├── README.md                              # 英文说明文档
├── README_CN.md                           # 中文说明文档
├── LLM_SFT_for_ERNIE4_5_Chinese.ipynb   # 中文微调教程
├── LLM_SFT_for_ERNIE4_5_English.ipynb   # 英文微调教程
└── outputs/                               # 训练输出目录
    └── ernie-4.5-0.3b-sft-merged/       # 微调后的模型权重
```

## 关键特性

- **零基础友好** - 从基础概念到实际操作的完整覆盖
- **资源优化** - 支持在消费级GPU上运行大模型微调
- **实战导向** - 基于真实场景的案例和最佳实践
- **快速迭代** - 高效的训练流程，快速验证想法

## 常见问题

### Q: 显存不足怎么办？
A: 可以尝试：
- 使用更小的模型（0.3B版本）
- 启用4-bit量化（load_in_4bit=True）
- 减小批处理大小
- 使用梯度累积

### Q: 训练速度太慢？
A: 建议：
- 确保使用了Unsloth优化
- 启用混合精度训练（fp16/bf16）
- 使用数据打包（packing=True）
- 优化数据加载流程

## 贡献指南

欢迎提交Issue和Pull Request来改进本项目。请确保：
- 代码符合项目规范
- 添加必要的文档说明
- 通过所有测试用例

## 许可证

本项目采用MIT许可证 - 详见LICENSE文件

## 联系方式

- 实验室主页：[ShareAI Lab](https://shareai-lab.github.io)
- 问题反馈：请提交GitHub Issue
- 技术交流：加入我们的技术社区

## 致谢

感谢以下开源项目的支持：
- [Unsloth](https://github.com/unslothai/unsloth)
- [Hugging Face](https://huggingface.co)
- [百度ERNIE](https://github.com/PaddlePaddle/ERNIE)

---
*让AI技术更易获得，让创新更快发生* - ShareAI Lab