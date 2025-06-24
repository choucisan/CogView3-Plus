# CogView3-Plus

## 项目简介

**CogView3-Plus** 是基于清华大学提出的 [CogView3](https://arxiv.org/abs/2403.05121) 模型扩展和改进的版本，致力于实现更高效、更精细的文本到图像生成（Text-to-Image Generation）。原始 CogView3 引入了 **Relay Diffusion** 技术，在生成质量与生成速度之间取得了更优的平衡。

本项目提供：

- CogView3-Plus 源码；
- 本地部署与使用示例；
- 支持快速文本生成图像的推理功能。

---

## 📦 模型权重（Checkpoint）

请手动下载预训练模型权重，推荐来源如下：

- [HuggingFace 官方模型库](https://huggingface.co/THUDM)
- [ModelScope 魔搭社区](https://modelscope.cn/models)

下载后，将模型放置于项目根目录下的 `./checkpoints/` 目录，目录结构如下：

```
CogView3-Plus/
├── checkpoints/
│   ├── transformer/
│   │   ├── 1/
│   │   └── latest/
│   ├── T5/
│   │   └── ...（T5子模型权重）
│   └── vae/
│       └── imagekl_ch16.pt
```

---

## 🚀 快速开始（Quick Start）

### 克隆仓库

```bash
git clone https://github.com/choucisan/CogView3-Plus.git
cd CogView3-Plus
```

### 安装依赖

```bash
pip install -r requirements.txt
```

### 准备模型权重

将下载好的模型权重文件放入 `checkpoints/` 目录中，确保结构如上所示。

### 运行推理脚本（文本生成图像）

请将输入文本写入 `configs/test.txt`，每行为一条生成指令。

执行命令：

```bash
python sample_dit.py --base configs/cogview3_plus.yaml
```

生成图像结果将保存在默认输出目录下。

---

Citation
```bibtex
@article{zheng2024cogview3,
  title={Cogview3: Finer and faster text-to-image generation via relay diffusion},
  author={Zheng, Wendi and Teng, Jiayan and Yang, Zhuoyi and Wang, Weihan and Chen, Jidong and Gu, Xiaotao and Dong, Yuxiao and Ding, Ming and Tang, Jie},
  journal={arXiv preprint arXiv:2403.05121},
  year={2024}}
```

---

联系方式: choucisan@gmail.com
