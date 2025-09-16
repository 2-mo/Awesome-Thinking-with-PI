<h1 align="center">Awesome Thinking with PI (<u>P</u>erception & <u>I</u>nteraction)</h1>

<p align="center">
  <b>A curated list of resources on visual reasoning, video understanding, embodied AI, robot action, and perception-driven interaction.</b>
</p>


<!-- Top badges -->
<p align="center">
  <a href="https://github.com/2-mo/Awesome-Thinking-with-PI/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-MIT-blueviolet" alt="License: MIT"></a>
  <a href="https://github.com/2-mo/Awesome-Thinking-with-PI/issues"><img src="https://img.shields.io/badge/Issues-Track-orange" alt="Issues"></a>
<a href="https://github.com/2-mo/Awesome-Thinking-with-PI/pulls"><img src="https://img.shields.io/badge/Pull%20Requests-Welcome-brightgreen" alt="Pull Requests"></a>
<a href="https://github.com/2-mo/Awesome-Thinking-with-PI/commits/main"><img src="https://img.shields.io/badge/Commits-Main-blue" alt="Commits: main"></a>
</p>

<!-- [![repo](https://img.shields.io/badge/GitHub-2--mo%2FAwesome--Thinking--with--PI-black?logo=github)](https://github.com/2-mo/Awesome-Thinking-with-PI) -->



## 📚 Contents

- 🤔 [1. Why We Need Thinking?](#1-why-we-need-thinking)
  - [1.1 理论基础](#11-理论基础) - 人类视觉启示 / 多模态挑战 / 视频异常检测
  - [1.2 核心理念与方法](#12-核心理念与方法) - OpenAI思想 / 观点文章
  - [1.3 可信视觉智能](#13-可信视觉智能) - 发展趋势
  - [1.4 应用案例与工作](#14-应用案例与工作) - 代表性工作 / 最新观点
  - [1.5 理论研究](#15-理论研究) - 学术论文
- 💭 [2. Thinking with Language](#2-thinking-with-language)
  - [2.1 Language as Explicit Thought](#21-language-as-explicit-thought) - CoT / 基础推理
  - [2.2 MCTS](#22-mcts-monte-carlo-tree-search) - 蒙特卡洛树搜索
  - [2.3 R1-Style Models](#23-r1-style-models-overview截至-3-月) - r1-like models
  - [2.4 Text-Space Multimodal Reasoning](#24-text-space-multimodal-reasoning) - 文本空间多模态推理
  - [2.5 Tool-Augmented Reasoning](#25-tool-augmented-reasoning工具增强推理) - 工具使用与增强
- 🔍 [3. Thinking with Images](#3-thinking-with-images)
  - [3.1 Region-Focus](#31-region-focus-non-rlhf) - 区域聚焦
  - [3.2 Image Manipulation](#32-image-manipulation) - 图像操作
  - [3.3 基于图像交互的理解/推理](#33-基于图像交互的理解推理) - 交互式理解
  - [3.4 图像生成](#34-图像生成) - 生成与想象
  - [3.5 GUI 代理与屏幕操作](#35-gui-代理与屏幕操作) - 界面交互
- 🤖 [4. Thinking with Embodiment](#4-thinking-with-embodiment)
  - [4.1 VLA](#41-vla-is-all-you-need-) - 视觉语言动作模型
  - [4.2 具身导航](#42-具身导航无人机) - 导航与操作
- 🛠️ [5. Tutorials and Tooling](#5-tutorials-and-tooling)
  - [5.1 强化学习框架](#51-强化学习框架) - RL 框架
  - [5.2 强化学习算法](#52-强化学习算法) - 算法与优化
  - [5.3 操作实现](#53-操作实现) - 实现工具
- 📖 [6. Related Collections](#6-related-collections)
  - [6.1 综述文章](#61-综述文章) - 相关综述

---

## 1. 🤔 Why We Need Thinking?

无论在人类视觉还是多模态模型里，感知给出的观测往往不完全、含噪且多解，可靠决策必须依赖跨时整合与假设检验——这就是“思考”。

[![Wiki](https://img.shields.io/badge/Wiki-Thinking%2C%20Fast%20and%20Slow-blue?logo=wikipedia)](https://en.wikipedia.org/wiki/Thinking,_Fast,_and_Slow)

### 1.1 理论基础

#### 人类视觉的启示

- **输入不完整**：瞬时感知零碎，二维到三维存在天然歧义，仅靠直接感知容易被错觉与遮挡误导。
- **预测—校正循环**：视觉依赖自上而下与自下而上的互动，通过假设生成、误差修正来抵御歧义。
- **跨时与主动控制**：稳健行为依赖跨时因果追踪、速度–准确性权衡，以及目标驱动的注意与资源分配。

#### 多模态模型的挑战

- **多模态输入同样不全**：图像可能遮挡，语音含噪，文本歧义，模态间还可能互相冲突。
- **单次反应易偏差**：只依赖“快感知”容易被局部或错误线索牵引。
- **思考才能稳健**：跨模态/跨时间整合，假设比较与检验，风险下自适应调控，才能将嘈杂不全的感知转化为可靠决策。

#### 视频异常检测的启示
> 参见 [[LLM4VAD · Video Anomaly Detection]](./llm4vad/README.md)

### 1.2 核心理念与方法

#### OpenAI的思考方法

AI之所以会产生幻觉，是因为我们训练它的方式，从一开始，就在系统性地奖励这种瞎蒙的行为。
[![OpenAI](https://img.shields.io/badge/OpenAI-Why%20LMs%20Hallucinate-9cf?logo=openai)](https://openai.com/zh-Hans-CN/index/why-language-models-hallucinate/)

AI里最大的Bug，却也是人类文明最伟大的起点。
[![WeChat](https://img.shields.io/badge/WeChat-Article-07C160?logo=wechat)](https://mp.weixin.qq.com/s/brNtm8QLR3V9LHGznu9E2A)

### 1.3 可信视觉智能

可信并非仅来自“可解释性”，而是来自长期训练与真实世界的稳定表现（参见一次演讲中的比喻：我们信任陌生司机，多因可靠经验而非完全可解释的大脑机理）。

> Paraphrase from the [[talk]](https://www.youtube.com/watch?v=NA6EH8r-IT0): In response to a question about interpretability, Kaiming He asks—why do you trust a taxi driver you don't know? Not because the brain is fully interpretable, but because extensive real‑world training and testing make performance reliable; just like airplanes are trusted after millions of flights. Interpretability matters, yet reliability is ultimately earned through empirical evidence.



#### 趋势与发展方向
当前多模态模型在静态图像基础任务（如简单物体识别、清晰OCR、画面描述）已趋近饱和，Benchmark价值减弱。但动态视频交互、高分辨率复杂场景（如手机拍摄的倾斜快递面单、强光干扰下的局部信息捕捉）及深度逻辑推理能力仍存显著短板。未来核心方向聚焦动态建模强化、长尾场景泛化性提升，并推进电商等垂直领域实用化落地（如商品属性自动审核）。
动态多模态在真实环境适应性上的突破尤为关键，尤其在弱光或非理想构图下。

#### OpenAI的核心思想

Similar to how a human may think for a long time before responding to a difficult question, o1 uses a chain of thought when attempting to solve a problem. Through reinforcement learning, o1 learns to hone its chain of thought and refine the strategies it uses. It learns to recognize and correct its mistakes. It learns to break down tricky steps into simpler ones. It learns to try a different approach when the current one isn’t working. This process dramatically improves the model’s ability to reason.
与人类在回答难题之前可能会思考很长时间类似，o1 在尝试解决问题时也会使用思维链。通过强化学习，o1 可以学会磨练自己的思维链，并完善自己使用的策略。它学会识别和纠正错误。它学会把棘手的步骤分解成更简单的步骤。它学会在当前方法无效时尝试不同的方法。这一过程极大地提高了模型的推理能力。

[![OpenAI Learning](https://img.shields.io/badge/OpenAI-Learning%20to%20Reason-9cf?logo=openai)](https://openai.com/zh-Hant/index/learning-to-reason-with-llms/)
[![OpenAI Thinking](https://img.shields.io/badge/OpenAI-Thinking%20with%20Images-9cf?logo=openai)](https://openai.com/index/thinking-with-images/)
[![Wiki](https://img.shields.io/badge/Wiki-Visual%20Thinking-blue?logo=wikipedia)](https://en.wikipedia.org/wiki/Visual_thinking)


### 1.4 应用案例与工作

#### 代表性工作

[![OpenAI o1](https://img.shields.io/badge/OpenAI-ChatGPT--o1-9cf?logo=openai)](https://openai.com/o1/)
[![DeepSeek-R1](https://img.shields.io/github/stars/deepseek-ai/DeepSeek-R1?style=social&label=DeepSeek-R1&logo=github)](https://github.com/deepseek-ai/DeepSeek-R1)

#### 最新观点

为何GRPO大放异彩DPO销声匿迹？
[![WeChat](https://img.shields.io/badge/WeChat-GRPO%20vs%20DPO-07C160?logo=wechat)](https://mp.weixin.qq.com/s/b4OkzqfRcpFhPzTocwJatw)

### 1.5 理论研究

从语言空间到像素空间的思考有效性：

**High-level visual representations in the human brain are aligned with large language models**
[![Nature Machine Intelligence](https://img.shields.io/badge/Nature%20Machine%20Intelligence-2025-darkgreen?logo=nature)](https://www.nature.com/articles/s42256-025-01072-0)

> 研究发现人类大脑高层视觉表征与大语言模型存在显著对齐，为AI系统的视觉-语言理解提供了神经科学基础。该研究表明LLM嵌入能够成功表征大脑从自然场景中提取的复杂视觉信息，支持了多模态"思考"的生物学合理性。

**A Theoretical Understanding of Self-Correction through In-context Alignment** (NeurIPS 2024)
Wang Yifei et al.

![Self-Correction In-Context Alignment](./assets/self-correction-incontext-alignment.png)

**ExpeL: LLM Agents Are Experiential Learners** (AAAI 2024)
Zhao Andrew et al.

---

理解了“思考”的必要性之后，我们首先探索如何让模型实现这一过程。在当前的技术范式中，语言是最直接、最核心的思维载体。本章节将聚焦于模型如何利用语言构建显式的推理链条，从简单的“思维链”（Chain-of-Thought）逐步演进到更复杂的搜索与强化学习策略。

## 2. 💭 Thinking with Language

> CoT -> GoT -> MCTS -> RL

Chain-of-Thought (基础) 
    ↓
Tree/Graph of Thoughts (结构化)
    ↓  
MCTS (搜索优化)
    ↓
GRPO/RLHF (强化学习)
    ↓
R1-Style Models (现代实现)

### 2.1 Language as Explicit Thought

**Let’s Verify Step by Step** (process supervision/PRM, OpenAI): [![arXiv](https://img.shields.io/badge/arXiv-2305.20050-b31b1b?logo=arxiv)](https://arxiv.org/abs/2305.20050) -- 过程奖励

**Chain-of-Thought Prompting Elicits Reasoning in Large Language Models** [![arXiv](https://img.shields.io/badge/arXiv-2201.11903-b31b1b?logo=arxiv)](https://arxiv.org/abs/2201.11903)

**Tree of Thoughts: Deliberate Problem Solving with Large Language Models** [![arXiv](https://img.shields.io/badge/arXiv-2305.10601-b31b1b?logo=arxiv)](https://arxiv.org/abs/2305.10601)

**Graph of Thoughts: Solving Elaborate Problems with Large Language Models** [![arXiv](https://img.shields.io/badge/arXiv-2308.09687-b31b1b?logo=arxiv)](https://arxiv.org/abs/2308.09687)

**Automatic Chain of Thought Prompting in Large Language Models (ICLR 2023)** [![arXiv](https://img.shields.io/badge/arXiv-2210.03493-b31b1b?logo=arxiv)](https://arxiv.org/abs/2210.03493)

**Self-Consistency Improves Chain of Thought Reasoning in Language Models (ICLR 2023)** 
[![arXiv](https://img.shields.io/badge/arXiv-2203.11171-b31b1b?logo=arxiv)](https://arxiv.org/abs/2203.11171)
多样化思路投票

**Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena (NeurIPS 2023 Datasets and Benchmarks Track)** 
[![arXiv](https://img.shields.io/badge/arXiv-2306.05685-b31b1b?logo=arxiv)](https://arxiv.org/abs/2306.05685)

Wang Yifei et al., A Theoretical Understanding of Self-Correction through In-context Alignment, NeurIPS 2024.

### 2.2 MCTS (Monte Carlo Tree Search)

这个是一个过渡，o1刚出的时候没有技术报告，社区猜测的实现方式，在deepseek-r1之后，大家都是grpo了～

社区早期常将 o1 的“长思考”理解为 ToT/MCTS 风格搜索；在 DeepSeek‑R1 之后，主流实现更多结合 GRPO/RFT 等强化学习方法以提升过程质量与稳定性。


![llava-cot](./assets/llava-cot.png)

LLaVA-CoT — 逐步思维链用于多模态过程监督 [![arXiv](https://img.shields.io/badge/arXiv-2410.21922-b31b1b?logo=arxiv)](https://arxiv.org/abs/2410.21922)



**Timeline of o1-style releases**

|              | Sep 12 | Oct 09 | Nov 04 | Nov 15 | Nov 16 | Nov 20 | Nov 25 | Nov 28 |
|--------------|------------|------------|------------|------------|------------|------------|------------|------------|
| Release      | OpenAI o1  | O1-Journey | LLaMA-O1   | LLaVA-CoT  | K0-math    | DeepSeek-R1| InternThinker | QwQ      |
| Organization | OpenAI     | SJTU       | Shanghai AI Lab | PKU     | Moonshot AI | DeepSeek  | Shanghai AI Lab | Alibaba Group |



[A] Xu Guowei et al., LLaVA-CoT: Let Vision Language Models Reason Step-by-Step, in arXiv, 2024.


### 2.3 R1-Style Models Overview（截至 3 月）

<details>
<summary>Click to expand: R1-Style Models Overview (as of March)</summary>

| Model | Foundational LLMs | Time | Institution | Task | Feature |
|-------|------------------|------|-------------|------|---------|
| Deepseek-R1-Zero [![GitHub stars](https://img.shields.io/github/stars/deepseek-ai/DeepSeek-R1?style=social&label=GitHub&logo=github)](https://github.com/deepseek-ai/DeepSeek-R1) | Deepseek-V3-671B | Jan 22, 2025 | DeepSeek-AI | Generic | - |
| Open-R1 [![GitHub stars](https://img.shields.io/github/stars/huggingface/open-r1?style=social&label=GitHub&logo=github)](https://github.com/huggingface/open-r1) | Qwen2.5-1.5B-Instruct | Jan 24, 2025 | HuggingFace | Generic | - |
| Multimodal-Open-R1 [![GitHub stars](https://img.shields.io/github/stars/EvolvingLMMs-Lab/open-r1-multimodal?style=social&label=GitHub&logo=github)](https://github.com/EvolvingLMMs-Lab/open-r1-multimodal) | Qwen2-VL-2B/7B-Instruct | Jan 27, 2025 | LMMs-Lab | Generic | - |
| R1-V [![GitHub stars](https://img.shields.io/github/stars/Deep-Agent/R1-V?style=social&label=GitHub&logo=github)](https://github.com/Deep-Agent/R1-V) | Qwen2-VL-2B-Instruct | Feb 2, 2025 | Deep Agent | Math | - |
| VLM-R1 [![GitHub stars](https://img.shields.io/github/stars/om-ai-lab/VLM-R1?style=social&label=GitHub&logo=github)](https://github.com/om-ai-lab/VLM-R1) | Qwen2.5-VL-3B/7B | Feb 3, 2025 | Zhejiang University | Object Detection | - |
| MedVLM-R1 | Qwen2-VL-2B | Feb 26, 2025 | Technical University of Munich | Medical Image Analysis | - |
| R1-Omni [![GitHub stars](https://img.shields.io/github/stars/HumanMLLM/R1-Omni?style=social&label=GitHub&logo=github)](https://github.com/HumanMLLM/R1-Omni) | HumanOmni-0.5B | Mar 7, 2025 | Chinese Academy of Sciences | Generic | - |
| MM-Eureka-Zero | InternVL2.5-Pretrained-8B | Mar 7, 2025 | Shanghai AI Lab | Math | - |
| VisualThinker-R1-Zero [![GitHub stars](https://img.shields.io/github/stars/turningpoint-ai/VisualThinker-R1-Zero?style=social&label=GitHub&logo=github)](https://github.com/turningpoint-ai/VisualThinker-R1-Zero) | Qwen2-VL-2B | Mar 7, 2025 | University of California | Math | "Aha Moment" on a 2B Non-SFT Model |
| Seg-Zero [![GitHub stars](https://img.shields.io/github/stars/dvlab-research/Seg-Zero?style=social&label=GitHub&logo=github)](https://github.com/dvlab-research/Seg-Zero) | Qwen2.5-VL-3B + SAM2 | Mar 9, 2025 | CUHK | Segmentation | - |
| Vision-R1 [![GitHub stars](https://img.shields.io/github/stars/Osilly/Vision-R1?style=social&label=GitHub&logo=github)](https://github.com/Osilly/Vision-R1) | Qwen-2.5-VL-72B | Mar 9, 2025 | Zhejiang University | Math | - |
| MM-Eureka | InternVL2.5-Instruct-8B | Mar 10, 2025 | Shanghai AI Laboratory | Math | Leave-One-Out, RLOO |
| LMM-R1 [![GitHub stars](https://img.shields.io/github/stars/thu-SLT-Lab/LMM-R1?style=social&label=GitHub&logo=github)](https://github.com/thu-SLT-Lab/LMM-R1) | Qwen2.5-VL-Instruct-3B | Mar 10, 2025 | Southeast University | Math, ScienceQA, ChartQA | Game Planning, PPO |
| Curr-ReFT | Qwen2.5-VL-3B | Mar 10, 2025 | USTC | Detection/Classification/Math | - |
| AlphaDrive | Qwen2VL-2B | Mar 10, 2025 | HUST | Autonomous driving | - |
| DriveLMM-o1 [![GitHub stars](https://img.shields.io/github/stars/mbzuai-oryx/DriveLMM-o1?style=social&label=GitHub&logo=github)](https://github.com/mbzuai-oryx/DriveLMM-o1) | InternVL2.5-8B | Mar 13, 2025 | MBZUAI | Autonomous driving | - |
| R1-OneVision [![GitHub stars](https://img.shields.io/github/stars/Fancy-MLLM/R1-Onevision?style=social&label=GitHub&logo=github)](https://github.com/Fancy-MLLM/R1-Onevision) | Qwen2.5-VL-7B-Instruct | Mar 13, 2025 | Zhejiang University | Math/General/Science/Chart | Formal Description |
| R1-VL [![GitHub stars](https://img.shields.io/github/stars/jingyi0000/R1-VL?style=social&label=GitHub&logo=github)](https://github.com/jingyi0000/R1-VL) | Qwen2-VL-7B | Mar 17, 2025 | NYTU | Math | Step-wise Reward |
| OpenVLThinker [![GitHub stars](https://img.shields.io/github/stars/yihedeng9/OpenVLThinker?style=social&label=GitHub&logo=github)](https://github.com/yihedeng9/OpenVLThinker) | Qwen2.5-VL-7B-Instruct | Mar 21, 2025 | University of California | Math | - |
| Easy-R1 | Qwen2.5-VL | Mar 21, 2025 | Beihang University | Math | Efficient, Scalable |
| Safe RLHF-V | Qwen2-VL-7B | Mar 22, 2025 | Peking University | Multimodal Safety | - |
| Video-R1 [![GitHub stars](https://img.shields.io/github/stars/tulerfeng/Video-R1?style=social&label=GitHub&logo=github)](https://github.com/tulerfeng/Video-R1) | Qwen2.5-VL-7B | Mar 27, 2025 | CUHK | Video Reasoning | - |
| Open-R1-Video [![GitHub stars](https://img.shields.io/github/stars/Wang-Xiaodong1899/Open-R1-Video?style=social&label=GitHub&logo=github)](https://github.com/Wang-Xiaodong1899/Open-R1-Video) | Qwen2-VL-7B | Mar 27, 2025 | CUHK | Video Understanding | - |
| Embodied-Reasoner [![GitHub stars](https://img.shields.io/github/stars/zwq2018/embodied_reasoner?style=social&label=GitHub&logo=github)](https://github.com/zwq2018/embodied_reasoner) | Qwen2-VL-7B | Mar 27, 2025 | Zhejiang University | Embodied Interactive | Observation–Thought–Action |
| UI-R1 | Qwen2.5-VL-3B | Mar 27, 2025 | vivo AI Lab | Action Prediction of GUI Agents | - |
| Q-Insight [![GitHub stars](https://img.shields.io/github/stars/bytedance/Q-Insight?style=social&label=GitHub&logo=github)](https://github.com/bytedance/Q-Insight) | Qwen-2.5-VL-7B | Mar 28, 2025 | Peking University | Image Quality Assessment | - |

Note: A small GitHub badge next to a model name links to its confirmed repository. If no badge is shown, the official repo is pending or unverified.

<!-- Legend removed as Modality column was dropped -->

<!-- table ends -->

</details>

### 2.4 Text-Space Multimodal Reasoning

定义：r1‑like 的跨模态设定，推理链（CoT）主要在文本空间进行；多模态信号（图像/视频/音频/图表等）作为条件、奖励或评估信号参与训练与生成，输出可为多模态，但中间不产生视觉类中间表征。

关注：在检测/分割/视频/医学等任务中，使用 GRPO/DPO/RLHF 与过程监督改进文本空间推理的稳健性与对齐效果。

#### 评估基准/基于评价的

MM-Eureka / MM-Eureka-Zero — 留一法与RLOO强化样式 [示例](https://github.com/ShanghaiAILab/MM-Eureka)



**Vision-SR1: Self-Rewarded Vision-Language Model via Reasoning Decomposition**
腾讯AI Lab等提出自我奖励方法，分阶段提升VLM推理能力，代码已开源。



**LLaVA-Critic-R1: Your Critic Model is Secretly a Strong Policy Model**
**arXiv**：[arXiv:2509.00676](https://arxiv.org/abs/2509.00676)
**主要内容**：分析生成式奖励模型在视觉-语言任务中的表现，提出LLaVA-Critic-R1。



#### 目标检测/分割

https://github.com/om-ai-lab/VLM-R1


**Visual-RFT: Visual Reinforcement Fine-Tuning (ICCV 2025)**

[![arXiv](https://img.shields.io/badge/arXiv-2503.01785-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2503.01785)
[![GitHub stars](https://img.shields.io/github/stars/Liuziyu77/Visual-RFT?style=social&label=GitHub&logo=github)](https://github.com/Liuziyu77/Visual-RFT)

![Visual-RFT](assets/visual-rft-architecture.png)


**MedVLM-R1: Incentivizing Medical Reasoning Capability of Vision-Language Models via RL (arXiv 2025)**

[![arXiv](https://img.shields.io/badge/arXiv-2502.19634-b31b1b?logo=arxiv)](https://arxiv.org/abs/2502.19634)

Highlight: 通过强化学习激励机制提升医学多模态推理覆盖度与可靠性。

Med-R1: Reinforcement Learning for Generalizable Medical Reasoning in Vision-Language Models (arXiv 2025)

[![arXiv](https://img.shields.io/badge/arXiv-2503.13939-b31b1b?logo=arxiv)](https://arxiv.org/abs/2503.13939) [![Code](https://img.shields.io/github/stars/Yuxiang-Lai117/Med-R1?style=social&label=Code&logo=github)](https://github.com/Yuxiang-Lai117/Med-R1)

Highlight: 关注跨任务泛化的医学推理 RL 对齐范式，改进鲁棒性与数据效用。

<img src="https://github.com/Yuxiang-Lai117/Med-R1/raw/main/Images/fig_data_distribution.png" alt="Med-R1 dataset distribution" width="55%" />


SAM-R1: Leveraging SAM for Reward Feedback in Multimodal Segmentation via RL

[![arXiv](https://img.shields.io/badge/arXiv-2505.22596-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2505.22596)

![SAM-R1](assets/sam-r1-framework.png)

---

#### 视频理解 

Video-R1: Reinforcing Video Reasoning in MLLMs
强化视频时空推理 
[![arXiv](https://img.shields.io/badge/arXiv-2503.21776-b31?logo=arxiv)](https://arxiv.org/pdf/2503.21776)
[![Zhihu](https://img.shields.io/badge/Zhihu-Review-informational?logo=zhihu)](https://zhuanlan.zhihu.com/p/1889342435928282728)
[![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://github.com/tulerfeng/Video-R1)
[![GitHub stars](https://img.shields.io/github/stars/tulerfeng/Video-R1?style=social&label=GitHub&logo=github)](https://github.com/tulerfeng/Video-R1)

![Video-R1](assets/video-r1-overview.png)

**VideoChat-R1: Enhancing Spatio-Temporal Perception via Reinforcement Fine-Tuning**
[![arXiv](https://img.shields.io/badge/arXiv-2504.06958-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2504.06958)
[![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://github.com/OpenGVLab/VideoChat-R1)
[![GitHub stars](https://img.shields.io/github/stars/OpenGVLab/VideoChat-R1?style=social&label=GitHub&logo=github)](https://github.com/OpenGVLab/VideoChat-R1)

> 时空感知强化微调

![VideoChat-R1](assets/videochat-r1-overview.png)

TinyLLaVA-Video-R1: Towards Smaller LMMs for Video Reasoning
小参数视频推理
[![arXiv](https://img.shields.io/badge/arXiv-2504.09641-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2504.09641)
[![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://github.com/ZhangXJ199/TinyLLaVA-Video-R1)
[![GitHub stars](https://img.shields.io/github/stars/ZhangXJ199/TinyLLaVA-Video-R1?style=social&label=GitHub&logo=github)](https://github.com/ZhangXJ199/TinyLLaVA-Video-R1)

![TinyLLaVA-Video-R1](assets/tinyllava-video-r1-overview.png)


#### Extended Vision Modalities
其他模态（事件相机,3D,红外）




#### 可信安全

- Safe RLHF-V — 多模态安全对齐 [项目](https://github.com/PKU-Alignment/Safe-RLHF-V)

> 小结：多模态“思维—搜索—验证”闭环正在标准化，核心在于过程监督（PRM）、行为奖励与环境校验相结合。


### 2.5 Tool-Augmented Reasoning（工具增强推理）

**思维+行动的交替（检索/工具使用）(2023)**

**ReAct: Synergizing Reasoning and Acting in Language Models** <sup><kbd>ICLR 2023</kbd></sup> [![arXiv](https://img.shields.io/badge/arXiv-2210.03629-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2210.03629)
> **Core Idea**: Proposes a paradigm that interleaves `thought` (reasoning) and `action` (tool use) to solve complex tasks.

**Program of Thoughts Prompting: Disentangling Computation from Reasoning** (TMLR 2023) [![arXiv](https://img.shields.io/badge/arXiv-2211.12588-b31b1b?logo=arxiv)](https://arxiv.org/abs/2211.12588)
> **Core Idea**: Offloads calculation steps to an external interpreter (e.g., Python), allowing the LLM to focus on reasoning.

**Toolformer: Language Models Can Teach Themselves to Use Tools** (arXiv 2023) [![arXiv](https://img.shields.io/badge/arXiv-2302.04761-b31b1b?logo=arxiv)](https://arxiv.org/abs/2302.04761)
> **Core Idea**: A method for teaching LLMs to decide when and how to use external tools through simple API calls, and to incorporate the results.

**TOOLLLM: Facilitating Large Language Models to Master 16000+ Real-World APIs** <sup><kbd>ICLR 2024</kbd></sup> [![OpenReview](https://img.shields.io/badge/OpenReview-Link-green?logo=openreview)](https://openreview.net/forum?id=dHng2O0Jjr)
> **Core Idea**: A framework and dataset for training and evaluating LLMs on their ability to use a vast number of real-world APIs.

**DSPy: A framework for algorithmically optimizing LM prompts and weights** [![GitHub stars](https://img.shields.io/github/stars/stanfordnlp/dspy?style=social&label=GitHub&logo=github)](https://github.com/stanfordnlp/dspy)
> **Core Idea**: A programmatic approach (`compiling` instead of `prompting`) that separates logic from prompts to build more reliable systems.

**AgenTracer: Who Is Inducing Failure in the LLM Agentic Systems?** [![Project](https://img.shields.io/badge/Project-Website-blue?logo=safari)](https://bingreeky.github.io/atracer/)
> **Team**: Shuicheng Yan's team (颜水成老师团队)
> **Core Idea**: An automated framework for attributing failures in multi-agent systems, improving debugging and diagnosis efficiency.


## 3. 🖼️ Thinking with Images 

从纯文本推理到与感知深度融合，本章将探讨一种更高级的范式：**图文交错的多模态推理** (Interleaved Vision-Language Reasoning)。

> 这种范式与 r1-like 模型有着本质区别。r1-like 模型通常将图像作为一次性的初始输入，其后的推理链完全在文本空间展开。而在这里，**视觉表征本身就是推理过程的一部分**。模型会与视觉信息进行多轮交互，在推理过程中主动生成并利用新的视觉产物（如裁剪、标注、草图），实现“边看边想、边画边想”的深度融合。这与“Thinking across Modalities”中推理链主要局限于文本空间形成鲜明对比。



### 3.1 Region-Focus (Non-RLHF)

LSNet: See Large, Focus Small [![arXiv](https://img.shields.io/badge/arXiv-2503.23135-b31b1b?logo=arxiv)](https://arxiv.org/abs/2503.23135) [![GitHub stars](https://img.shields.io/github/stars/THU-MIG/lsnet?style=social&label=GitHub&logo=github)](https://github.com/THU-MIG/lsnet)

A Stitch in Time Saves Nine: Small VLM is a Precise Guidance for accelerating Large VLMs (CVPR 2025) [![GitHub stars](https://img.shields.io/github/stars/NUS-HPC-AI-Lab/SGL?style=social&label=GitHub&logo=github)](https://github.com/NUS-HPC-AI-Lab/SGL)

**VLsI**: **V**erbalized **L**ayer**s**-to-**I**nteractions from Large to Small Vision Language Models [![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://byungkwanlee.github.io/VLsI-page/) [![arXiv](https://img.shields.io/badge/arXiv-2412.01822-b31b1b?logo=arxiv)](https://arxiv.org/abs/2412.01822)

Boltzmann Attention Sampling for Image Analysis with Small Objects (CVPR 2025) [![arXiv](https://img.shields.io/badge/arXiv-2503.02841-b31b1b?logo=arxiv)](https://arxiv.org/abs/2503.02841) [![GitHub stars](https://img.shields.io/github/stars/microsoft/BoltzFormer?style=social&label=GitHub&logo=github)](https://github.com/microsoft/BoltzFormer)



### 3.2 Image Manipulation

**Number it: Temporal Grounding Videos like Flipping Manga**
[![arXiv](https://img.shields.io/badge/arXiv-2411.10332-b31b1b?logo=arxiv)](https://arxiv.org/abs/2411.10332)


**Instruction-Guided Visual Masking** [[paper](https://arxiv.org/pdf/2405.19783)] [[code](https://github.com/2toinf/IVM)]

Plug-and-play module: mask irrelevant regions to enable better understanding by large models.

![Instruction-Guided Visual Masking example](assets/instruction-masking-example.png)

**COGCOM: A VISUAL LANGUAGE MODEL WITH CHAIN-OF-MANIPULATIONS REASONING** [[paper](https://arxiv.org/pdf/2402.04236)] [[code](https://github.com/THUDM/CogCoM)]

Chain of manipulations; intrinsic operations (e.g., locate, zoom) that produce intermediate outputs (e.g., bounding boxes, image patches).

![CogCoM chain-of-manipulations example](assets/cogcom-chain-example.png)

Number it: Temporal Grounding Videos like Flipping Manga (CVPR 2025) [![arXiv](https://img.shields.io/badge/arXiv-2411.10332-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2411.10332)

![Flipping Manga temporal grounding example](assets/number-it-example.png)





### 3.3 基于图像交互的理解/推理

**Simple o3: Towards Interleaved Vision-Language Reasoning**
[![arXiv](https://img.shields.io/badge/arXiv-2508.12109-b31b1b?logo=arxiv)](https://arxiv.org/abs/2508.12109)

> Interleaved Reasoning, Tool-Use, Visual Planning
> 面向“图文交错推理”的端到端方法，结合可执行视觉操作（裁剪/放大/复用图像）与语言推理，强化长链多模态推理与细粒度理解。


**Mini-o3: Scaling Up Reasoning Patterns and Interaction for Visual Search**

[![arXiv](https://img.shields.io/badge/arXiv-2509.07969-b31b1b?logo=arxiv)](https://arxiv.org/abs/2509.07969)
[![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://mini-o3.github.io/)
[![GitHub stars](https://img.shields.io/github/stars/Mini-03/Mini-o3?style=social&label=GitHub&logo=github)](https://github.com/Mini-03/Mini-o3)
[![Zhihu](https://img.shields.io/badge/Zhihu-Review-informational?logo=zhihu)](https://zhuanlan.zhihu.com/p/1949143503058760011)

> 字节跳动等提出Mini-o3系统，通过多步交互和深度推理提升视觉搜索任务表现。
> 
> ![alt text](./assets/mini-o3.png)


**LaV-CoT: Language-Aware Visual CoT with Multi-Aspect Reward Optimization for Real-World Multilingual VQA**
Ant Group & Nanyang Technological University
https://arxiv.org/abs/2509.10026
https://github.com/HJNVR/LaV-CoT

![alt text](./assets/lav-cot.png)


**Introducing Visual Perception Token into Multimodal Large Language Model**
[![arXiv](https://img.shields.io/badge/arXiv-2502.17425-b31b1b?logo=arxiv)](https://arxiv.org/abs/2502.17425)
[![GitHub stars](https://img.shields.io/github/stars/yu-rp/VisualPerceptionToken?style=social&label=GitHub&logo=github)](https://github.com/yu-rp/VisualPerceptionToken)

> 提出视觉感知令牌概念，赋予MLLM自主控制视觉感知过程的能力。包括区域选择令牌和视觉重编码令牌两种类型，使模型能够自主识别需要进一步感知的特定区域或使用隐藏状态作为控制信号。
> 
> ![alt text](./assets/VisualPerceptionToken.png)
> 视觉重编码（Vision Re-Encoding）进一步调用 DINO 特征，并利用语言模型隐藏状态控制特征选择，实现“粗看—再细看”的两步感知，更接近人类观察过程(专注地看)。



**Thyme: Think Beyond Images**
> 开源多模态大模型Thyme，支持主动调用工具进行复杂图像处理和数学计算，具备高度自主性。


**OCR Comparison: Expert Models vs. Vision-Language Models**
> 介绍通义团队提出的点金OCR-R1，及其与主流视觉语言模型在复杂文档解析任务中的对比表现。


**Vision-G1: Towards General Vision Language Reasoning with Multi-Domain Data Curation**
[![arXiv](https://img.shields.io/badge/arXiv-2508.12680-b31b1b?logo=arxiv)](https://arxiv.org/abs/2508.12680)

> UCSD等提出多领域数据整理和多轮强化学习训练管道，提升视觉语言模型的广泛推理能力。


**PyVision: Enabling Fast, Interactive Visual Programming with AI**
[![PyVision arXiv](https://img.shields.io/badge/PyVision-arXiv-ff69b4?logo=arxiv)](https://arxiv.org/pdf/2507.07998) [![PyVision Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://agent-x.space/pyvision/)

> <img src="./assets/pyvision-overview.png" alt="PyVision overview" width="60%" />


**DeepEyes: Incentivizing "Thinking with Images" via Reinforcement Learning**
[![arXiv](https://img.shields.io/badge/arXiv-2505.14362-b31b1b?logo=arxiv)](https://arxiv.org/abs/2505.14362)

> ![deepeyes-overview](./assets/deepeyes-overview.png)



**VisualToolAgent (VisTA): A Reinforcement Learning Framework for Visual Tool Selection**

![VisTA overview](./assets/vista-overview.png)


**REVPT: Reinforced Visual Perception with Tools**
[![GitHub stars](https://img.shields.io/github/stars/Is-kelvin/REVPT?style=social&label=GitHub&logo=github)](https://github.com/Is-kelvin/REVPT) [![arXiv](https://img.shields.io/badge/arXiv-2509.01656-b31b1b?logo=arxiv)](https://arxiv.org/abs/2509.01656)

提出REVPT方法，通过RL训练多模态大模型使用视觉工具，提升感知-推理能力。


**VLM-R3: Region Recognition, Reasoning, and Refinement for Enhanced Multimodal Chain-of-Thought**
[![arXiv](https://img.shields.io/badge/arXiv-2505.16192-b31b1b?logo=arxiv)](https://arxiv.org/abs/2505.16192)

> 提出VLM-R3框架，强化MLLM在视觉区域识别与推理能力，提升多模态链式推理表现。


**Ego-R1: Chain-of-Tool-Thought for Ultra-Long Egocentric Video Reasoning**

> 提出Ego-R1智能体，采用Chain-of-Tool-Thought方法，支持超长自中心视频推理。


**M2IO-R1: An Efficient RL-Enhanced Reasoning Framework for Multimodal Retrieval Augmented Multimodal Generation**
[![arXiv](https://img.shields.io/badge/arXiv-2508.06328-b31b1b?logo=arxiv)](https://arxiv.org/abs/2508.06328)

> 北大等提出的多模态检索增强生成框架，采用RL优化多模态输入输出，提升推理能力和效率。


**VLM-FO1: A New Object Detection Method for Vision-Language Models**
> 介绍VLM-FO1模型，通过“画框”方式提升视觉语言模型的目标检测精度。



#### 视频理解

**VideoChat-A1: Thinking with Long Videos by Chain-of-Shot Reasoning**
[![arXiv](https://img.shields.io/badge/arXiv-2506.06097-b31b1b?logo=arxiv)](https://arxiv.org/abs/2506.06097)

王利民老师团队，乔宇老师

![VideoChat-A1](./assets/videochat-a1-overview.png)

**RynnEC: Bringing MLLMs into Embodied World**
[![GitHub stars](https://img.shields.io/github/stars/alibaba-damo-academy/RynnEC?style=social&label=GitHub&logo=github)](https://github.com/alibaba-damo-academy/RynnEC)

阿里达摩院提出RynnEC视频多模态大模型，支持区域级视频交互，提升具身智能任务表现。


**ReasonAct: Progressive Training for Fine-Grained Video Reasoning in Small Models**

提出三阶段渐进式训练范式，提升小型多模态模型在复杂视频推理任务上的表现。


### 3.4 图像生成


> Thinking with Images for Multimodal Reasoning: Foundations, Methods, and Future Frontiers


<details>
<summary>
Stage1: Tool-Driven Visual Exploration
-> Stage2: Programmatic Visual Manipulation
-> Stage3: Intrinsic Visual Imagination
</summary>

**Visual Planning: Let's Think Only with Images**
[![arXiv](https://img.shields.io/badge/arXiv-2505.11409-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2505.11409)   [![GitHub stars](https://img.shields.io/github/stars/yix8/VisualPlanning?style=social&label=GitHub&logo=github)](https://github.com/yix8/VisualPlanning)

> ![Visual Planning](assets/visual-planning-teaser.png)


**T2I-R1: Reinforcing Image Generation with Collaborative Semantic-level and Token-level CoT**
[![arXiv](https://img.shields.io/badge/arXiv-2505.00703-b31b1b?logo=arxiv)](https://arxiv.org/abs/2505.00703)
[![Code](https://img.shields.io/github/stars/CaraJ7/T2I-R1?style=social&label=Code&logo=github)](https://github.com/CaraJ7/T2I-R1)

> Highlight: 将 R1 式逐步推理/奖励思路引入文本到图像生成。
> 
> ![alt text](./assets/t2i-r1.png)

**GRIT: Teaching MLLMs to Think with Images**
[![WeChat](https://img.shields.io/badge/WeChat-Explainer-07C160?logo=wechat)](https://mp.weixin.qq.com/s/I3bk4FGOwrj-tKl_IYRfKw)

> Highlight: 以视觉为中介的“图像思考”范式解读与科普。

**d1: Scaling Reasoning in Diffusion Large Language Models via Reinforcement Learning (arXiv 2025)**

[![arXiv](https://img.shields.io/badge/arXiv-2504.12216-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2504.12216)

> Highlight: 将强化学习用于扩散式大模型，提升复杂推理能力。

**DanceGRPO (Text-to-Image)**
[![Code](https://img.shields.io/github/stars/XueZeyue/DanceGRPO?style=social&label=Code&logo=github)](https://github.com/XueZeyue/DanceGRPO)

> Highlight: 面向文生图的 GRPO 训练与策略实现。

**Flow-GRPO: Training Flow Matching Models via Online RL**
[![Code](https://img.shields.io/github/stars/yifan123/flow_grpo?style=social&label=Code&logo=github)](https://github.com/yifan123/flow_grpo)

> Highlight: 基于 Flow/扩散流程的 GRPO 训练范式与实践。

**Interleaving Reasoning for Better Text-to-Image Generation (IRG)**
[![Code](https://img.shields.io/github/stars/Osilly/Interleaving-Reasoning-Generation?style=social&label=Code&logo=github)](https://github.com/Osilly/Interleaving-Reasoning-Generation)

> Highlight: 交错式推理提升文本生成图像的细节与一致性；提供可复现实验与开源代码。


**Draw-In-Mind: Learning Precise Image Editing via Chain-of-Thought Imagination (DIM)**
[![Code](https://img.shields.io/github/stars/showlab/DIM?style=social&label=Code&logo=github)](https://github.com/showlab/DIM)

> Highlight: 链式思维驱动的精确图像编辑与专用数据集，显著提升复杂指令下的编辑精度。

**PromptEnhancer: A Simple Approach to Enhance Text-to-Image Models via Chain-of-Thought Prompt Rewriting**
[![arXiv](https://img.shields.io/badge/arXiv-2509.04545-b31b1b?logo=arxiv)](https://arxiv.org/abs/2509.04545)
[![Code](https://img.shields.io/github/stars/Hunyuan-PromptEnhancer/PromptEnhancer?style=social&label=Code&logo=github)](https://github.com/Hunyuan-PromptEnhancer/PromptEnhancer)
[![Project](https://img.shields.io/badge/Project-Website-0a84ff?logo=safari)](https://hunyuan-promptenhancer.github.io/)

> Highlight: 利用思维链对提示语进行重写，改善文本到图像的生成质量与对齐程度。

</details>

### 3.5 GUI 代理与屏幕操作

信息空间交互，迈向具身智能

UI-R1 — 图形界面智能体动作预测 [项目](https://github.com/vivo-ai-lab/UI-R1)
Qwen-Agent — 工具增强与GUI自动化生态 [项目](https://github.com/QwenLM/Qwen-Agent/tree/main)


Mobile-Agent-v3: Fundamental Agents for GUI Automation
https://arxiv.org/pdf/2508.15144
https://github.com/X-PLUG/MobileAgent

![mobileagentv3_framework](./assets/mobileagentv3-framework.png)


Learning Active Perception via Self-Evolving Preference Optimization for GUI Grounding
**主要内容**：提出LASER框架，提升VLM在GUI理解任务中的主动感知与多步推理能力。
**链接**：[https://github.com/wwfnb/Laser](https://github.com/wwfnb/Laser)




## 4. 🤖 Thinking with Embodiment

从语言思考到图文思考，我们逐步增强了模型在数字世界中的感知与推理能力。然而，要实现通用人工智能，模型必须能够与物理世界进行交互。本章将探讨“思考”的最终前沿：**具身智能（Embodied AI）**。

在这里，“思考”不再仅仅是为了理解或生成内容，而是为了**指导行动**。模型需要将感知、推理与物理动作（如导航、抓取、操作）相结合，形成一个完整的“感知—思考—行动”闭环。我们将看到，视觉语言动作模型（VLA）如何成为连接数字智能与物理现实的关键桥梁。

### 4.1 VLA is All You Need ！

**Magma: A Foundation Model for Multimodal AI Agents (CVPR 2025)**
[![arXiv](https://img.shields.io/badge/arXiv-2502.13130-b31b1b?logo=arxiv)](https://www.arxiv.org/pdf/2502.13130)
[![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://microsoft.github.io/Magma/)
[![GitHub stars](https://img.shields.io/github/stars/microsoft/Magma?style=social&label=GitHub&logo=github)](https://github.com/microsoft/Magma)


Microsoft Research 高剑峰团队

![alt text](./assets/magma-overview.png)


F1: A Vision-Language-Action Model Bridging Understanding and Generation to Actions

![alt text](./assets/f1-paradigms-for-manipulation-policies.png)


RoboPoint: A Vision-Language Model for Spatial Affordance Prediction for Robotics

[![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://robo-point.github.io/)
[![GitHub stars](https://img.shields.io/github/stars/wentaoyuan/RoboPoint?style=social&label=GitHub&logo=github)](https://github.com/wentaoyuan/RoboPoint)
[![Datasets](https://img.shields.io/badge/Datasets-HuggingFace-orange?logo=huggingface)](https://huggingface.co/datasets/wentao-yuan/robopoint-data)

![Embodied-Reasoner](assets/robopoint.png)

From Seeing to Doing: Bridging Reasoning and Decision for Robotic Manipulation

[![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://embodied-fsd.github.io/)
[![GitHub stars](https://img.shields.io/github/stars/pickxiguapi/Embodied-FSD?style=social&label=GitHub&logo=github)](https://github.com/pickxiguapi/Embodied-FSD)
[![Datasets](https://img.shields.io/badge/Datasets-HuggingFace-orange?logo=huggingface)](https://huggingface.co/IffYuan)
[![Email](https://img.shields.io/badge/Contact-yuanyf%40tju.edu.cn-informational?logo=gmail)](mailto:yuanyf@tju.edu.cn)

![Embodied-Reasoner](assets/fsd.png)

Embodied-R1: Reinforced Embodied Reasoning for General Robotic Manipulation

[![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://embodied-r1.github.io/)
[![GitHub stars](https://img.shields.io/github/stars/pickxiguapi/Embodied-R1?style=social&label=GitHub&logo=github)](https://github.com/pickxiguapi/Embodied-R1)
[![Datasets](https://img.shields.io/badge/Datasets-HuggingFace-orange?logo=huggingface)](https://huggingface.co/IffYuan)
[![Email](https://img.shields.io/badge/Contact-yuanyf%40tju.edu.cn-informational?logo=gmail)](mailto:yuanyf@tju.edu.cn)

![Embodied-Reasoner](assets/embodied-r1.png)

Embodied-Reasoner: Synergizing Visual Search, Reasoning, and Action for Embodied Interactive Tasks

[![arXiv](https://img.shields.io/badge/arXiv-2503.21696-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2503.21696v1)
[![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://embodied-reasoner.github.io/)
[![GitHub stars](https://img.shields.io/github/stars/zwq2018/embodied_reasoner?style=social&label=GitHub&logo=github)](https://github.com/zwq2018/embodied_reasoner)

![Embodied-Reasoner](assets/embodied-reasoner-overview.png)

---

Reason-RFT: Reinforcement Fine-Tuning for Visual Reasoning

[![arXiv](https://img.shields.io/badge/arXiv-2503.20752-b31b1b?logo=arxiv)](https://arxiv.org/abs/2503.20752)
[![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://tanhuajie.github.io/ReasonRFT/)
[![GitHub stars](https://img.shields.io/github/stars/tanhuajie/Reason-RFT?style=social&label=GitHub&logo=github)](https://github.com/tanhuajie/Reason-RFT)

![Reason-RFT](assets/teaser.png)

---

Think Small, Act Big: Primitive Prompt Learning for Lifelong Robot Manipulation

[![CVPR 2025](https://img.shields.io/badge/CVPR-2025-blue)](https://openaccess.thecvf.com/content/CVPR2025/papers/Yao_Think_Small_Act_Big_Primitive_Prompt_Learning_for_Lifelong_Robot_CVPR_2025_paper.pdf)

![Think Small, Act Big](assets/think-small-act-big.png)

---

### 4.2 具身导航（无人机）
OpenFly: A Versatile Toolchain and Large-scale Benchmark for Aerial Vision-Language Navigation

[![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://shailab-ipec.github.io/openfly/)

![OpenFly](assets/toolchain.png)

---



AgentThink: A Unified Framework for Tool-Augmented Chain-of-Thought Reasoning in Vision-Language Models for Autonomous Driving

[![arXiv](https://img.shields.io/badge/arXiv-2505.15298-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2505.15298)

![AgentThink](assets/agentthink-overview.png)
小米团队



---

前面我们探讨了“思考”在不同模态（语言、图像、具身）中的理论与应用。为了将这些前沿理念付诸实践，我们需要强大的工具和框架。本章节将聚焦于实现这些复杂系统所需的核心技术，特别是强化学习相关的框架与算法，并提供一系列可以直接上手的开源项目。

## 5. 🛠️ Tutorials and Tooling


### 5.1 强化学习框架

微软研究院提出的零代码强化学习（RL）优化 AI Agent 的工业级方案。
https://github.com/microsoft/agent-lightning

### 5.2 强化学习算法

**Title**: Part I: Tricks or Traps? A Deep Dive into RL for LLM Reasoning
**主要内容**: 阿里团队关于RL4LLM领域的论文，分析PPO等RL方法在大模型推理中的应用与挑战。


卡片化汇总主流/新近的对齐与策略优化方法，统一展示 arXiv / 官方链接 / 代码。

DPO: Direct Preference Optimization (arXiv 2023)
[![arXiv](https://img.shields.io/badge/arXiv-2305.18290-b31b1b?logo=arxiv)](https://arxiv.org/abs/2305.18290)

Highlight: 直接在偏好数据上拟合概率偏序，避免显式奖励建模。

Agentic Reinforced Policy Optimization (ARPO, arXiv 2025)
[![arXiv](https://img.shields.io/badge/arXiv-2507.19849-b31b1b?logo=arxiv)](https://arxiv.org/abs/2507.19849)

Highlight: 面向智能体交互的强化对齐策略优化，聚焦多阶段推理质量。

GAPO: Learning Preferential Prompt through Generative Adversarial Policy Optimization (ACL 2025)
[![ACL](https://img.shields.io/badge/ACL-2025-1877F2)](https://aclanthology.org/2025.acl-long.13/) [![Code](https://img.shields.io/github/stars/MikeGu721/GAPO?style=social&label=Code&logo=github)](https://github.com/MikeGu721/GAPO)

Highlight: 生成式对抗 + 偏好信号联合，提升提示学习与策略稳定性。

PAPO: Perception-Aware Policy Optimization for Multimodal Reasoning
[![Code](https://img.shields.io/github/stars/MikeWangWZHL/PAPO?style=social&label=Code&logo=github)](https://github.com/MikeWangWZHL/PAPO)

Highlight: 针对 GRPO 的改进方法（稳定性 / 收敛效率）。

TreePO: Bridging Policy Optimization and Inference Efficiency (arXiv 2025)
[![arXiv](https://img.shields.io/badge/arXiv-2508.17445-b31b1b?logo=arxiv)](https://arxiv.org/abs/2508.17445)

Highlight: 引入树式启发结构，兼顾对齐效果与推理效率。

RuleReasoner: Reinforced Rule-based Reasoning via Domain-aware Dynamic Sampling (arXiv 2025)
[![arXiv](https://img.shields.io/badge/arXiv-2509.06461v1-b31b1b?logo=arxiv)](https://arxiv.org/abs/2509.06461v1) [![Code](https://img.shields.io/github/stars/bigai-nlco/RuleReasoner?style=social&label=Code&logo=github)](https://github.com/bigai-nlco/RuleReasoner)

Highlight: 结合领域规则动态采样与强化优化，提高结构化推理质量与可控性。


PREF-GRPO: Pairwise Preference Reward-Based GRPO for Stable Text-to-Image Reinforcement Learning
- **作者**：Yibin Wang, Zhimin Li, Yuhang Zang, 等
- **主要内容**：提出首个基于成对偏好奖励的GRPO方法，提升文本生成图像的稳定性，缓解reward hacking问题。
- **链接**：[codegoat24.github.io/UnifiedReward/Pref-GRPO](https://codegoat24.github.io/UnifiedReward/Pref-GRPO)
- **arXiv**：[arxiv.org/pdf/2508.20751](https://arxiv.org/pdf/2508.20751)

---
### 5.3 操作实现


[![EasyR1](https://img.shields.io/github/stars/hiyouga/EasyR1?style=social&label=EasyR1&logo=github)](https://github.com/hiyouga/EasyR1) — R1 训练与复现的简洁模板。


[![Multimodal-Open-R1](https://img.shields.io/github/stars/EvolvingLMMs-Lab/open-r1-multimodal?style=social&label=Multimodal-Open-R1&logo=github)](https://github.com/EvolvingLMMs-Lab/open-r1-multimodal) — 通用多模态 R1。


[![R1-VL](https://img.shields.io/github/stars/jingyi0000/R1-VL?style=social&label=R1-VL&logo=github)](https://github.com/jingyi0000/R1-VL) — 视觉-语言逐步奖励。

[![Open-R1-Video](https://img.shields.io/github/stars/Wang-Xiaodong1899/Open-R1-Video?style=social&label=Open-R1-Video&logo=github)](https://github.com/Wang-Xiaodong1899/Open-R1-Video) — 开源视频 R1 范式。


[![RLFactory-Agent](https://img.shields.io/github/stars/Simple-Efficient/RL-Factory?style=social&label=RLFactory-Agent&logo=github)](https://github.com/Simple-Efficient/RL-Factory) — RL 工具与代理训练框架。

[![Qwen-Agent](https://img.shields.io/badge/Industry-Qwen--Agent-blueviolet?logo=github)](https://github.com/QwenLM/Qwen-Agent/tree/main)


## 6. 📖 Related Collections

[![arXiv](https://img.shields.io/badge/arXiv-2508.17281-b31b1b?logo=arxiv)](https://arxiv.org/abs/2508.17281) — From Language to Action: A Review of Large Language Models as Autonomous Agents and Tool Users 


[![System-2-Research](https://img.shields.io/github/stars/open-thought/system-2-research?style=flat&color=black&label=system-2-research&logo=github&logoColor=white)](https://github.com/open-thought/system-2-research) — System‑2 agents, tool‑use, and planning resources.

[![Efficient-Reasoning](https://img.shields.io/github/stars/Zanette-Labs/efficient-reasoning?style=flat&color=black&label=efficient-reasoning&logo=github&logoColor=white)](https://github.com/Zanette-Labs/efficient-reasoning) — Compute/data‑efficient reasoning methods and benchmarks.


[![Awesome-Thinking-With-Images](https://img.shields.io/github/stars/ligeng0197/Awesome-Thinking-With-Images?style=flat&color=black&label=Awesome-Thinking-With-Images&logo=github&logoColor=white)](https://github.com/ligeng0197/Awesome-Thinking-With-Images) — Broad visual thinking and perception resources.

[![Thinking-with-Generated-Images](https://img.shields.io/github/stars/GAIR-NLP/thinking-with-generated-images?style=flat&color=black&label=thinking-with-generated-images&logo=github&logoColor=white)](https://github.com/GAIR-NLP/thinking-with-generated-images) — Reasoning with generated intermediate images (papers + code).


[![Awesome-Self-Evolving-Agents](https://img.shields.io/github/stars/EvoAgentX/Awesome-Self-Evolving-Agents?style=flat&color=black&label=Awesome-Self-Evolving-Agents&logo=github&logoColor=white)](https://github.com/EvoAgentX/Awesome-Self-Evolving-Agents) — Self‑evolving agents (auto‑improvement, reflection, curricula).


### 6.1 综述文章


[![Awesome_Think_With_Images](https://img.shields.io/github/stars/zhaochen0110/Awesome_Think_With_Images?style=flat&color=black&label=Awesome_Think_With_Images&logo=github&logoColor=white)](https://github.com/zhaochen0110/Awesome_Think_With_Images) — Visual-only reasoning with images (papers + code).


Agent AI: Surveying the Horizons of Multimodal Interaction
李飞飞团队

AI agent（AI 智能体）定义：一个具体的系统或程序，它能够在某个环境中感知、决策并采取行动以完成任务。
Agent AI 定义：一类以智能体为核心范式的人工智能技术或系统框架，关注多模态交互、动态适应能力以及通用智能的实现。
AI agent 是实现，Agent AI 是框架和研究方向


Explain Before You Answer: A Survey on Compositional Visual Reasoning
- **作者**：Fucai Ke, Joy Hsu, Zhixi Cai, 等
- **主要内容**：综述2023-2025年组合式视觉推理（CVR）相关文献，系统梳理260+论文。
- **arXiv**：[arXiv:2508.17298](https://arxiv.org/abs/2508.17298)



**The Landscape of Agentic Reinforcement Learning for LLMs: A Survey**
[![arXiv](https://img.shields.io/badge/arXiv-2509.02547-b31b1b?logo=arxiv)](https://arxiv.org/abs/2509.02547) 
[![Awesome-AgenticLLM-RL-Papers](https://img.shields.io/github/stars/xhyumiracle/Awesome-AgenticLLM-RL-Papers?style=flat&color=black&label=Awesome-AgenticLLM-RL-Papers&logo=github&logoColor=white)](https://github.com/xhyumiracle/Awesome-AgenticLLM-RL-Papers) 



**The Landscape of Agentic Reinforcement Learning for LLMs: A Survey.**


**A Survey of Reinforcement Learning for Large Reasoning Models**
地址：https://arxiv.org/pdf/2509.08827
周伯文老师团队

![aaa](./assets/survey_rl4lrm.png)

**主要内容**: 清华大学等团队系统梳理了RL+LLMs领域的最新进展，涵盖奖励设计、训练范式、多智能体、工具学习等多个方向。
**链接**: https://github.com/TsinghuaC3I/Awesome-RL-for-LRMs