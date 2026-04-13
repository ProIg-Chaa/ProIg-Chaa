# SHUO GU

<div align="center">

### ProIg-Chaa

**Software Engineering Student | LLM Systems | Quantization | CUDA**

<a href="#-中文">中文</a> · <a href="#-english">English</a>

</div>

---

## 中文

<div align="center">

### 把大模型系统做得更高效，也更容易理解

</div>

你好，我是 **SHUO GU**，GitHub 用户名是 **ProIg-Chaa**。  
目前是华南理工大学软件工程专业学生，主要在做和学习这些方向：

<div align="center">

`LLM Inference` `KV Cache` `Prefix Reuse` `Quantization` `CUDA` `PyTorch`

</div>

### 我在关注什么

- 大语言模型推理优化与轻量 serving 系统
- Prefix Cache / KV Cache 复用机制
- 模型量化、压缩与性能基准测试
- CUDA 算子实现与底层工程实践

我比较喜欢把论文里的思路一步一步落到工程实现里，做成可以复现实验、可观察、可继续扩展的小系统，而不是只停留在想法层面。

### 代表项目

#### [nano-radix-vllm](https://github.com/ProIg-Chaa/nano-radix-vllm)

一个从 `nano-vllm` 演进出来的独立项目，目标是在保持轻量推理框架可理解性的同时，逐步接入 SGLang 风格的 radix / prefix reuse 能力。  
它更强调“渐进式系统演化”，而不是一次性照搬完整实现。

**你可以从这里看到我在做什么：**
- 逐阶段推进 radix / prefix cache 能力演化
- 加入 prefix-aware scheduling 和 tree-based prefix cache
- 支持比原始 `nano-vllm` 更细粒度的 partial-tail reuse

#### [llm-quant-benchmark](https://github.com/ProIg-Chaa/llm-quant-benchmark)

一个本地大模型量化 benchmark 项目，用统一流程对比 `FP16`、`INT8`、`INT4`、`AWQ`、`GPTQ` 等方案的效果。

**项目侧重点：**
- 统一 benchmark pipeline 和输出 schema
- 对比 TTFT、总延迟、吞吐和显存占用
- 强调结果可复现、方便后续扩展

#### [cuda-oplib](https://github.com/ProIg-Chaa/cuda-oplib)

一个用于构建、测试和 benchmark 自定义 CUDA operator 的基础脚手架，为后续 kernel 实验和 PyTorch 绑定预留了清晰结构。

**项目侧重点：**
- 面向长期扩展的工程目录设计
- 包含 tests、benchmarks、examples、bindings
- 作为后续 CUDA kernel 学习和沉淀的基础工程

#### [turboquant-pytorch-learning](https://github.com/ProIg-Chaa/turboquant-pytorch-learning)

一个围绕 TurboQuant 的学习与工程化整理项目，重点在于把压缩 KV Cache 的能力整理成更容易接入 HuggingFace `generate()` 的接口。

**项目侧重点：**
- 从脚本实现整理成更清晰的接口层
- 支持 HuggingFace 风格生成流程接入
- 更偏重“理解 + 工程可用性”

### 技术栈

<div align="center">

`Python` `PyTorch` `CUDA` `C++` `CMake` `Transformers` `LLM Serving` `Quantization`

</div>

### 现在的目标

- 继续深入高效 LLM 推理系统
- 做更多 KV Cache / Prefix Reuse 相关实验
- 补强 CUDA kernel 和底层系统能力
- 把已有项目逐渐整理成更完整的工程作品

### 联系方式

- GitHub: [@ProIg-Chaa](https://github.com/ProIg-Chaa)

---

## English

<div align="center">

### Making LLM systems more efficient and easier to understand

</div>

Hi, I'm **SHUO GU**, and my GitHub handle is **ProIg-Chaa**.  
I am a Software Engineering student at South China University of Technology, currently working on and learning about:

<div align="center">

`LLM Inference` `KV Cache` `Prefix Reuse` `Quantization` `CUDA` `PyTorch`

</div>

### What I care about

- LLM inference optimization and lightweight serving systems
- Prefix cache and KV cache reuse
- Quantization, compression, and benchmarking
- CUDA operators and low-level systems engineering

I enjoy turning research ideas into small but understandable engineering systems that are reproducible, observable, and easy to iterate on.

### Featured Projects

#### [nano-radix-vllm](https://github.com/ProIg-Chaa/nano-radix-vllm)

An independent project evolved from `nano-vllm`, aimed at incrementally integrating SGLang-style radix and prefix reuse ideas while keeping the framework lightweight and understandable.  
It emphasizes gradual systems evolution rather than a one-shot port.

**What this project emphasizes:**
- Incremental radix and prefix cache evolution
- Prefix-aware scheduling and tree-based prefix cache management
- Finer-grained partial-tail reuse beyond the original `nano-vllm`

#### [llm-quant-benchmark](https://github.com/ProIg-Chaa/llm-quant-benchmark)

A local LLM quantization benchmark project that compares `FP16`, `INT8`, `INT4`, `AWQ`, and `GPTQ` under a unified evaluation pipeline.

**What this project emphasizes:**
- A unified benchmark pipeline and output schema
- TTFT, latency, throughput, and GPU memory comparison
- Reproducible engineering experiments

#### [cuda-oplib](https://github.com/ProIg-Chaa/cuda-oplib)

A scaffold for building, testing, and benchmarking custom CUDA operators, with a clean structure for future kernels and PyTorch bindings.

**What this project emphasizes:**
- Long-term extensible project organization
- Dedicated tests, benchmarks, examples, and bindings
- A solid base for future CUDA kernel work

#### [turboquant-pytorch-learning](https://github.com/ProIg-Chaa/turboquant-pytorch-learning)

A learning-oriented and engineering-focused TurboQuant project that makes compressed KV cache integration easier for HuggingFace-style `generate()` workflows.

**What this project emphasizes:**
- Refactoring experimental logic into cleaner APIs
- HuggingFace-style generation integration
- A balance between understanding and usability

### Tech Stack

<div align="center">

`Python` `PyTorch` `CUDA` `C++` `CMake` `Transformers` `LLM Serving` `Quantization`

</div>

### Current Focus

- Efficient LLM inference systems
- More experiments on KV cache and prefix reuse
- Stronger CUDA kernel and systems engineering skills
- Turning current projects into more polished engineering work

### Contact

- GitHub: [@ProIg-Chaa](https://github.com/ProIg-Chaa)

---

<div align="center">

`Still learning.` `Still building.` `Still curious about LLM systems.`

</div>
