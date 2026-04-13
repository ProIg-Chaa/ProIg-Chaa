## Hi there 👋
# SHUO GU / ProIg-Chaa

<p align="right">
  <a href="#-中文">中文</a> | <a href="#-english">English</a>
</p>

Software Engineering student at South China University of Technology, currently focusing on LLM inference optimization, quantization, and CUDA systems learning.

华南理工大学软件工程专业学生，当前主要关注大语言模型推理优化、模型量化与 CUDA 系统方向实践。

---

## 中文

### 关于我

你好，我是 **SHUO GU**，GitHub 用户名是 **ProIg-Chaa**。  
我目前的学习和项目重点主要围绕以下几个方向展开：

- 大语言模型推理优化
- KV Cache / Prefix Cache 复用机制
- 模型量化与性能基准测试
- CUDA 算子与底层系统工程

我比较喜欢把论文思路和工程实现结合起来，尽量把一个想法做成可以复现实验、能跑通、可继续迭代的小系统。

### 我在做什么

- 研究 prefix reuse 和 radix 风格的 KV Cache 复用思路，并尝试把它逐步接入轻量推理框架
- 搭建统一的 LLM 量化 benchmark 流程，对比不同量化方案在延迟、吞吐和显存上的表现
- 搭 CUDA 算子库脚手架，为后续 kernel、benchmark、测试和 PyTorch 绑定做准备

### 代表项目

#### [nano-vllm-radix](https://github.com/ProIg-Chaa/nano-vllm-radix)

基于轻量推理框架持续推进 prefix-aware / radix 风格 KV Cache 复用实验。  
这个项目更偏向系统实现过程中的可验证演进，而不是一次性大改动。

**亮点：**
- 按阶段推进 prefix cache 能力改造
- 强调可观测、可验证、低风险迭代
- 面向 LLM serving 场景理解缓存复用机制

#### [llm-quant-benchmark](https://github.com/ProIg-Chaa/llm-quant-benchmark)

一个面向本地大模型推理的量化基准测试项目，用统一流程比较 `FP16`、`bitsandbytes INT8/INT4`、`AWQ`、`GPTQ` 等方案。

**亮点：**
- 统一 benchmark pipeline 和输出 schema
- 关注 TTFT、总延迟、吞吐和显存占用
- 强调结果可复现，而不是一次性实验脚本

#### [cuda-oplib](https://github.com/ProIg-Chaa/cuda-oplib)

一个用于构建、测试、benchmark 和后续扩展的 CUDA 算子库脚手架，适合作为后续 kernel 实验的基础工程。

**亮点：**
- 结构清晰，适合长期扩展
- 包含测试、benchmark、示例和绑定目录
- 面向后续自定义 CUDA operator 开发

#### [turboquant-pytorch-learning](https://github.com/ProIg-Chaa/turboquant-pytorch-learning)

基于 TurboQuant 的学习与工程化整理项目，重点是把压缩 KV Cache 的能力封装成更容易接入 HuggingFace 生成流程的接口。

**亮点：**
- 将压缩逻辑整理为更清晰的接口层
- 支持 HuggingFace 风格 `generate()` 接入
- 更强调工程可用性和理解过程

### 技术关键词

`Python` `PyTorch` `CUDA` `C++` `CMake` `LLM Serving` `Quantization`

### 目前关注

- 高效大模型推理系统
- Prefix Cache / KV Cache 优化
- CUDA Kernel 工程实践
- 模型压缩与部署性能分析

### 联系我

- GitHub: [@ProIg-Chaa](https://github.com/ProIg-Chaa)

---

## English

### About Me

Hi, I'm **SHUO GU**, and my GitHub handle is **ProIg-Chaa**.  
I am a Software Engineering student at South China University of Technology, currently focusing on:

- LLM inference optimization
- KV cache and prefix cache reuse
- quantization benchmarking
- CUDA operators and systems engineering

I enjoy turning research ideas into reproducible experiments and small but understandable systems that can be iterated on over time.

### What I'm Working On

- Exploring prefix reuse and radix-style KV cache management in lightweight LLM inference frameworks
- Building a unified benchmarking pipeline for local LLM quantization experiments
- Creating a reusable CUDA operator library scaffold for future kernel and systems work

### Featured Projects

#### [nano-vllm-radix](https://github.com/ProIg-Chaa/nano-vllm-radix)

A project centered on incremental integration of prefix-aware and radix-style KV cache reuse into a lightweight inference framework.

**Highlights:**
- Step-by-step evolution of prefix cache capabilities
- Focus on observability, verification, and low-risk iteration
- Practical systems understanding for LLM serving workloads

#### [llm-quant-benchmark](https://github.com/ProIg-Chaa/llm-quant-benchmark)

A reproducible benchmark project for local LLM inference, comparing `FP16`, `bitsandbytes INT8/INT4`, `AWQ`, and `GPTQ` under a unified pipeline.

**Highlights:**
- Unified benchmark pipeline and output schema
- Measures TTFT, latency, throughput, and GPU memory
- Built for reproducible engineering experiments

#### [cuda-oplib](https://github.com/ProIg-Chaa/cuda-oplib)

A CUDA operator library scaffold for building, testing, benchmarking, and later extending custom GPU kernels.

**Highlights:**
- Organized for long-term growth
- Includes tests, benchmarks, examples, and binding structure
- A solid base for future custom operator development

#### [turboquant-pytorch-learning](https://github.com/ProIg-Chaa/turboquant-pytorch-learning)

A learning-oriented and engineering-focused project around TurboQuant, with emphasis on making compressed KV cache integration easier for HuggingFace-style generation workflows.

**Highlights:**
- Refactors compression logic into clearer APIs
- Supports HuggingFace-style `generate()` integration
- Focuses on engineering usability and understanding

### Tech Stack

`Python` `PyTorch` `CUDA` `C++` `CMake` `LLM Serving` `Quantization`

### Current Interests

- Efficient LLM serving systems
- Prefix cache and KV cache optimization
- CUDA kernel engineering
- Practical model compression and deployment analysis

### Contact

- GitHub: [@ProIg-Chaa](https://github.com/ProIg-Chaa)

---

> Still learning, still building, and trying to make LLM systems more efficient and more understandable.

<!--
**ProIg-Chaa/ProIg-Chaa** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
