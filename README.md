<div align="center">

<img src="https://img.shields.io/badge/🦙-OllamaForge-black?style=for-the-badge&labelColor=F59E0B&color=111827" alt="OllamaForge" height="40">

# OllamaForge

### 🔥 The Only Ollama UI That Lets You **Chat**, **Fine-Tune**, **Pretrain from Scratch**, and **Deploy** — All in One Interface

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.115+-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![Ollama](https://img.shields.io/badge/Ollama-Compatible-black?style=flat-square)](https://ollama.com)
[![Platform](https://img.shields.io/badge/Windows%20|%20Linux%20|%20macOS-grey?style=flat-square)]()
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square)](https://github.com/zhengxuanjiang/ollama-forge/pulls)

<br>

**🇬🇧 A 39.6M-parameter model trained from scratch through this GUI can write classical Chinese poetry.**
**🇨🇳 通过这个界面从零训练的 3960 万参数模型，能够生成古诗词和《红楼梦》风格对话。**

<br>

[English](#-english) · [中文](#-中文) · [Quick Start](#-quick-start--快速开始) · [Screenshots](#-screenshots-gallery--截图画廊)

<br>

![OllamaForge Hero](screenshots/1.png)

<br>

</div>

---

> **💡 Other Ollama UIs let you chat. OllamaForge lets you build.**
>
> Most tools give you a textbox and a send button. OllamaForge gives you a **complete AI workstation** — chat with models, fine-tune them on your data, design Transformer architectures visually, pretrain language models from scratch, quantize and convert models, share them via API — all without leaving the browser.
>
> **💡 别的 Ollama 界面让你聊天，OllamaForge 让你造模型。**
>
> 大多数工具只给你一个输入框。OllamaForge 给你一个**完整的 AI 工作站** — 聊天对话、数据微调、可视化设计 Transformer 架构、从零预训练、量化转换、API 共享 — 全部在浏览器中完成。

---

# 🇬🇧 English

## 📊 At a Glance

| | Chat-only UIs | **OllamaForge** |
|---|:---:|:---:|
| 💬 Multi-turn Chat with History | ✅ | ✅ |
| 🧠 Thinking Mode (Chain-of-Thought) | rare | ✅ |
| 🎨 Code Highlighting + LaTeX + Vision | partial | ✅ |
| ⚡ GPU/CPU/Hybrid Switching | ❌ | ✅ |
| 🔧 QLoRA / LoRA Fine-Tuning | ❌ | ✅ |
| 🏗️ Pretrain a Model from Zero | ❌ | ✅ |
| 🧩 Drag-and-Drop Architecture Designer | ❌ | ✅ |
| 📖 Custom Tokenizer Training | ❌ | ✅ |
| ⚡ HuggingFace Import + Quantization | ❌ | ✅ |
| 🔑 OpenAI-Compatible API with Key Mgmt | ❌ | ✅ |
| 📈 Live Training Dashboard + Loss Curves | ❌ | ✅ |
| 🚀 One-Click Deploy to Ollama | ❌ | ✅ |

---

## 🎯 Features

### 💬 Chat Interface — Beautiful, Fast, Full-Featured

> Not just another chat window. Every detail is crafted for power users.

![Chat Interface](screenshots/1.png)

<table>
<tr><td width="50%">

**Conversation & Generation**
- Multi-conversation sidebar with search
- Streaming responses with real-time stats (tokens/s, token count, elapsed time)
- Thinking Mode — expand to see the model's reasoning chain
- System prompt presets: Assistant / Coder / Translator / Writer / Analyst
- Image upload for vision models (LLaVA, Qwen-VL, etc.)

</td><td width="50%">

**Model & Inference Control**
- One-click device switching: Auto / GPU / CPU / Hybrid
- Keep-Alive timer: Instant / 5min / 30min / 1hr / Permanent
- Full parameter panel: Temperature, Top P, Repeat Penalty, Context Length (512–128K), Seed
- Running model dashboard: see VRAM usage, uptime, one-click unload
- Code highlighting (highlight.js) + LaTeX rendering (KaTeX)

</td></tr>
</table>

---

### 🔧 Fine-Tune Center — From Base Model to Domain Expert, No Code

> **Upload your data. Pick a model. Click train. That's it.**
> Your fine-tuned model auto-registers to Ollama and is ready to chat immediately.

![Fine-Tune Methods](screenshots/3.png)

#### Four Methods for Every Skill Level

| Method | GPU Required | Time | Difficulty | Best For |
|--------|:---:|:---:|:---:|----------|
| 📝 **Modelfile Customization** | ❌ None | < 1 min | ⭐ Beginner | Prompt engineering, few-shot |
| 🚀 **QLoRA 4-bit Fine-Tune** | ≥ 8 GB VRAM | 1–4 hours | ⭐⭐ Easy | Best efficiency-quality balance |
| 🎯 **LoRA 16-bit Fine-Tune** | ≥ 24 GB VRAM | 2–8 hours | ⭐⭐ Easy | Maximum training precision |
| 📦 **Import GGUF** | ❌ None | < 5 min | ⭐ Beginner | Bring models from Colab/cloud |

#### Smart Hardware Detection

The system scans your machine and tells you exactly what you can do.

![Hardware Detection](screenshots/2.png)

- Auto-detects **GPU model, VRAM, system RAM, disk space, CUDA version**
- Shows recommended approaches based on your hardware
- Custom storage paths — avoid filling your C: drive
- File structure browser for your training data directory

#### One-Click Environment Setup

No more fighting with PyTorch + CUDA version mismatches:

- Detects your system CUDA version automatically (11.7 / 11.8 / 12.1 / 12.4 / 12.6)
- Installs the matching PyTorch GPU build with one click
- Supports **system Python, conda environments, and virtualenvs**
- Dependency checker with clear missing-package indicators

#### Curated Base Model Library

![QLoRA Config](screenshots/4.png)

Don't know which model to fine-tune? The built-in model browser helps:

- **Filter by vendor**: Meta (LLaMA), Qwen, Google (Gemma), Mistral, Microsoft (Phi), DeepSeek
- **Filter by size**: 0.5B / 1B / 3B / 7B / 8B / 14B / 70B
- **VRAM requirement tags**: see at a glance which models fit your GPU (≈6GB / ≈8GB / ≈16GB / ≈48GB)
- **Free/Gated badges**: know if you need a HuggingFace access token
- Or type any HuggingFace model ID directly

#### Powerful Dataset Management

![Dataset Management](screenshots/5.png)

- **Upload** JSONL, JSON, or CSV files — auto-detect format and row count
- **Download from HuggingFace** — paste any dataset ID, auto-converts to training format
- **Format auto-detection**: Alpaca (`instruction/input/output`), ShareGPT (`conversations`), OpenAI (`messages`)
- **Live preview** — see your data structure and sample rows before training
- **Format examples** — built-in templates showing correct data format for each type

#### Full Hyperparameter Control

Every knob you need, with sensible defaults:

- **LoRA Rank (r)** & **LoRA Alpha** — control adapter capacity
- **Epochs** / **Batch Size** / **Learning Rate** / **Max Sequence Length**
- **Quantization format**: Q4_K_M / Q5_K_M / Q8_0 (for Ollama export)
- **Auto-register to Ollama**: trained model immediately available for chat

#### Real-Time Training Monitor

![Training Log](screenshots/21.jpg)

- Live progress bar with percentage and ETA
- Current loss value updated in real-time
- Full training log with step details (step/total, time, speed)
- **Stop button** — safely interrupt training at any time
- Background training — **keep chatting while your model trains**

#### Complete Training History

![Training History](screenshots/6.png)

Every training run is recorded with full details:

- Base model, method (QLoRA/LoRA), dataset, training duration
- Final loss, total steps, all hyperparameters
- LoRA r/α, sequence length, Ollama registration status (✅/❌)
- **Resume training** from any checkpoint
- Copy output path for manual operations

#### 📊 Real Results: Before vs After Fine-Tuning

Fine-tuning a **Qwen 0.5B** model (only 500M parameters!) with a code dataset:

| ❌ Before Fine-Tuning | ✅ After Fine-Tuning |
|:---:|:---:|
| ![Before](screenshots/16.jpg) | ![After](screenshots/17.jpg) |
| *Asked to write PSO code* | *Same question after fine-tuning* |
| Model says "I cannot generate code" and gives vague text descriptions | Correctly identifies PSO (Particle Swarm Optimization), provides **complete working Python implementation** with numpy |

> **The same tiny model, same question. Fine-tuning transforms capability.**

---

### 🏗️ Pretrain Lab — Build a Language Model from Absolute Zero

> **This is the crown jewel of OllamaForge**, and something no other Ollama UI offers.
>
> Design a Transformer architecture visually. Train a tokenizer. Prepare datasets. Train the model. Watch it learn to speak. Export to GGUF. Deploy to Ollama. **The entire pipeline, from empty weights to working chatbot, through a GUI.**

![Pretrain Lab Overview](screenshots/11.png)

#### 🧩 Visual Model Architecture Designer

> Drag and drop Transformer building blocks. See parameter counts update in real-time. No PhD required.

![Architecture Editor](screenshots/12.png)

<table>
<tr><td width="33%">

**🧱 Component Palette**

*Core Layers*
- Token Embedding
- Self-Attention
- Cross-Attention
- Feed-Forward Network (FFN)
- Linear Projection
- LM Head

*Normalization*
- Pre-Norm / Post-Norm
- Final Norm
- LayerNorm / RMSNorm

*Connections & Advanced*
- Residual Add
- Dropout / Skip Connect
- Gating / MoE Layer
- Parallel / KV Cache

</td><td width="33%">

**📐 Architecture Choices**

*Positional Encoding*
- RoPE (LLaMA/Mistral style)
- ALiBi (BLOOM style)
- Absolute (GPT-2 style)

*Activation Functions*
- SwiGLU (modern default)
- GELU / ReLU / SiLU

*Attention Types*
- Multi-Head (MHA)
- Grouped-Query (GQA)
- Multi-Query (MQA)

</td><td width="33%">

**📊 Real-Time Stats**
- Total parameter count
- Training VRAM (FP16)
- Inference VRAM
- Embedding parameters & ratio
- Attention parameters & ratio
- Head dimension
- Architecture validation ✅/❌

</td></tr>
</table>

**9 Pre-built Templates** to start from — or design your own:

| Template | Params | VRAM (FP16) | Style |
|----------|:---:|:---:|---|
| GPT-2 Small | 124.4M | ~1.57 GB | Classic OpenAI |
| GPT-2 Medium | 354.6M | ~4.46 GB | Mid-size classic |
| LLaMA Tiny | 39.6M | ~491 MB | Modern LLaMA-style |
| LLaMA Small | 109.1M | ~1.28 GB | Larger LLaMA |
| Mistral Tiny | 38.5M | ~696 MB | Sliding window attention |
| Phi Tiny | 34.8M | ~475 MB | Parallel Attention+FFN |
| Gemma Tiny | 37.9M | ~488 MB | Google Gemma-style |
| MoE Tiny | 95.8M | ~1.16 GB | Mixture of Experts |
| **Custom Minimal** | **2.1M** | **~26 MB** | **Learn in minutes** |

> 💡 The 2.1M "Custom Minimal" template trains in minutes — perfect for your first experiment!

#### 📖 Tokenizer Workshop

> The tokenizer decides how your model sees text. Choose a pretrained one or train your own.

![Tokenizer Workshop](screenshots/13.png)

**6 pretrained tokenizers ready to use:**

| Tokenizer | Vocab Size | Type | Language |
|-----------|:---:|---|:---:|
| GPT-2 | 50,257 | BPE | 🇬🇧 EN |
| LLaMA 2 | 32,000 | SentencePiece | 🇬🇧 EN |
| LLaMA 3 | 128,256 | tiktoken | 🌍 Multi |
| Qwen 2 | 151,936 | BPE | 🇨🇳🇬🇧 ZH/EN |
| Mistral | 32,000 | SentencePiece | 🇬🇧 EN |
| BERT Chinese | 21,128 | WordPiece | 🇨🇳 ZH |

- **Train a custom tokenizer** from your own corpus
- **Download any tokenizer** from HuggingFace by model ID
- **Live tokenization preview** — input text and see color-coded tokens in real-time

#### 📚 Data Preparation

> Curated datasets for education and research. Or bring your own.

![Data Preparation](screenshots/14.png)

**Recommended pretraining datasets:**

| Dataset | Size | Rows | Level | Best For |
|---------|:---:|:---:|:---:|---------|
| **TinyStories** | ~470 MB | ~2.1M | 🟢 Beginner | 1M–50M param models, first experiments |
| **WikiText-2** | ~12 MB | ~36K | 🟢 Beginner | Quick validation, minutes to train |
| **WikiText-103** | ~500 MB | ~1.8M | 🟢 Beginner | Classic language modeling benchmark |
| **Chinese Wikipedia** | ~1.5 GB | ~1M | 🟡 Intermediate | Chinese language models |
| **SlimPajama** | ~627 GB | ~600B tok | 🔴 Advanced | 100M+ param models |
| **FineWeb-Edu** | ~1.3 TB | ~1.3T tok | 🔴 Advanced | High-quality English pretraining |

- **Three ways to add data**: upload files (txt/jsonl/json/csv), paste text directly, download from HuggingFace
- Auto tokenize and pack into training format
- Built-in data processing pipeline

#### 📈 Training Configuration & Monitoring

> Full control over the training loop, with a live dashboard to watch it converge.

![Training Dashboard](screenshots/20.jpg)

**Training configuration with every knob exposed:**

![Training Config](screenshots/15.png)

| Parameter | Options |
|-----------|---------|
| Batch Size | Any positive integer |
| Total Steps | Configurable (e.g., 5000, 15000) |
| Warmup Steps | Linear warmup period |
| Weight Decay | Regularization strength |
| Gradient Clipping | Prevent exploding gradients |
| LR Scheduler | **Cosine** / Linear / Constant |
| Save Interval | Checkpoint every N steps |
| Sample Interval | Auto-generate text every N steps |
| Validation Interval | Evaluate on held-out data |
| Precision | **FP16 mixed precision** ✅ |
| Multi-GPU | **DDP distributed training** ✅ |

**Live monitoring dashboard:**
- 📊 Step counter with total progress
- 📉 Real-time loss curve visualization
- 📖 Learning rate tracking
- ⚡ Training speed (tokens/sec)
- 🖥️ GPU device information
- 🎯 Auto-generated text samples at configurable intervals

#### 🎨 Watch Your Model Learn to Speak

> The most magical part: your model starts from **random noise** and gradually learns language.

A **39.6M parameter** LLaMA Tiny architecture, pretrained from scratch on Chinese classical literature:

<table>
<tr>
<td align="center" width="50%">

**Trained on the Four Great Classical Novels (四大名著)**

![Novel Generation](screenshots/18.jpg)

Given the prompt "林黛玉道" (Lin Daiyu said), the model generates fluent **Dream of the Red Chamber** style dialogue — with character voices, classical vernacular Chinese, and period-appropriate expressions.

</td>
<td align="center" width="50%">

**Trained on Classical Chinese Poetry (古诗词)**

![Poetry Generation](screenshots/19.jpg)

At step 8800, the model generates structured **classical Chinese poetry** with proper rhythm and imagery — "举头望明月，一望几山空" (Raising my head to gaze at the bright moon, gazing far over empty mountains).

</td>
</tr>
</table>

> 🏮 **From random weights to literature in hours** — a tiny 39.6M model, trained entirely through this GUI, with zero command-line interaction.

---

### 🔨 Model Workshop — Complete Model Lifecycle Management

> Manage, import, quantize, create variants, and test — all your local models in one place.

#### 📋 Model Management

![Model Management](screenshots/7.png)

- View all installed Ollama models with size, age, and actions
- **Copy** model to create variants
- **Export** Modelfile for backup or sharing
- **Delete** unused models to free disk space
- Supports both local models and cloud-proxied models

#### 🌐 HuggingFace Import

> Any HuggingFace model → quantized → registered to Ollama. Three fields and one click.

![HF Import](screenshots/8.png)

- Input any **HuggingFace model ID** (e.g., `Qwen/Qwen2.5-7B-Instruct`)
- Choose your **Ollama model name**
- Select **quantization precision**:

| Precision | Description |
|:---:|---|
| **Q4_K_M** | Recommended — small size, great quality |
| Q5_K_M | Balanced — slightly larger, slightly better |
| Q8_0 | Full quality — largest but best |
| Q3_K_M | Extreme compression — for tight VRAM |
| F16 | Lossless — for later re-quantization |
| Q4_0 | Classic 4-bit — simple and fast |

#### ⚡ Quantization Conversion

> Already have a high-precision model? Convert it to save VRAM and boost speed.

![Quantization](screenshots/9.png)

Choose from the visual comparison table:

| Quant Type | Size (7B) | Quality | Speed | Recommended For |
|:---:|:---:|:---:|:---:|---|
| **Q4_K_M** | ~4.1 GB | ★★★★☆ | ★★★★★ | 🏆 Daily use — best overall |
| Q5_K_M | ~4.8 GB | ★★★★½ | ★★★★☆ | When you have extra VRAM |
| Q8_0 | ~7.2 GB | ★★★★★ | ★★★☆☆ | Maximum quality |
| Q3_K_M | ~3.3 GB | ★★★☆☆ | ★★★★★ | VRAM-constrained setups |
| F16 | ~13.5 GB | ★★★★★ | ★★☆☆☆ | Lossless storage / re-quant |

---

### 🔑 API Sharing Center — Your Models as a Service

> Turn your local Ollama into an **OpenAI-compatible API server** and share models with your team, apps, or scripts.

![API Sharing](screenshots/10.png)

<table>
<tr><td width="50%">

**Key Management**
- Create API keys with custom names
- **Rate limiting**: requests per minute
- **Daily quotas**: max calls per day
- **Expiration**: auto-expire after N days
- **Model restrictions**: limit which models each key can access
- One-click revoke compromised keys

</td><td width="50%">

**Dashboard & Integration**
- Active keys count
- Today's call volume
- Total cumulative usage
- Available model count
- Ready-to-copy **cURL** examples
- Ready-to-copy **Python (OpenAI SDK)** examples

</td></tr>
</table>

**Drop-in replacement for OpenAI API:**

```python
from openai import OpenAI

# Just change base_url and api_key — your code stays the same
client = OpenAI(
    base_url="http://localhost:8751/v1",
    api_key="ogk-your-api-key"
)

response = client.chat.completions.create(
    model="qwen3:4b",
    messages=[{"role": "user", "content": "Explain quantum computing"}]
)
print(response.choices[0].message.content)
```

```bash
# cURL works too
curl http://localhost:8751/v1/chat/completions \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer ogk-your-api-key" \
  -d '{"model":"qwen3:4b","messages":[{"role":"user","content":"Hello!"}]}'
```

**Security:**
- 🏠 **Localhost auto-bypass** — no auth needed on your own machine
- 🔐 **LAN requires admin token** — generated on first launch
- 🔑 **Per-key permissions** — granular model access control

---

## 🚀 Quick Start / 快速开始

### Prerequisites / 前置要求

- **Python 3.10+**
- **[Ollama](https://ollama.com)** installed and running (`ollama serve`)

### 3 Commands to Launch / 三行命令启动

```bash
git clone https://github.com/zhengxuanjiang/ollama-forge.git
cd ollama-forge
python run.py
```

> Dependencies auto-install on first run. Browser opens at `http://localhost:8751` 🎉

### Fine-Tuning Setup (Optional) / 微调环境（可选）

**Option A: One-Click** — open Fine-Tune Center → click "一键安装"

**Option B: Manual**

```bash
conda create -n ollama-forge python=3.11 -y && conda activate ollama-forge

# PyTorch GPU (check CUDA: nvidia-smi)
pip install torch==2.4.0 --index-url https://download.pytorch.org/whl/cu121

pip install -r requirements-finetune.txt
```

### Custom Storage / 自定义存储路径

```bash
# Windows PowerShell
$env:OLLAMA_GUI_FT_DIR = "D:\ollama-forge-data"

# Linux / macOS
export OLLAMA_GUI_FT_DIR=/data/ollama-forge
```

Or set it directly in the UI → Hardware Detection → Storage Path Settings.

---

## 📐 Project Structure

```
ollama-forge/
├── run.py                      # One-command launcher (auto-installs deps)
├── config.json                 # Persistent config (data dirs, HF cache)
├── requirements.txt            # Core: FastAPI, httpx, uvicorn
├── requirements-finetune.txt   # Training: PyTorch, PEFT, TRL, bitsandbytes
│
├── backend/
│   ├── app.py                  # Main server (2600+ lines)
│   │                           #   Chat proxy, fine-tune orchestration,
│   │                           #   model workshop, API sharing, hardware detect
│   └── pretrain/               # Pretrain Lab engine
│       ├── architect.py        #   Architecture templates & validation
│       ├── tokenizer_builder.py#   Tokenizer training & download
│       ├── data_manager.py     #   Dataset processing pipeline
│       ├── trainer.py          #   Training loop, process mgmt, monitoring
│       ├── streaming.py        #   Real-time training data WebSocket stream
│       ├── inference.py        #   Text generation from trained models
│       ├── exporter.py         #   GGUF export & Ollama registration
│       └── routes.py           #   FastAPI routes for pretrain lab
│
└── frontend/
    ├── index.html              # Main HTML (1200 lines of UI structure)
    ├── app.js                  # Chat interface & core logic
    ├── pretrain-lab.js         # Pretrain Lab interface (3000 lines)
    └── styles.css              # Dark theme with amber/gold accents
```

**~15,800 lines of code** · Zero framework dependencies on frontend · Pure Python backend

---

## 🛠️ Tech Stack

| Layer | Technology | Why |
|-------|-----------|-----|
| Backend | Python · FastAPI · Uvicorn | Async, fast, modern |
| HTTP Client | httpx | Async Ollama API proxy |
| Frontend | Vanilla JavaScript | Zero deps, instant load |
| Fine-Tuning | HuggingFace PEFT + TRL | Standard, stable, Windows-compatible |
| Quantization | llama.cpp (GGUF) | Industry standard |
| Code Highlight | highlight.js | Beautiful syntax coloring |
| Math | KaTeX | Fast LaTeX rendering |
| Styling | Custom CSS | Dark theme, amber accents |

> **Why no Unsloth?** We chose standard HuggingFace PEFT + TRL for maximum compatibility. No triton/xformers headaches, full Windows support, fewer dependencies, fewer crashes.

---

## 🗺️ Roadmap

- [ ] 🌐 English UI localization (currently Chinese, but code & docs are bilingual)
- [ ] 📚 RAG (Retrieval-Augmented Generation)
- [ ] 📊 Model evaluation benchmarks (MMLU, C-Eval, etc.)
- [ ] 🐳 Docker one-click deployment
- [ ] 🧩 Plugin/extension system
- [ ] 👥 Multi-user collaboration
- [ ] 📈 Cross-run training comparison dashboard
- [ ] 🎙️ Voice input/output integration

---

## 🤝 Contributing

Every contribution makes OllamaForge better — bug fixes, features, translations, docs, or just ideas.

```bash
# Fork → Branch → Code → PR
git checkout -b feature/your-feature
git commit -m "Add your feature"
git push origin feature/your-feature
# Open a Pull Request on GitHub
```

---

## 📄 License

[MIT License](LICENSE) — use it freely for personal and commercial projects.

---

<br>
<br>

---

<br>
<br>

# 🇨🇳 中文

## 📊 功能一览

| | 普通聊天界面 | **OllamaForge** |
|---|:---:|:---:|
| 💬 多轮对话 & 历史记录 | ✅ | ✅ |
| 🧠 思考模式（思维链展开） | 少见 | ✅ |
| 🎨 代码高亮 + LaTeX + 图片理解 | 部分 | ✅ |
| ⚡ GPU / CPU / 混合推理切换 | ❌ | ✅ |
| 🔧 QLoRA / LoRA 微调 | ❌ | ✅ |
| 🏗️ 从零预训练模型 | ❌ | ✅ |
| 🧩 拖拽式架构设计器 | ❌ | ✅ |
| 📖 自定义 Tokenizer 训练 | ❌ | ✅ |
| ⚡ HuggingFace 导入 + 量化 | ❌ | ✅ |
| 🔑 OpenAI 兼容 API & 密钥管理 | ❌ | ✅ |
| 📈 实时训练面板 + Loss 曲线 | ❌ | ✅ |
| 🚀 一键部署到 Ollama | ❌ | ✅ |

---

## 🎯 功能详解

### 💬 聊天界面 — 优雅、高效、功能完整

> 不是又一个聊天窗口，而是为深度用户打造的完整对话环境。

![聊天界面](screenshots/1.png)

<table>
<tr><td width="50%">

**对话与生成**
- 侧边栏多会话管理与搜索
- 流式响应，实时统计（tok/s、token 数、耗时）
- 思考模式 — 展开查看模型推理链
- 系统提示词预设：助手 / 编程 / 翻译 / 写作 / 分析
- 图片上传支持视觉模型（LLaVA、Qwen-VL 等）

</td><td width="50%">

**模型与推理控制**
- 设备一键切换：自动 / GPU / CPU / 混合
- Keep-Alive：即时 / 5分 / 30分 / 1时 / 永久
- 完整参数面板：Temperature、Top P、重复惩罚、上下文长度（512–128K）、种子
- 运行模型面板：查看显存占用、运行时间、一键卸载
- 代码高亮 (highlight.js) + LaTeX 公式 (KaTeX)

</td></tr>
</table>

---

### 🔧 微调中心 — 从基座模型到领域专家，全程无代码

> **上传数据 → 选模型 → 点训练。就这么简单。**
> 微调完成后自动注册到 Ollama，立即可以对话。

![微调方式](screenshots/3.png)

#### 四种方式，适配各种需求

| 方式 | GPU 要求 | 耗时 | 难度 | 适用场景 |
|------|:---:|:---:|:---:|---------|
| 📝 **Modelfile 定制** | ❌ 无需 | < 1 分钟 | ⭐ 入门 | 提示词工程、few-shot |
| 🚀 **QLoRA 4-bit 微调** | ≥ 8 GB 显存 | 1–4 小时 | ⭐⭐ 简单 | 效率与质量的最佳平衡 |
| 🎯 **LoRA 16-bit 微调** | ≥ 24 GB 显存 | 2–8 小时 | ⭐⭐ 简单 | 最高训练精度 |
| 📦 **导入 GGUF** | ❌ 无需 | < 5 分钟 | ⭐ 入门 | 导入 Colab/云端训好的模型 |

#### 智能硬件检测

系统自动扫描你的硬件，告诉你能做什么。

![硬件检测](screenshots/2.png)

- 自动检测 **GPU 型号、显存、系统内存、磁盘空间、CUDA 版本**
- 根据硬件推荐合适的微调方案
- 自定义存储路径 — 避免占满 C 盘
- 文件结构浏览器

#### 一键环境安装

再也不用和 PyTorch + CUDA 版本不匹配作斗争：

- 自动检测系统 CUDA 版本（11.7 / 11.8 / 12.1 / 12.4 / 12.6）
- 一键安装匹配的 PyTorch GPU 版
- 支持**系统 Python、conda 环境、virtualenv**
- 依赖检查器，清晰显示缺少的包

#### 精选基座模型库

![QLoRA 配置](screenshots/4.png)

不知道微调哪个模型？内置模型浏览器帮你选：

- **按厂商筛选**：Meta (LLaMA)、Qwen、Google (Gemma)、Mistral、Microsoft (Phi)、DeepSeek
- **按大小筛选**：0.5B / 1B / 3B / 7B / 8B / 14B / 70B
- **显存需求标签**：一眼看出哪些模型适合你的 GPU（≈6GB / ≈8GB / ≈16GB / ≈48GB）
- **免费/需申请标识**：知道是否需要 HuggingFace 访问令牌
- 也可直接输入任意 HuggingFace 模型 ID

#### 强大的数据集管理

![数据集管理](screenshots/5.png)

- **上传** JSONL/JSON/CSV — 自动识别格式和条目数
- **从 HuggingFace 下载** — 粘贴数据集 ID，自动转换为训练格式
- **格式自动检测**：Alpaca（`instruction/input/output`）、ShareGPT（`conversations`）、OpenAI（`messages`）
- **实时预览** — 训练前查看数据结构和样本
- **格式示例** — 内置模板展示各种格式的正确写法

#### 完整超参数控制

所有旋钮都暴露出来，带合理默认值：

- **LoRA Rank (r)** & **LoRA Alpha** — 控制适配器容量
- **Epochs** / **Batch Size** / **学习率** / **最大序列长度**
- **量化格式**：Q4_K_M / Q5_K_M / Q8_0（用于 Ollama 导出）
- **自动注册 Ollama**：训练完立即可用

#### 实时训练监控

![训练日志](screenshots/21.jpg)

- 实时进度条，显示百分比和预计剩余时间
- Loss 值实时更新
- 完整训练日志，包含步骤详情（step/total、时间、速度）
- **停止按钮** — 随时安全中断训练
- 后台训练 — **边训练边聊天**

#### 完整训练历史

![历史记录](screenshots/6.png)

每次训练都有完整记录：

- 基座模型、方式（QLoRA/LoRA）、数据集、训练时长
- 最终 Loss、总步数、所有超参数
- LoRA r/α、序列长度、Ollama 注册状态（✅/❌）
- **断点续训** — 从任意 Checkpoint 恢复
- 复制输出路径，方便手动操作

#### 📊 真实效果：微调前后对比

使用代码数据集微调 **Qwen 0.5B**（仅 5 亿参数！）：

| ❌ 微调前 | ✅ 微调后 |
|:---:|:---:|
| ![微调前](screenshots/16.jpg) | ![微调后](screenshots/17.jpg) |
| *要求写 PSO 代码* | *同样的问题，微调后* |
| 模型说"我无法生成或创建代码"，只给出模糊的文字描述 | 正确识别 PSO（粒子群优化），提供**完整可运行的 Python 实现** |

> **同一个小模型，同一个问题。微调改变一切。**

---

### 🏗️ 训练实验室 — 从绝对零开始打造你的语言模型

> **OllamaForge 的王牌功能**，也是其他 Ollama 界面都没有的。
>
> 可视化设计 Transformer 架构 → 训练 Tokenizer → 准备数据集 → 训练模型 → 看它学会说话 → 导出 GGUF → 部署到 Ollama。**从空白权重到可用聊天机器人的完整流程，全部通过 GUI 完成。**

![训练实验室全览](screenshots/11.png)

#### 🧩 可视化模型架构设计器

> 拖拽 Transformer 构建模块，实时查看参数量变化。不需要博士学位。

![架构编辑器](screenshots/12.png)

<table>
<tr><td width="33%">

**🧱 组件面板**

*核心层*
- Token Embedding
- Self-Attention（自注意力）
- Cross-Attention（交叉注意力）
- FFN（前馈网络）
- Linear（线性投影）
- LM Head（语言模型头）

*归一化*
- Pre-Norm / Post-Norm
- Final Norm
- LayerNorm / RMSNorm

*连接与高级*
- Residual Add（残差连接）
- Dropout / Skip Connect
- Gating / MoE Layer
- Parallel / KV Cache

</td><td width="33%">

**📐 架构选择**

*位置编码*
- RoPE（LLaMA/Mistral 风格）
- ALiBi（BLOOM 风格）
- 绝对位置编码（GPT-2 风格）

*激活函数*
- SwiGLU（现代默认）
- GELU / ReLU / SiLU

*注意力类型*
- Multi-Head (MHA)
- Grouped-Query (GQA)
- Multi-Query (MQA)

</td><td width="33%">

**📊 实时统计**
- 总参数量
- 训练显存（FP16）
- 推理显存
- Embedding 参数量与占比
- 注意力参数量与占比
- Head 维度
- 架构验证 ✅/❌

</td></tr>
</table>

**9 种预设模板** — 也可以从零设计：

| 模板 | 参数量 | 显存 (FP16) | 风格 |
|------|:---:|:---:|------|
| GPT-2 Small | 124.4M | ~1.57 GB | 经典 OpenAI |
| GPT-2 Medium | 354.6M | ~4.46 GB | 中等经典 |
| LLaMA Tiny | 39.6M | ~491 MB | 现代 LLaMA 风格 |
| LLaMA Small | 109.1M | ~1.28 GB | 较大 LLaMA |
| Mistral Tiny | 38.5M | ~696 MB | 滑动窗口注意力 |
| Phi Tiny | 34.8M | ~475 MB | 并行 Attention+FFN |
| Gemma Tiny | 37.9M | ~488 MB | Google Gemma 风格 |
| MoE Tiny | 95.8M | ~1.16 GB | 混合专家 |
| **自定义极简** | **2.1M** | **~26 MB** | **几分钟训完** |

> 💡 2.1M 的"极简入门"模板几分钟就能训完 — 非常适合你的第一次实验！

#### 📖 词表构建

> Tokenizer 决定了你的模型如何看待文本。选择现成的或训练自己的。

![词表构建](screenshots/13.png)

**6 种预训练 Tokenizer 可直接使用：**

| Tokenizer | 词表大小 | 类型 | 语言 |
|-----------|:---:|------|:---:|
| GPT-2 | 50,257 | BPE | 🇬🇧 英文 |
| LLaMA 2 | 32,000 | SentencePiece | 🇬🇧 英文 |
| LLaMA 3 | 128,256 | tiktoken | 🌍 多语言 |
| Qwen 2 | 151,936 | BPE | 🇨🇳🇬🇧 中英 |
| Mistral | 32,000 | SentencePiece | 🇬🇧 英文 |
| BERT 中文 | 21,128 | WordPiece | 🇨🇳 中文 |

- **训练自定义 Tokenizer** — 使用你自己的语料
- **下载任意 Tokenizer** — 输入 HuggingFace 模型 ID
- **实时分词预览** — 输入文本，查看不同颜色标注的 token

#### 📚 数据准备

> 精选教育和研究用数据集，也可以用自己的数据。

![数据准备](screenshots/14.png)

**推荐预训练数据集：**

| 数据集 | 大小 | 条目数 | 级别 | 适合场景 |
|--------|:---:|:---:|:---:|---------|
| **TinyStories** | ~470 MB | ~2.1M | 🟢 入门 | 1M–50M 参数模型，首次实验 |
| **WikiText-2** | ~12 MB | ~36K | 🟢 入门 | 快速验证，几分钟完成 |
| **WikiText-103** | ~500 MB | ~1.8M | 🟢 入门 | 经典语言模型训练 |
| **中文维基百科** | ~1.5 GB | ~1M | 🟡 中等 | 中文模型训练 |
| **SlimPajama** | ~627 GB | ~600B tok | 🔴 高级 | 100M+ 参数模型 |
| **FineWeb-Edu** | ~1.3 TB | ~1.3T tok | 🔴 高级 | 高质量英文预训练 |

- **三种数据添加方式**：上传文件（txt/jsonl/json/csv）、直接粘贴文本、从 HuggingFace 下载
- 自动分词打包为训练格式
- 内置数据预处理管线

#### 📈 训练配置与监控

> 训练循环的完整控制权，加上实时 Loss 曲线。

![训练面板](screenshots/20.jpg)

**每个参数都可配置：**

![训练配置](screenshots/15.png)

| 参数 | 选项 |
|------|------|
| Batch Size | 任意正整数 |
| 总步数 | 可配置（如 5000、15000） |
| Warmup 步数 | 线性预热 |
| 权重衰减 | 正则化强度 |
| 梯度裁剪 | 防止梯度爆炸 |
| 学习率调度 | **Cosine** / Linear / Constant |
| 保存间隔 | 每 N 步保存 Checkpoint |
| 样本间隔 | 每 N 步自动生成文本 |
| 验证间隔 | 在验证集上评估 |
| 精度 | **FP16 混合精度** ✅ |
| 多卡 | **DDP 分布式训练** ✅ |

**实时监控面板：**
- 📊 步数进度条
- 📉 实时 Loss 曲线可视化
- 📖 学习率追踪
- ⚡ 训练速度（tokens/sec）
- 🖥️ GPU 设备信息
- 🎯 可配置间隔的自动文本生成样本

#### 🎨 看你的模型学会说话

> 最神奇的部分：你的模型从**随机噪声**开始，逐渐学会语言。

**39.6M 参数** LLaMA Tiny 架构，使用中国古典文学从零预训练：

<table>
<tr>
<td align="center" width="50%">

**四大名著训练**

![小说生成](screenshots/18.jpg)

输入提示词"林黛玉道"，模型生成流畅的**《红楼梦》风格对话** — 人物声口、古典白话文、时代特征一应俱全。

</td>
<td align="center" width="50%">

**古诗词训练**

![诗词生成](screenshots/19.jpg)

在第 8800 步，模型生成了结构工整的**古诗词** — "举头望明月，一望几山空"，意象到位、韵律和谐。

</td>
</tr>
</table>

> 🏮 **从随机权重到古典文学，仅需数小时** — 一个 3960 万参数的小模型，完全通过本 GUI 从零训练，零命令行操作。

---

### 🔨 模型工坊 — 模型全生命周期管理

> 管理、导入、量化、创建变体、测试 — 所有本地模型一站搞定。

#### 📋 模型管理

![模型管理](screenshots/7.png)

- 查看所有已安装 Ollama 模型，显示大小、时间
- **复制**模型创建变体
- **导出** Modelfile 备份或分享
- **删除**不用的模型释放磁盘
- 支持本地模型和云端代理模型

#### 🌐 HuggingFace 导入

> 任意 HuggingFace 模型 → 量化 → 注册到 Ollama。三个字段一键完成。

![HF 导入](screenshots/8.png)

- 输入任意 **HuggingFace 模型 ID**（如 `Qwen/Qwen2.5-7B-Instruct`）
- 选择 **Ollama 模型名**
- 选择**量化精度**：Q4_K_M（推荐）/ Q5_K_M（平衡）/ Q8_0（全质量）/ Q3_K_M（极限压缩）/ F16（无损）/ Q4_0（经典）

#### ⚡ 量化转换

> 已有高精度模型？转换为低精度，省显存、加速度。

![量化转换](screenshots/9.png)

| 量化类型 | 体积 (7B) | 质量 | 速度 | 推荐场景 |
|:---:|:---:|:---:|:---:|---------|
| **Q4_K_M** | ~4.1 GB | ★★★★☆ | ★★★★★ | 🏆 日常使用首选 |
| Q5_K_M | ~4.8 GB | ★★★★½ | ★★★★☆ | 显存充足时推荐 |
| Q8_0 | ~7.2 GB | ★★★★★ | ★★★☆☆ | 追求最佳质量 |
| Q3_K_M | ~3.3 GB | ★★★☆☆ | ★★★★★ | 显存紧张 |
| F16 | ~13.5 GB | ★★★★★ | ★★☆☆☆ | 无损 / 后续再量化 |

---

### 🔑 API 共享中心 — 你的模型即服务

> 把本地 Ollama 变成 **OpenAI 兼容 API 服务器**，共享给团队、应用或脚本。

![API 共享](screenshots/10.png)

<table>
<tr><td width="50%">

**密钥管理**
- 创建自定义名称的 API 密钥
- **速率限制**：每分钟请求数
- **每日配额**：每天最大调用数
- **过期时间**：N 天后自动失效
- **模型限制**：指定每个密钥可用的模型
- 一键吊销被泄露的密钥

</td><td width="50%">

**仪表盘与集成**
- 活跃密钥数量
- 今日调用量
- 累计使用量
- 可用模型数
- 即拿即用的 **cURL** 示例
- 即拿即用的 **Python (OpenAI SDK)** 示例

</td></tr>
</table>

**直接替换 OpenAI API，你的代码一行不改：**

```python
from openai import OpenAI

client = OpenAI(
    base_url="http://localhost:8751/v1",
    api_key="ogk-你的密钥"
)

r = client.chat.completions.create(
    model="qwen3:4b",
    messages=[{"role": "user", "content": "解释量子计算"}]
)
print(r.choices[0].message.content)
```

**安全机制：**
- 🏠 **本机免认证** — localhost 自动跳过鉴权
- 🔐 **局域网需 Token** — 首次启动时自动生成
- 🔑 **按密钥授权** — 精细的模型访问控制

---

## 📐 项目结构

```
ollama-forge/
├── run.py                      # 一键启动（自动安装依赖）
├── config.json                 # 持久化配置（数据目录、HF 缓存）
├── requirements.txt            # 核心依赖：FastAPI, httpx, uvicorn
├── requirements-finetune.txt   # 训练依赖：PyTorch, PEFT, TRL, bitsandbytes
│
├── backend/
│   ├── app.py                  # 主服务（2600+ 行）
│   │                           #   聊天代理、微调编排、模型工坊、API 共享、硬件检测
│   └── pretrain/               # 训练实验室引擎
│       ├── architect.py        #   架构模板与验证
│       ├── tokenizer_builder.py#   Tokenizer 训练与下载
│       ├── data_manager.py     #   数据集处理管线
│       ├── trainer.py          #   训练循环、进程管理、监控
│       ├── streaming.py        #   实时训练数据流
│       ├── inference.py        #   文本生成推理
│       ├── exporter.py         #   GGUF 导出与 Ollama 注册
│       └── routes.py           #   训练实验室 API 路由
│
└── frontend/
    ├── index.html              # 主 HTML（1200 行 UI 结构）
    ├── app.js                  # 聊天界面与核心逻辑
    ├── pretrain-lab.js         # 训练实验室界面（3000 行）
    └── styles.css              # 暗色主题 + 琥珀色点缀
```

**约 15,800 行代码** · 前端零框架依赖 · 纯 Python 后端

---

## 🛠️ 技术栈

| 层级 | 技术 | 理由 |
|------|------|------|
| 后端 | Python · FastAPI · Uvicorn | 异步、高性能、现代 |
| HTTP 客户端 | httpx | 异步代理 Ollama API |
| 前端 | 原生 JavaScript | 零依赖、秒加载 |
| 微调 | HuggingFace PEFT + TRL | 标准方案、稳定、Windows 兼容 |
| 量化 | llama.cpp (GGUF) | 业界标准 |
| 代码高亮 | highlight.js | 美观的语法着色 |
| 公式 | KaTeX | 快速 LaTeX 渲染 |
| 样式 | 自定义 CSS | 暗色主题、琥珀色调 |

> **为什么不用 Unsloth？** 我们选择标准 HuggingFace PEFT + TRL 以获得最大兼容性。无需 triton/xformers，完整 Windows 支持，依赖更少，崩溃更少。

---

## 🗺️ 路线图

- [ ] 🌐 英文界面国际化（目前界面为中文，代码和文档双语）
- [ ] 📚 RAG 检索增强生成
- [ ] 📊 模型评测基准（MMLU、C-Eval 等）
- [ ] 🐳 Docker 一键部署
- [ ] 🧩 插件/扩展系统
- [ ] 👥 多用户协作
- [ ] 📈 跨训练 Loss 对比面板
- [ ] 🎙️ 语音输入/输出

---

## 🤝 贡献

每一份贡献都让 OllamaForge 更好 — Bug 修复、新功能、翻译、文档、或者只是想法。

```bash
Fork → git checkout -b feature/xxx → commit → push → Pull Request
```

---

## 📄 许可证

[MIT License](LICENSE) — 个人和商业项目均可自由使用。

---

<div align="center">

<br>

**Built with ❤️ for the local LLM community**

🦙 *Your models. Your data. Your machine. No cloud required.*

🦙 *你的模型，你的数据，你的机器。无需云端。*

<br>

**⭐ 如果觉得有用，请给个 Star！/ Star this repo if you find it useful! ⭐**

<br>

<!-- [![Star History Chart](https://api.star-history.com/svg?repos=zhengxuanjiang/ollama-forge&type=Date)](https://star-history.com/#zhengxuanjiang/ollama-forge&Date) -->

</div>
