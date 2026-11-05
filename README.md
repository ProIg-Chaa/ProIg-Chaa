<div align="center">

#Shuo Gu (Adrian)

**Software Engineering Undergraduate @ South China University of Technology**

**MLLM Reasoning Research · LLM Inference Systems · CUDA / PyTorch**

[GitHub](https://github.com/ProIg-Chaa) · [Projects](https://github.com/ProIg-Chaa?tab=repositories) · [AI 学习笔记](https://proig-chaa.github.io/)

</div>

---

### 关于我 / About Me

我是华南理工大学软件学院 **2024 级软件工程卓越班**本科生，预计 2028 年毕业。

我主要沿两条相互关联的方向开展科研与工程实践：

- **MLLM Reasoning**：研究多模态模型在推理早期如何利用视觉信息，以及无需训练（training-free）的推理阶段干预如何影响后续决策。
- **AI Systems / LLM Inference**：关注 KV Cache 与上下文复用、prefill/decode、serving 调度、量化和 CUDA kernel，尝试将论文想法落实为可运行、可测试、可分析的系统原型。

我希望长期研究的是 **推理质量、计算成本与系统效率之间的真实权衡**。

### 🔬 科研经历 / Research

#### 1. Sparse Visual Difference Feedback (SVDF) · 多模态推理优化

**2026 · 在研 / Work in Progress** ｜ Training-free MLLM Reasoning

- 围绕多模态模型的 **early-stage reasoning**，探索如何在有限推理步骤内引入图像条件化反馈，而不更新模型权重。
- 研究原图与弱化图条件下的 next-token prediction 差异，将其构造为早期反馈信号，并在后续解码中恢复常规生成。
- 实现独立视觉分支、推理状态隔离与短时反馈注入，关注 KV 状态、随机性及模型参数冻结条件下的可复现性。
- 在多个 7B 级多模态基座与 VStar、MMVP、RealWorldQA、VisuLogic、MMK12、POPE、VMCBench 等基准上开展评估；同时分析性能变化、失败案例与额外推理开销。

> 研究仍在推进中；这里不将实验工作表述为已录用论文，也不宣称所有数据集均有提升。

#### 2. Test-Time Adaptation (TTA) · OOD 样本与决策边界分析

**2026 · 研究探索** ｜ Robustness / Distribution Shift

- 围绕图像分类中的 ID/OOD 混合测试流，比较 Source、TENT、SAR、EATA、DOCO 等方法下的预测变化行为。
- 分析 **30 万余条样本级预测记录**：观察到 OOD 样本更容易出现预测改变，而在控制置信度与分类 margin 后，差异明显减弱。
- 将观察进一步聚焦到 **decision boundary proximity**，为理解无监督适应中的样本行为提供机制层面的分析线索。

#### 3. Compositional Visual Retrieval / Reference-Image RAG

**2026–至今 · 早期探索** ｜ Multimodal Retrieval / Compositional Semantics

- 研究参考图像在组合语义检索与生成中的作用，关注跨模态表示、组合关系保持和检索证据的使用。
- 当前以文献调研、方法复现和问题定义为主，尚不将其描述为完成的系统或正式成果。

### 🛠️ 精选工程项目 / Selected Projects

| 项目 | 方向 | 具体工作 |
| --- | --- | --- |
| [**nano-radix-vllm**](https://github.com/ProIg-Chaa/nano-radix-vllm) | LLM Serving / KV Cache | 基于 nano-vllm 探索 radix-style prefix cache、跨请求 KV 复用、prefix-aware scheduling、logical-page-aware prefill 与 partial-tail reuse；保留 benchmark 和可调试结构。 |
| [**cuda-oplib**](https://github.com/ProIg-Chaa/cuda-oplib) | CUDA / C++ / PyTorch | 构建 CUDA 算子实验工程，整理 CMake、PyTorch bindings、tests、benchmarks 与 examples，服务于 kernel correctness 和 profiling 实践。 |
| [**llm-quant-benchmark**](https://github.com/ProIg-Chaa/llm-quant-benchmark) | Quantization / Benchmarking | 在统一模型、prompt 和生成设置下比较 FP16、bitsandbytes INT8/INT4、AWQ、GPTQ，记录显存、时延、吞吐及生成结果。 |
| [**turboquant-pytorch-learning**](https://github.com/ProIg-Chaa/turboquant-pytorch-learning) | KV Cache Compression | 学习并整理 TurboQuant 的 PyTorch 实现与推理接口，探索其与 Hugging Face 生成流程的集成。 |

这些仓库既有研究型原型，也有学习/实验型工程；**benchmark 的存在不等于已经获得端到端加速**。我更重视可以检验的正确性、对照实现和清晰的性能边界。

### 技术与工具 / Toolkit

`Python` · `PyTorch` · `Transformers` · `CUDA` · `C++` · `CMake` · `vLLM` · `LLM Serving` · `Benchmarking`

目前重点深化：**KV Cache / Prefix Reuse、Prefill & Decode、CUDA Memory Access、Profiling 与 MLLM Inference**。

### 交流与机会 / Open To

- MLLM reasoning、视觉证据利用、training-free inference 方向的科研交流。
- LLM inference systems、KV cache、serving efficiency、CUDA 相关工程讨论与研究合作。
- 与上述方向契合的 **Research Assistant / Research Internship / AI Infra Internship** 机会。

联系：[@ProIg-Chaa](https://github.com/ProIg-Chaa) · [AI 学习笔记](https://proig-chaa.github.io/)

---

### English Summary

I'm **Shuo Gu (Adrian)**, a Software Engineering undergraduate in the Excellence Program at **South China University of Technology** (expected graduation: 2028).

My current interests connect two areas:

1. **MLLM reasoning:** early-stage visual conditioning, training-free inference-time feedback, and the quality–cost tradeoff in multimodal generation. My ongoing **SVDF** research investigates short-horizon, image-conditioned feedback without parameter updates, with evaluations across several 7B-class models and multimodal benchmarks.
2. **LLM inference systems:** KV cache and prefix reuse, cache-aware scheduling, quantization benchmarking, CUDA operators, and reproducible performance analysis. My repositories include [nano-radix-vllm](https://github.com/ProIg-Chaa/nano-radix-vllm), [cuda-oplib](https://github.com/ProIg-Chaa/cuda-oplib), and [llm-quant-benchmark](https://github.com/ProIg-Chaa/llm-quant-benchmark).

I have also studied **test-time adaptation under distribution shift**, including sample-level ID/OOD behavior and its relationship with confidence and decision margins. I'm currently exploring **compositional visual retrieval and reference-image RAG**.

I'm interested in research collaboration and internship opportunities in **MLLM reasoning and AI Systems**. I value implementations that are **reproducible, measurable, and honest about their limitations**.

