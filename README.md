# OllamaForge
Not just another chat UI — a complete local LLM workstation from conversation to training to deployment.

<div align="center">

# 🦙 OllamaForge

### Chat · Fine-Tune · Pretrain · Deploy — All-in-One Local LLM Platform

[![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.115+-009688?logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Ollama](https://img.shields.io/badge/Ollama-Compatible-black)](https://ollama.com)
[![Platform](https://img.shields.io/badge/Platform-Windows%20|%20Linux%20|%20macOS-lightgrey)]()

**Not just another chat UI — a complete local LLM workstation from conversation to training to deployment.**

**不只是聊天界面 — 从对话、微调、预训练到部署，一站式本地大模型平台。**

[English](#-english) · [中文](#-中文) · [Quick Start / 快速开始](#-quick-start--快速开始)

---

![OllamaForge Main Interface](screenshots/1.png)

</div>

---

# 🇬🇧 English

## ✨ Why OllamaForge?

Most Ollama UIs stop at chat. **OllamaForge goes much further:**

| | Chat-only UIs | **OllamaForge** |
|---|:---:|:---:|
| 💬 Elegant Chat Interface | ✅ | ✅ |
| 🧠 Thinking Mode & Code Highlighting | ❌ | ✅ |
| 🔧 Fine-Tune Models (QLoRA / LoRA) | ❌ | ✅ |
| 🏗️ Pretrain from Scratch | ❌ | ✅ |
| 🧩 Visual Architecture Designer | ❌ | ✅ |
| ⚡ Quantization & HuggingFace Import | ❌ | ✅ |
| 🔑 OpenAI-Compatible API Sharing | ❌ | ✅ |
| 📊 Real-time Training Dashboard | ❌ | ✅ |

---

## 🎯 Features

### 💬 Chat Interface

![Chat Interface](screenshots/1.png)

- **Multi-conversation** sidebar with full history
- **Thinking Mode** — unfold the model's chain-of-thought reasoning
- **Device Control** — GPU / CPU / Hybrid inference switching
- **Keep-Alive** — instant / 5 min / 30 min / 1 hr / permanent
- **Full parameter tuning** — Temperature, Top P, Repeat Penalty, Context Length, Seed
- **Running model panel** — VRAM usage, one-click unload
- **Code highlighting** + **LaTeX rendering** + **Image understanding**
- **System prompt presets** — Assistant, Coder, Translator, Writer, Analyst
- **Generation stats** — tokens/s, token count, elapsed time

---

### 🔧 Fine-Tune Center

Turn any base model into your domain expert — **zero command line, zero config files.**

![Fine-Tune Methods](screenshots/3.png)

**Four approaches for every skill level:**

| Method | GPU | Time | Use Case |
|--------|:---:|:---:|----------|
| Modelfile Customization | ❌ None | < 1 min | Prompt engineering |
| **QLoRA 4-bit** | ≥ 8 GB | 1–4 h | Best efficiency ⭐ |
| LoRA 16-bit | ≥ 24 GB | 2–8 h | Higher precision |
| Import GGUF | ❌ None | < 5 min | External models |

**Key capabilities:**

- 🔍 **Auto hardware detection** — GPU, VRAM, CUDA version, disk space
- 📦 **One-click install** — auto-matches PyTorch to your CUDA
- 🤗 **Curated model list** — filter by vendor, size, VRAM requirement
- 📊 **Dataset management** — upload JSONL/JSON/CSV, download from HuggingFace, auto-format detection (Alpaca / ShareGPT / OpenAI)
- ⚙️ **Full hyperparameters** — LoRA rank/alpha, epochs, batch size, LR, seq length, quantization
- 📈 **Real-time monitor** — live progress bar, loss, step counter, log streaming
- ✅ **Auto-deploy** — merged model auto-registered to Ollama after training
- 🔄 **Resume training** — checkpoint-based continuation

![Hardware Detection](screenshots/2.png)

![QLoRA Configuration](screenshots/4.png)

![Dataset Management](screenshots/5.png)

![Training Log](screenshots/21.jpg)

![Training History](screenshots/6.png)

#### Fine-Tune: Before vs After

A **Qwen 0.5B** model fine-tuned with code dataset:

| Before | After |
|:---:|:---:|
| ![Before](screenshots/16.jpg) | ![After](screenshots/17.jpg) |
| ❌ *"I cannot generate code"* | ✅ *Complete Python PSO implementation* |

---

### 🏗️ Pretrain Lab — Build Your Own LLM from Scratch

**Design, train, and deploy a language model from zero** — entirely through a visual interface. The crown jewel of OllamaForge.

![Pretrain Lab Overview](screenshots/11.png)

#### 🧩 Visual Architecture Designer

Drag-and-drop Transformer blocks. Real-time parameter stats. No code.

![Architecture Editor](screenshots/12.png)

- **9 templates** — GPT-2 Small/Medium, LLaMA Tiny/Small, Mistral Tiny, Phi Tiny, Gemma Tiny, MoE Tiny, Custom
- **Component palette** — Embedding, Self-Attention, Cross-Attention, FFN, MoE Layer, Residual Add, Dropout, Gating, and more
- **Architecture choices** — RoPE / ALiBi / Absolute, SwiGLU / GELU / ReLU, MHA / GQA / MQA, LayerNorm / RMSNorm
- **Live stats** — total params, FP16 training VRAM, inference VRAM, embedding ratio
- **Export / Import JSON** architecture configs

#### 📖 Tokenizer Workshop

![Tokenizer Builder](screenshots/13.png)

- 6 pretrained tokenizers (GPT-2, LLaMA 2/3, Qwen 2, Mistral, BERT Chinese)
- Train custom tokenizer from your data
- Live color-coded tokenization preview

#### 📚 Data Preparation

![Data Preparation](screenshots/14.png)

- **Recommended datasets** — TinyStories, WikiText-103/2, Chinese Wikipedia, SlimPajama, FineWeb-Edu
- Upload, paste, or download from HuggingFace
- Auto tokenize & pack

#### 📈 Training & Monitoring

![Training Loss Curve](screenshots/20.jpg)

![Training Config](screenshots/15.png)

- **Live dashboard** — step, loss curve, learning rate, tok/s, GPU device
- **Auto text generation** — watch your model learn to speak every N steps
- **LR schedulers** — Cosine / Linear / Constant
- **FP16 mixed precision** + **multi-GPU DDP**
- **Checkpoint save & resume**

#### 🎨 See Your Model Learn to Speak

A **39.6M parameter** LLaMA Tiny, trained from scratch on Chinese classical literature:

| Trained on Four Great Classical Novels | Trained on Classical Chinese Poetry |
|:---:|:---:|
| ![Novel Generation](screenshots/18.jpg) | ![Poetry Generation](screenshots/19.jpg) |
| *Dream of the Red Chamber* style dialogue | Classical Chinese verse generation |

> 🏮 From random noise to coherent literature — a tiny model trained entirely through this GUI.

---

### 🔨 Model Workshop

Full lifecycle management for your local models.

![Model Management](screenshots/7.png)

#### HuggingFace Import

Download safetensors → auto-quantize → register to Ollama. One click.

![HF Import](screenshots/8.png)

#### Quantization Conversion

![Quantization](screenshots/9.png)

| Quant | Size (7B) | Quality | Speed | Best For |
|:---:|:---:|:---:|:---:|---|
| Q4_K_M | ~4.1 GB | ★★★★ | ★★★★★ | Daily use |
| Q5_K_M | ~4.8 GB | ★★★★½ | ★★★★ | Balanced |
| Q8_0 | ~7.2 GB | ★★★★★ | ★★★ | Best quality |
| Q3_K_M | ~3.3 GB | ★★★ | ★★★★★ | Low VRAM |
| F16 | ~13.5 GB | ★★★★★ | ★★ | Lossless / re-quant |

---

### 🔑 API Sharing Center

Share your local models through a standard OpenAI-compatible endpoint.

![API Sharing](screenshots/10.png)

- **OpenAI-compatible** `/v1/chat/completions`
- **Key management** — rate limits, daily quotas, expiration, per-model restrictions
- **Usage dashboard** — active keys, call stats, available models
- **Code examples** — cURL + Python (OpenAI SDK) ready to copy
- **LAN sharing** — admin token for secure network access; localhost auto-bypass

```python
from openai import OpenAI

client = OpenAI(base_url="http://localhost:8751/v1", api_key="ogk-your-key")
r = client.chat.completions.create(
    model="qwen3:4b",
    messages=[{"role": "user", "content": "Hello!"}]
)
print(r.choices[0].message.content)
```

---

## 🚀 Quick Start / 快速开始

### Prerequisites / 前置要求

- **Python 3.10+**
- **[Ollama](https://ollama.com)** installed and running (`ollama serve`)

### Install & Run / 安装与运行

```bash
git clone https://github.com/YOUR_USERNAME/ollama-forge.git
cd ollama-forge

pip install -r requirements.txt

python run.py
```

Browser opens automatically at `http://localhost:8751` 🎉

### Fine-Tuning Setup (Optional) / 微调环境（可选）

**Option A: One-Click** — click "一键安装" in the Fine-Tune Center UI.

**Option B: Manual**

```bash
conda create -n ollama-forge python=3.11 -y
conda activate ollama-forge

# Install PyTorch (check CUDA version: nvidia-smi)
pip install torch==2.4.0 --index-url https://download.pytorch.org/whl/cu121

pip install -r requirements-finetune.txt
```

### Custom Data Directory / 自定义数据目录

Default: `~/.ollama-gui-finetune`. Change in the UI (Hardware Detection tab) or via environment variable:

```bash
# Windows
$env:OLLAMA_GUI_FT_DIR = "D:\ollama-forge-data"

# Linux / macOS
export OLLAMA_GUI_FT_DIR=/data/ollama-forge
```

---

## 📐 Project Structure / 项目结构

```
ollama-forge/
├── run.py                      # One-command entry point / 一键启动
├── config.json                 # Persistent config / 持久化配置
├── requirements.txt            # Core: FastAPI, httpx, uvicorn
├── requirements-finetune.txt   # Training: PyTorch, PEFT, TRL
├── backend/
│   ├── app.py                  # Main server — chat, fine-tune, workshop, API
│   └── pretrain/
│       ├── architect.py        # Architecture templates & validation
│       ├── tokenizer_builder.py
│       ├── data_manager.py
│       ├── trainer.py          # Training loop & monitoring
│       ├── streaming.py        # Real-time training stream
│       ├── inference.py        # Text generation
│       ├── exporter.py         # GGUF export & Ollama deploy
│       └── routes.py
└── frontend/
    ├── index.html
    ├── app.js                  # Chat & core UI
    ├── pretrain-lab.js         # Pretrain Lab UI
    └── styles.css              # Dark theme + amber accents
```

---

## 🛠️ Tech Stack / 技术栈

| Layer | Technology |
|-------|-----------|
| Backend | Python · FastAPI · Uvicorn · httpx |
| Frontend | Vanilla JS — zero framework dependencies |
| Fine-Tuning | HuggingFace PEFT + TRL (no Unsloth needed) |
| Quantization | llama.cpp GGUF |
| Code Highlight | highlight.js |
| Math Rendering | KaTeX |

---

## 🗺️ Roadmap

- [ ] English UI / 英文界面国际化
- [ ] RAG integration / RAG 检索增强
- [ ] Model evaluation benchmarks / 模型评测
- [ ] Docker deployment / Docker 部署
- [ ] Plugin system / 插件系统
- [ ] Multi-user collaboration / 多用户协作
- [ ] Cross-run loss comparison / 跨训练 Loss 对比

---

<br>

---

<br>

# 🇨🇳 中文

## ✨ 为什么选择 OllamaForge？

大多数 Ollama 界面只做到了聊天。**OllamaForge 远不止于此：**

| | 普通聊天 UI | **OllamaForge** |
|---|:---:|:---:|
| 💬 优雅的聊天界面 | ✅ | ✅ |
| 🧠 思考模式 & 代码高亮 | ❌ | ✅ |
| 🔧 模型微调 (QLoRA / LoRA) | ❌ | ✅ |
| 🏗️ 从零预训练 | ❌ | ✅ |
| 🧩 可视化架构设计器 | ❌ | ✅ |
| ⚡ 量化转换 & HuggingFace 导入 | ❌ | ✅ |
| 🔑 OpenAI 兼容 API 共享 | ❌ | ✅ |
| 📊 实时训练监控面板 | ❌ | ✅ |

---

## 🎯 功能特性

### 💬 聊天界面

![聊天界面](screenshots/1.png)

- **多会话管理** — 侧边栏历史记录
- **思考模式** — 展开模型的推理链
- **设备切换** — GPU / CPU / 混合推理一键切换
- **Keep-Alive 控制** — 即时 / 5分 / 30分 / 1时 / 永久
- **完整参数调节** — Temperature、Top P、重复惩罚、上下文长度、种子
- **运行模型面板** — 查看显存占用、一键卸载
- **代码高亮** + **LaTeX 公式渲染** + **图片理解**
- **系统提示词预设** — 助手、编程、翻译、写作、分析
- **生成统计** — tok/s、token 数、耗时

---

### 🔧 微调中心

把任何基座模型变成你的领域专家 — **不用命令行，不用写配置文件。**

![微调方式](screenshots/3.png)

**四种微调方式，适配不同需求：**

| 方式 | GPU 要求 | 耗时 | 适用场景 |
|------|:---:|:---:|---------|
| Modelfile 定制 | ❌ 无需 | < 1 分钟 | 提示词工程 |
| **QLoRA 4-bit** | ≥ 8 GB | 1–4 小时 | 效率最佳 ⭐ |
| LoRA 16-bit | ≥ 24 GB | 2–8 小时 | 更高精度 |
| 导入 GGUF | ❌ 无需 | < 5 分钟 | 导入外部模型 |

**核心能力：**

- 🔍 **硬件自动检测** — GPU 型号、显存、CUDA 版本、磁盘空间
- 📦 **一键安装依赖** — 自动匹配 CUDA 版本安装对应 PyTorch
- 🤗 **推荐模型列表** — 按厂商、大小、显存需求筛选
- 📊 **数据集管理** — 上传 JSONL/JSON/CSV、从 HuggingFace 下载、自动识别格式（Alpaca / ShareGPT / OpenAI）
- ⚙️ **超参数控制** — LoRA rank/alpha、Epochs、Batch Size、学习率、序列长度、量化方式
- 📈 **实时监控** — 进度条、Loss、步数、日志流
- ✅ **自动部署** — 训练完成后自动合并 LoRA 并注册到 Ollama
- 🔄 **断点续训** — 基于 Checkpoint 恢复训练

![硬件检测](screenshots/2.png)

![QLoRA 配置](screenshots/4.png)

![数据集管理](screenshots/5.png)

![训练日志](screenshots/21.jpg)

![历史记录](screenshots/6.png)

#### 📊 微调效果：前后对比

使用代码数据集微调 **Qwen 0.5B**：

| 微调前 | 微调后 |
|:---:|:---:|
| ![微调前](screenshots/16.jpg) | ![微调后](screenshots/17.jpg) |
| ❌ *"我无法生成或创建代码"* | ✅ *完整的 Python PSO 粒子群优化实现* |

---

### 🏗️ 训练实验室 — 从零打造你的大模型

**设计架构、训练模型、部署使用** — 全程可视化操作。OllamaForge 的王牌功能。

![训练实验室](screenshots/11.png)

#### 🧩 可视化架构设计器

拖拽 Transformer 组件，实时参数统计，无需写代码。

![架构编辑器](screenshots/12.png)

- **9 种预设模板** — GPT-2 Small/Medium、LLaMA Tiny/Small、Mistral Tiny、Phi Tiny、Gemma Tiny、MoE Tiny、自定义极简
- **完整组件面板**：
  - 核心层：Embedding、Self-Attention、Cross-Attention、FFN、Linear、LM Head
  - 归一化：Pre-Norm、Post-Norm、Final Norm（LayerNorm / RMSNorm）
  - 连接：Residual Add、Dropout、Skip Connect、Gating
  - 高级：MoE Layer、Parallel、KV Cache
- **架构选择** — RoPE / ALiBi / 绝对位置编码，SwiGLU / GELU / ReLU，MHA / GQA / MQA
- **实时统计** — 总参数量、FP16 训练显存、推理显存、Embedding 占比
- **导出 / 导入 JSON** 架构配置

#### 📖 词表构建

![词表构建](screenshots/13.png)

- 6 种预训练 Tokenizer（GPT-2、LLaMA 2/3、Qwen 2、Mistral、BERT 中文）
- 从你的数据训练自定义 Tokenizer
- 实时分词预览，不同颜色标注不同 token

#### 📚 数据准备

![数据准备](screenshots/14.png)

- **推荐数据集** — TinyStories、WikiText-103/2、中文维基百科、SlimPajama、FineWeb-Edu
- 上传文件、粘贴文本、或从 HuggingFace 下载
- 自动分词打包为训练格式

#### 📈 训练与监控

![Loss 曲线](screenshots/20.jpg)

![训练配置](screenshots/15.png)

- **实时面板** — 步数、Loss 曲线、学习率、tok/s、GPU 设备
- **自动生成文本** — 每 N 步模型自动试说话，观察模型从乱码到流畅的全过程
- **学习率调度** — Cosine / Linear / Constant
- **FP16 混合精度** + **多卡分布式 (DDP)**
- **Checkpoint 保存与恢复**

#### 🎨 看你的模型学会说话

**39.6M 参数** LLaMA Tiny 架构，使用中国古典文学从零预训练：

| 四大名著训练 | 古诗词训练 |
|:---:|:---:|
| ![小说生成](screenshots/18.jpg) | ![诗词生成](screenshots/19.jpg) |
| 生成《红楼梦》风格对话 | 生成工整的古诗词 |

> 🏮 从随机噪声到文言对话 — 仅 39.6M 参数的小模型，完全通过本 GUI 从零训练而成。

---

### 🔨 模型工坊

本地模型的全生命周期管理。

![模型管理](screenshots/7.png)

#### HuggingFace 导入

输入模型 ID → 自动下载 safetensors → 量化 → 注册到 Ollama，一步完成。

![HF 导入](screenshots/8.png)

#### 量化转换

将高精度模型转为低精度，节省显存、加速推理。

![量化转换](screenshots/9.png)

| 量化类型 | 体积 (7B) | 质量 | 速度 | 适用场景 |
|:---:|:---:|:---:|:---:|---------|
| Q4_K_M | ~4.1 GB | ★★★★ | ★★★★★ | 日常使用首选 |
| Q5_K_M | ~4.8 GB | ★★★★½ | ★★★★ | 显存充足时推荐 |
| Q8_0 | ~7.2 GB | ★★★★★ | ★★★ | 追求最佳质量 |
| Q3_K_M | ~3.3 GB | ★★★ | ★★★★★ | 显存紧张 |
| F16 | ~13.5 GB | ★★★★★ | ★★ | 无损存储 / 后续量化 |

---

### 🔑 API 共享中心

通过标准 OpenAI 兼容接口，将本地模型共享给团队。

![API 共享](screenshots/10.png)

- **OpenAI 兼容** `/v1/chat/completions` 接口
- **密钥管理** — 速率限制、每日配额、过期时间、指定可用模型
- **使用面板** — 活跃密钥数、调用统计、可用模型数
- **代码示例** — cURL + Python (OpenAI SDK) 即拿即用
- **局域网共享** — Admin Token 安全访问；本机免认证

```python
from openai import OpenAI

client = OpenAI(base_url="http://localhost:8751/v1", api_key="ogk-你的密钥")
r = client.chat.completions.create(
    model="qwen3:4b",
    messages=[{"role": "user", "content": "你好！"}]
)
print(r.choices[0].message.content)
```

---

## 🤝 Contributing / 贡献

Contributions welcome! 欢迎提交 PR！

```bash
Fork → git checkout -b feature/xxx → commit → push → Pull Request
```

---

## 📄 License

MIT License — see [LICENSE](LICENSE)

---

<div align="center">

**Built with ❤️ for the local LLM community**

🦙 *Your models. Your data. Your machine. No cloud required.*

🦙 *你的模型，你的数据，你的机器。无需云端。*

⭐ **如果觉得有用，请给个 Star！/ If you find it useful, please star!** ⭐

<!-- [![Star History Chart](https://api.star-history.com/svg?repos=YOUR_USERNAME/ollama-forge&type=Date)](https://star-history.com/#YOUR_USERNAME/ollama-forge&Date) -->

</div>
