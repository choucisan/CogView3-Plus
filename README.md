# CogView3-Plus

## 🧠 简介 Introduction

**CogView3-Plus** 是基于清华大学提出的 [CogView3](https://arxiv.org/abs/2403.05121) 扩展改进的版本，聚焦于更高效的文本到图像生成（Text-to-Image Generation）任务。原始 CogView3 引入了 **Relay Diffusion** 技术，实现了更精细且更快速的文本图像生成。

本项目支持：

- CogView3-Plus源码
- 本地部署与示例

## Checkpoint 权重

请手动下载预训练模型

CogView3 官方权重 [HuggingFace 🤗 模型库](https://huggingface.co/THUDM) 或 [ModelScope](https://modelscope.cn/models) |
      
下载后放置于项目根目录下的 `./checkpoints/` 文件夹中，确保结构如下：

CogView3-Plus/
├── transformer
│   ├── 1
│   └── latest
├── T5
│   ├── ……
├── vae
    └──imagekl_ch16.pt


## 🚀 快速开始 Quick Start

### 1. 克隆仓库

```bash
git clone https://github.com/choucisan/CogView3-Plus.git
cd CogView3-Plus


2. 安装依赖

pip install -r requirements.txt

3. 下载模型权重

CogView3-Plus/
├── transformer
│   ├── 1
│   └── latest
├── T5
│   ├── ……
├── vae
    └──imagekl_ch16.pt
将权重文件放入上述目录






4. 文本生成图像
文本输入在configs/test.txt
运行：
python sample_dit.py --base configs/cogview3_plus.yaml



✍️引用 Citation
@article{zheng2024cogview3,
  title={Cogview3: Finer and faster text-to-image generation via relay diffusion},
  author={Zheng, Wendi and Teng, Jiayan and Yang, Zhuoyi and Wang, Weihan and Chen, Jidong and Gu, Xiaotao and Dong, Yuxiao and Ding, Ming and Tang, Jie},
  journal={arXiv preprint arXiv:2403.05121},
  year={2024}
}


📫 联系 Contact[]


- 是否支持 Web UI（例如 Gradio）？
- 想部署在哪些平台（例如 Hugging Face、Colab、Docker）？

需要我一键帮你生成 `requirements.txt` 吗？
