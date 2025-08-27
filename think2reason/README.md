<h1 align="center">Awesome Thinking with PI (Perception & Interaction)</h1>

<p align="center">
  <b>A curated list of resources on visual reasoning, video understanding, embodied AI, robot action, and perception-driven interaction.</b>
</p>

<!-- 顶部徽章区（Badges） -->
<p align="center">
  <a href="https://github.com/ligeng0197/Awesome-Thinking-With-Images/blob/main/LICENSE"><img src="https://img.shields.io/github/license/ligeng0197/Awesome-Thinking-With-Images?color=blueviolet"></a>
  <a href="https://github.com/ligeng0197/Awesome-Thinking-With-Images/graphs/contributors"><img src="https://img.shields.io/github/contributors/ligeng0197/Awesome-Thinking-With-Images?color=ffaa00"></a>
</p>



## 📚 Contents

- 💭 [Thinking with Text](#thinking-with-text)
- 🖼️ [Thinking with Image](#thinking-with-image)
- 🤖 [Thinking with Action](#thinking-with-action)
- 🤝 [Contributing](#contributing)

---

## 💭 Thinking with Text

### R1-Style Reasoning Models Overview

| Model | Foundational LLMs | Time | Institution | Task | Feature | Modality | Learning | Algorithm |
|-------|------------------|------|-------------|------|---------|----------|----------|-----------|
| Deepseek-R1-Zero | Deepseek-V3-671B | Jan 22, 2025 | DeepSeek-AI | Generic | - | T | SFT+RL | GRPO |
| Open-R1 | Qwen2.5-1.5B-Instruct | Jan 24, 2025 | HuggingFace | Generic | - | T | SFT+RL | GRPO |
| Multimodal-Open-R1 | Qwen2-VL-2B/7B-Instruct | Jan 27, 2025 | LMMs-Lab | Generic | - | T,I | RL | GRPO |
| R1-V | Qwen2-VL-2B-Instruct | Feb 2, 2025 | Deep Agent | Math | - | T,I | RL | GRPO |
| VLM-R1 | Qwen2.5-VL-3B/7B | Feb 3, 2025 | Zhejiang University | Object Detection | - | T,I | RL | GRPO |
| MedVLM-R1 | Qwen2-VL-2B | Feb 26, 2025 | Technical University of Munich | Medical Image Analysis | - | T,I | SFT+RL | GRPO |
| R1-Omni | HumanOmni-0.5B | Mar 7, 2025 | Chinese Academy of Sciences | Generic | - | T,I,V,A | SFT+RL | GRPO |
| MM-Eureka-Zero | InternVL2.5-Pretrained-8B | Mar 7, 2025 | Shanghai AI Lab | Math | - | T,I | RL | GRPO |
| VisualThinker-R1-Zero | Qwen2-VL-2B | Mar 7, 2025 | University of California | Math | "Aha Moment" on a 2B Non-SFT Model | T,I | RL | GRPO |
| Seg-Zero | Qwen2.5-VL-3B + SAM2 | Mar 9, 2025 | CUHK | Segmentation | - | T,I | RL | GRPO |
| Vision-R1 | Qwen-2.5-VL-72B | Mar 9, 2025 | Zhejiang University | Math | - | T,I | RL | GRPO |
| MM-Eureka | InternVL2.5-Instruct-8B | Mar 10, 2025 | Shanghai AI Laboratory | Math | Leave-One-Out | T,I | SFT+RL | RLOO |
| LMM-R1 | Qwen2.5-VL-Instruct-3B | Mar 10, 2025 | Southeast University | Math, ScienceQA, ChartQA | Game Planning | T,I | RL | PPO |
| Curr-ReFT | Qwen2.5-VL-3B | Mar 10, 2025 | USTC | Detection/Classification/Math | - | T,I | RL+SFT | GRPO |
| AlphaDrive | Qwen2VL-2B | Mar 10, 2025 | HUST | Autonomous driving | - | T,I | RL+SFT | GRPO |
| DriveLMM-o1 | InternVL2.5-8B | Mar 13, 2025 | MBZUAI | Autonomous driving | - | T,I | RL+SFT | GRPO |
| R1-OneVision | Qwen2.5-VL-7B-Instruct | Mar 13, 2025 | Zhejiang University | Math/General/Science/Chart | Formal Description | T,I | SFT | - |
| R1-VL | Qwen2-VL-7B | Mar 17, 2025 | NYTU | Math | Step-wise Reward | T,I | RL | StepGPRO |
| OpenVLThinker | Qwen2.5-VL-7B-Instruct | Mar 21, 2025 | University of California | Math | - | T,I | SFT+RL | GRPO |
| Easy-R1 | Qwen2.5-VL | Mar 21, 2025 | Beihang University | Math | Efficient, Scalable | T,I | RL | GRPO |
| Safe RLHF-V | Qwen2-VL-7B | Mar 22, 2025 | Peking University | Multimodal Safety | - | T,I | RL | GRPO |
| Video-R1 | Qwen2.5-VL-7B | Mar 27, 2025 | CUHK | Video Reasoning | - | T,I,V | - | - |
| Open-R1-Video | Qwen2-VL-7B | Mar 27, 2025 | CUHK | Video Understanding | - | T,I,V | RL | GRPO |
| Embodied-Reasoner | Qwen2-VL-7B | Mar 27, 2025 | Zhejiang University | Embodied Interactive | Observation–Thought–Action | T,I,V,A | RL | - |
| UI-R1 | Qwen2.5-VL-3B | Mar 27, 2025 | vivo AI Lab | Action Prediction of GUI Agents | - | T,I | RL | GRPO |
| Q-Insight | Qwen-2.5-VL-7B | Mar 28, 2025 | Peking University | Image Quality Assessment | - | T,I | RL | GRPO |

**Legend:**
- **Modality**: T=Text, I=Image, V=Video, A=Audio
- **Learning**: SFT=Supervised Fine-Tuning, RL=Reinforcement Learning
- **Algorithm**: GRPO=Group Relative Policy Optimization, RLOO=Reinforce Leave-One-Out, PPO=Proximal Policy Optimization

### Reasoning as &lt;think&gt;

#### Open R1 Video

[![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://github.com/Wang-Xiaodong1899/Open-R1-Video)
 [![GitHub stars](https://img.shields.io/github/stars/Wang-Xiaodong1899/Open-R1-Video?style=social&label=GitHub&logo=github)](https://github.com/Wang-Xiaodong1899/Open-R1-Video)

![Open R1 Video](assets/image-20250620102641966.png)

---

#### Video-R1: Reinforcing Video Reasoning in MLLMs

[![arXiv](https://img.shields.io/badge/arXiv-2503.21776-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2503.21776)
[![Zhihu](https://img.shields.io/badge/Zhihu-解读-informational?logo=zhihu)](https://zhuanlan.zhihu.com/p/1889342435928282728)
[![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://github.com/tulerfeng/Video-R1)
 [![GitHub stars](https://img.shields.io/github/stars/tulerfeng/Video-R1?style=social&label=GitHub&logo=github)](https://github.com/tulerfeng/Video-R1)

![Video-R1](assets/image-20250620102641966.png)

---

#### VideoChat-R1: Enhancing Spatio-Temporal Perception via Reinforcement Fine-Tuning

[![arXiv](https://img.shields.io/badge/arXiv-2504.06958-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2504.06958)
[![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://github.com/OpenGVLab/VideoChat-R1)
 [![GitHub stars](https://img.shields.io/github/stars/OpenGVLab/VideoChat-R1?style=social&label=GitHub&logo=github)](https://github.com/OpenGVLab/VideoChat-R1)

![VideoChat-R1](assets/image-20250620144735572.png)

---

#### TinyLLaVA-Video-R1: Towards Smaller LMMs for Video Reasoning

[![arXiv](https://img.shields.io/badge/arXiv-2504.09641-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2504.09641)
[![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://github.com/ZhangXJ199/TinyLLaVA-Video-R1)
 [![GitHub stars](https://img.shields.io/github/stars/ZhangXJ199/TinyLLaVA-Video-R1?style=social&label=GitHub&logo=github)](https://github.com/ZhangXJ199/TinyLLaVA-Video-R1)

![TinyLLaVA-Video-R1](assets/image-20250620103826723.png)

---

### Tool Usage (Non-Visual)

TOOLLLM: FACILITATING LARGE LANGUAGE MODELS TO MASTER 16000+ REAL-WORLD APIS <sup><kbd>ICLR 2024</kbd></sup> [![OpenReview](https://img.shields.io/badge/OpenReview-Link-green?logo=openreview)](https://openreview.net/forum?id=dHng2O0Jjr)

REACT: SYNERGIZING REASONING AND ACTING IN LANGUAGE MODELS (ICLR 2023) [[arXiv](https://arxiv.org/pdf/2210.03629)]

---

## 🖼️ Thinking with Image

[![Wiki](https://img.shields.io/badge/Wiki-Visual%20Thinking-blue?logo=wikipedia)](https://en.wikipedia.org/wiki/Visual_thinking)
[![OpenAI](https://img.shields.io/badge/OpenAI-Thinking%20with%20Images-9cf?logo=openai)](https://openai.com/index/thinking-with-images/)

[![Guide](https://img.shields.io/badge/Guide-Embodied--AI--Guide-brightgreen?logo=github)](https://github.com/TianxingChen/Embodied-AI-Guide)
[![Qwen-Agent](https://img.shields.io/badge/Industry-Qwen--Agent-blueviolet?logo=github)](https://github.com/QwenLM/Qwen-Agent/tree/main)

### Collections (合集)

[![Awesome_Think_With_Images](https://img.shields.io/badge/Awesome-Think_With_Images-black?logo=github)](https://github.com/zhaochen0110/Awesome_Think_With_Images)
[![Awesome-Thinking-With-Images](https://img.shields.io/badge/Awesome-Thinking_With_Images-black?logo=github)](https://github.com/ligeng0197/Awesome-Thinking-With-Images)
[![Awesome-Anomaly-Detection-Foundation-Models](https://img.shields.io/badge/Awesome-Anomaly_Detection_Foundation_Models-black?logo=github)](https://github.com/mala-lab/Awesome-Anomaly-Detection-Foundation-Models/tree/main?tab=readme-ov-file)
[![Awesome-LLM4AD](https://img.shields.io/badge/Awesome-LLM4AD-black?logo=github)](https://github.com/Thinklab-SJTU/Awesome-LLM4AD)

[![PAPO](https://img.shields.io/badge/GRPO%E6%94%B9%E8%BF%9B-PAPO-orange?logo=github)](https://github.com/MikeWangWZHL/PAPO)

### To Sort (待整理)

[![HyperCLIP](https://img.shields.io/badge/To--Sort-HyperCLIP-lightgrey?logo=github)](https://github.com/SJTU-DeepVisionLab/HyperCLIP)
[![TreeVGR](https://img.shields.io/badge/To--Sort-TreeVGR-lightgrey?logo=github)](https://github.com/Haochen-Wang409/TreeVGR)
[![HyperVD](https://img.shields.io/badge/To--Sort-HyperVD-lightgrey?logo=github)](https://github.com/xiaogangpeng/HyperVD)

[![PyVision arXiv](https://img.shields.io/badge/PyVision-arXiv-ff69b4?logo=arxiv)](https://arxiv.org/pdf/2507.07998) [![PyVision Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://agent-x.space/pyvision/)

[![Data-Juicer arXiv](https://img.shields.io/badge/Data--Juicer-arXiv-ff69b4?logo=arxiv)](https://arxiv.org/pdf/2407.11784) [![Data-Juicer Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://modelscope.github.io/data-juicer/en/main/docs/awesome_llm_data.html)

### Curiosity-driven Learning

Humans monitor learning progress in curiosity-driven exploration (NC 2021) [[paper](https://www.nature.com/articles/s41467-021-26196-w)]

Curiosity-driven Exploration by Self-supervised Prediction (PMLR 2017) [[paper](https://proceedings.mlr.press/v70/pathak17a/pathak17a.pdf)]

Computational mechanisms of curiosity and goal-directed exploration (Neuroscience 2019) [[paper](https://elifesciences.org/articles/41703)]

### Foundation Models & Theory (基础模型/理论)

d1: Scaling Reasoning in Diffusion Large Language Models via Reinforcement Learning [![arXiv](https://img.shields.io/badge/arXiv-2504.12216-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2504.12216)

Hyperbolic Safety-Aware Vision-Language Models <sup><kbd>CVPR 2025</kbd></sup> [![GitHub stars](https://img.shields.io/github/stars/aimagelab/HySAC?style=social&label=GitHub&logo=github)](https://github.com/aimagelab/HySAC) [![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://aimagelab.github.io/HySAC/)

<img src="assets/hysac-method.png" width="400"/>

LSNet: See Large, Focus Small [![arXiv](https://img.shields.io/badge/arXiv-2503.23135-b31b1b?logo=arxiv)](https://arxiv.org/abs/2503.23135) [![GitHub stars](https://img.shields.io/github/stars/THU-MIG/lsnet?style=social&label=GitHub&logo=github)](https://github.com/THU-MIG/lsnet)

A Stitch in Time Saves Nine: Small VLM is a Precise Guidance for accelerating Large VLMs <sup><kbd>CVPR 2025</kbd></sup> [![GitHub stars](https://img.shields.io/github/stars/NUS-HPC-AI-Lab/SGL?style=social&label=GitHub&logo=github)](https://github.com/NUS-HPC-AI-Lab/SGL)

**VLsI**: **V**erbalized **L**ayer**s**-to-**I**nteractions from Large to Small Vision Language Models [![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://byungkwanlee.github.io/VLsI-page/) [![arXiv](https://img.shields.io/badge/arXiv-2412.01822-b31b1b?logo=arxiv)](https://arxiv.org/abs/2412.01822)

Boltzmann Attention Sampling for Image Analysis with Small Objects <sup><kbd>CVPR 2025</kbd></sup> [![arXiv](https://img.shields.io/badge/arXiv-2503.02841-b31b1b?logo=arxiv)](https://arxiv.org/abs/2503.02841) [![GitHub stars](https://img.shields.io/github/stars/microsoft/BoltzFormer?style=social&label=GitHub&logo=github)](https://github.com/microsoft/BoltzFormer)

EntitySeg Toolbox: Towards open-world and high-quality image segmentation <sup><kbd>ICCV 2023</kbd></sup> [![GitHub stars](https://img.shields.io/github/stars/qqlu/Entity?style=social&label=GitHub&logo=github)](https://github.com/qqlu/Entity) [![Paper](https://img.shields.io/badge/Paper-ICCV2023-blue)](https://openaccess.thecvf.com/content/ICCV2023/papers/Qi_High_Quality_Entity_Segmentation_ICCV_2023_paper.pdf)

### Image Manipulation (图像操作)

**Instruction-Guided Visual Masking** [[paper](https://arxiv.org/pdf/2405.19783)] [[code](https://github.com/2toinf/IVM)]

plug-and-play 模块，通过mask不相关区域，从而使得大模型获得更好的理解

<img src="assets/image-20250620101110725.png" width="400"/>

**COGCOM: A VISUAL LANGUAGE MODEL WITH CHAIN-OF-MANIPULATIONS REASONING** [[paper](https://arxiv.org/pdf/2402.04236)] [[code](https://github.com/THUDM/CogCoM)]

操作链、内在操作（如定位、放大）并产生中间结果（如边框、图像片段）

<img src="assets/image-20250620101001450.png" width="400"/>

Number it: Temporal Grounding Videos like Flipping Manga <sup><kbd>CVPR 2025</kbd></sup> [![arXiv](https://img.shields.io/badge/arXiv-2411.10332-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2411.10332)

<img src="assets/image-20250623093048591.png" width="400"/>

### Video Anomaly Understanding

（此处省略部分内容，详见 think-with-image.md 原文，可根据需要补充）

### Datasets (数据集)

shanghaitech-anomaly-detection [[project](https://svip-lab.github.io/dataset/campus_dataset.html)]

[UCF-Crime](https://www.crcv.ucf.edu/research/real-world-anomaly-detection-in-surveillance-videos/) Real-world Anomaly Detection in Surveillance Videos

Multi-Scenario Anomaly Detection (MSAD) Dataset <sup><kbd>NeurIPS 2024</kbd></sup> [![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://msad-dataset.github.io/) [![arXiv](https://img.shields.io/badge/arXiv-2402.04857-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2402.04857)

---

## 🤖 Thinking with Action

### Embodied Intelligence (具身智能)

#### Embodied-Reasoner: Synergizing Visual Search, Reasoning, and Action for Embodied Interactive Tasks

[![arXiv](https://img.shields.io/badge/arXiv-2503.21696-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2503.21696v1)
[![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://embodied-reasoner.github.io/)
[![GitHub stars](https://img.shields.io/github/stars/zwq2018/embodied_reasoner?style=social&label=GitHub&logo=github)](https://github.com/zwq2018/embodied_reasoner)

![Embodied-Reasoner](assets/image-20250620115046795.png)

---

#### Reason-RFT: Reinforcement Fine-Tuning for Visual Reasoning

[![arXiv](https://img.shields.io/badge/arXiv-2503.20752-b31b1b?logo=arxiv)](https://arxiv.org/abs/2503.20752)
[![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://tanhuajie.github.io/ReasonRFT/)
[![GitHub stars](https://img.shields.io/github/stars/tanhuajie/Reason-RFT?style=social&label=GitHub&logo=github)](https://github.com/tanhuajie/Reason-RFT)

![Reason-RFT](assets/teaser.png)

---

#### Think Small, Act Big: Primitive Prompt Learning for Lifelong Robot Manipulation

[![CVPR 2025](https://img.shields.io/badge/CVPR2025-Paper-blueviolet?logo=opencv)](https://openaccess.thecvf.com/content/CVPR2025/papers/Yao_Think_Small_Act_Big_Primitive_Prompt_Learning_for_Lifelong_Robot_CVPR_2025_paper.pdf)

![Think Small, Act Big](assets/image-20250630111854316.png)

---

#### OpenFly: A Versatile Toolchain and Large-scale Benchmark for Aerial Vision-Language Navigation

[![Project](https://img.shields.io/badge/Project-blue?logo=safari)](https://shailab-ipec.github.io/openfly/)

![OpenFly](assets/toolchain.png)

---

#### SAM-R1: Leveraging SAM for Reward Feedback in Multimodal Segmentation via RL

[![arXiv](https://img.shields.io/badge/arXiv-2505.22596-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2505.22596)

![SAM-R1](assets/image-20250630112453520.png)

---

#### Visual-RFT: Visual Reinforcement Fine-Tuning

[![arXiv](https://img.shields.io/badge/arXiv-2503.01785-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2503.01785)
[![GitHub stars](https://img.shields.io/github/stars/Liuziyu77/Visual-RFT?style=social&label=GitHub&logo=github)](https://github.com/Liuziyu77/Visual-RFT)

![Visual-RFT](assets/image-20250630104729762.png)

---

#### Visual Planning: Let's Think Only with Images

[![arXiv](https://img.shields.io/badge/arXiv-2505.11409-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2505.11409)   [![GitHub stars](https://img.shields.io/github/stars/yix8/VisualPlanning?style=social&label=GitHub&logo=github)](https://github.com/yix8/VisualPlanning)

![Visual Planning](assets/image-20250630105040047.png)

---

#### AgentThink: A Unified Framework for Tool-Augmented Chain-of-Thought Reasoning in Vision-Language Models for Autonomous Driving

[![arXiv](https://img.shields.io/badge/arXiv-2505.15298-b31b1b?logo=arxiv)](https://arxiv.org/pdf/2505.15298)

![AgentThink](assets/image-20250725211337583.png)

---

## 🤝 Contributing

Contributions are welcome! Please submit a pull request to add papers, code, or resources.

---

<!-- 快捷访问按钮区 -->
<p align="center">
  <a href="https://github.com/ligeng0197/Awesome-Thinking-With-Images/issues"><img src="https://img.shields.io/badge/Issues-Track-orange"></a>
  <a href="https://github.com/ligeng0197/Awesome-Thinking-With-Images/pulls"><img src="https://img.shields.io/badge/Pull%20Requests-Welcome-brightgreen"></a>
  <a href="https://github.com/ligeng0197/Awesome-Thinking-With-Images/commits/main"><img src="https://img.shields.io/badge/Commits-Main-blue"></a>
  <a href="https://github.com/ligeng0197/Awesome-Thinking-With-Images/graphs/contributors"><img src="https://img.shields.io/badge/Contributors-Graph-ffaa00"></a>
</p>

---

