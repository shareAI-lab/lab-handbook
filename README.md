# ShareAI Lab Handbook

A comprehensive training repository for new ShareAI Lab members - Master LLM fine-tuning techniques within one week

## Project Overview

This repository provides systematic onboarding materials for new ShareAI Lab members, designed to help them quickly master the core technologies and practical methods of Large Language Model (LLM) fine-tuning within one week.

## Core Content

### LLM Fine-tuning Tutorial
This repository contains a complete fine-tuning tutorial based on Baidu's ERNIE-4.5 model, covering:

- **Supervised Fine-Tuning (SFT)** - Task-specific optimization of pre-trained models using labeled data
- **Parameter-Efficient Fine-Tuning (PEFT)** - Low-resource model adaptation using LoRA technology
- **Quantization Techniques** - Significant memory reduction through 4-bit quantization
- **Practical Demonstrations** - Complete training workflows with real datasets

## Technology Stack

- **Optimization Framework**: Unsloth - Provides 2x training acceleration and 60% memory savings
- **Base Models**: Baidu ERNIE-4.5 series (0.3B/21B)
- **Fine-tuning Methods**: LoRA/QLoRA low-rank adaptation techniques
- **Training Framework**: Hugging Face Transformers + TRL
- **Quantization Tools**: bitsandbytes 4-bit/8-bit quantization

## Quick Start

### System Requirements
- Python 3.8+
- CUDA 11.8+ (12.1 recommended)
- GPU Memory >= 16GB (24GB+ recommended for 21B model)

### Installation Steps
```bash
# Clone repository
git clone https://github.com/shareai-lab/lab-handbook.git
cd lab-handbook

# Install dependencies
pip install --upgrade git+https://github.com/unslothai/unsloth.git
pip install bitsandbytes unsloth_zoo transformers trl
```

### Run Tutorial
Open the Jupyter Notebook to run the fine-tuning tutorial:
```bash
jupyter notebook LLM_SFT_for_ERNIE4_5_English.ipynb
```

## Learning Path

### Days 1-2: Theoretical Foundation
- Understand pre-trained model principles
- Master fine-tuning concepts
- Learn LoRA/PEFT principles

### Days 3-4: Environment Setup
- Configure development environment
- Familiarize with toolchain
- Run example code

### Days 5-6: Practical Training
- Prepare custom datasets
- Execute model fine-tuning
- Optimize hyperparameters

### Day 7: Project Practice
- Complete end-to-end project
- Model evaluation and deployment
- Summary and sharing

## File Structure

```
lab-handbook/
├── README.md                              # English documentation
├── README_CN.md                           # Chinese documentation
├── LLM_SFT_for_ERNIE4_5_.ipynb          # Chinese tutorial
├── LLM_SFT_for_ERNIE4_5_English.ipynb   # English tutorial
└── outputs/                               # Training output directory
    └── ernie-4.5-0.3b-sft-merged/       # Fine-tuned model weights
```

## Key Features

- **Beginner-Friendly** - Complete coverage from basic concepts to practical operations
- **Resource-Optimized** - Supports large model fine-tuning on consumer-grade GPUs
- **Practice-Oriented** - Real-world scenarios and best practices
- **Fast Iteration** - Efficient training workflow for rapid idea validation

## FAQ

### Q: What if I run out of memory?
A: Try:
- Using a smaller model (0.3B version)
- Enabling 4-bit quantization (load_in_4bit=True)
- Reducing batch size
- Using gradient accumulation

### Q: Training is too slow?
A: Recommendations:
- Ensure Unsloth optimization is enabled
- Enable mixed precision training (fp16/bf16)
- Use data packing (packing=True)
- Optimize data loading pipeline

## Contributing

We welcome Issues and Pull Requests to improve this project. Please ensure:
- Code follows project standards
- Necessary documentation is added
- All test cases pass

## License

This project is licensed under the MIT License - see LICENSE file for details

## Contact

- Lab Homepage: [ShareAI Lab](https://shareai-lab.github.io)
- Issue Reporting: Please submit GitHub Issues
- Technical Discussion: Join our technical community

## Acknowledgments

Thanks to the following open-source projects:
- [Unsloth](https://github.com/unslothai/unsloth)
- [Hugging Face](https://huggingface.co)
- [Baidu ERNIE](https://github.com/PaddlePaddle/ERNIE)

---
*Making AI technology more accessible, making innovation happen faster* - ShareAI Lab