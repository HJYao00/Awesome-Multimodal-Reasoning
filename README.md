# Awesome-Multimodal-Reasoning

**Contributions are most welcome**, if you have any suggestions or improvements, feel free to create an issue or raise a pull request.

## Contents
 - [Benchmark](#benchmark)
 - [Model](#model)
    - [Image MLLM](#image-mllm)
    - [Video MLLM](#video-mllm)
    - [Image Generation](#image-generation)
    - [LLM](#llm)
 - [Data](#data)

## Benchmark



| Date  | Project                                                      | Task                                     |
| ----- | ------------------------------------------------------------ | ---------------------------------------- |
| 24.05 | M3CoT: A Novel Benchmark for Multi-Domain Multi-step Multi-modal Chain-of-Thought [[📑Paper]](https://arxiv.org/html/2405.16473v1) | M3CoT                                    |
| 24.10 | MME-CoT: Benchmarking Chain-of-Thought in LMMs for Reasoning Quality, Robustness, and Efficiency [[📑Paper]](https://arxiv.org/pdf/2410.16198)[[🖥️Code]](https://github.com/CaraJ7/MME-CoT) | MME-CoT                                  |
| 24.11 | VLRewardBench: A Challenging Benchmark for Vision-Language Generative Reward Models [[📑Paper]](https://arxiv.org/abs/2411.17451) | VLRewardBench                            |
| 25.01 | LlamaV-o1: Rethinking Step-By-Step Visual Reasoning in LLMs [[📑Paper]](https://arxiv.org/abs/2501.06186)[[🖥️Code]](https://github.com/mbzuai-oryx/LlamaV-o1) | VRCBench                                 |
| 25.02 | OmniAlign-V: Towards Enhanced Alignment of MLLMs with Human Preference [[📑Paper]](https://arxiv.org/abs/2502.18411)[[🖥️Code]](https://github.com/PhoenixZ810/OmniAlign-V) | MM-AlignBench                            |
| 25.02 | MM-RLHF: The Next Step Forward in Multimodal LLM Alignment [[📑Paper]](https://arxiv.org/abs/2502.10391) | MM-RLHF-RewardBench, MM-RLHF-SafetyBench |

## Model

### Image MLLM

| Date             | Project                                                      | SFT                                                  | RL                                                           | Task                                                         |
| ---------------- | ------------------------------------------------------------ | ---------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 24.12            | Mulberry: Empowering MLLM with o1-like Reasoning and Reflection via Collective Monte Carlo Tree Search [[📑Paper]](https://arxiv.org/abs/2412.18319)[[🖥️Code]](https://github.com/HJYao00/Mulberry) | 260k reasoning and reflection sft data by CoMCTS                          |-                                                          | Various VQA                                                  |
| 24.03            | Visual CoT: Advancing Multi-Modal Language Models with a Comprehensive Dataset and Benchmark for Chain-of-Thought Reasoning [[📑Paper]](https://proceedings.neurips.cc/paper_files/paper/2024/file/0ff38d72a2e0aa6dbe42de83a17b2223-Paper-Datasets_and_Benchmarks_Track.pdf)[[🖥️Code]](https://github.com/deepcs233/Visual-CoT) | visual chain-of-thought dataset comprising 438k data items                          |-                                                          | Various VQA                                                  |
| 24.10            | Improve Vision Language Model Chain-of-thought Reasoning [[📑Paper]](https://arxiv.org/pdf/2410.16198)[[🖥️Code]](https://github.com/RifleZhang/LLaVA-Reasoner-DPO) | 193k CoT sft data by GPT4-o                          | DPO                                                          | Various VQA                                                  |
| 24.11            | LLaVA-CoT: Let Vision Language Models Reason Step-by-Step [[📑Paper]](https://arxiv.org/abs/2411.10440)[[🖥️Code]](https://github.com/PKU-YuanGroup/LLaVA-CoT) | LLaVA-CoT-100k by GPT4-o                             | -                                                            | Various VQA                                                  |
| 24.11            | Insight-V: Exploring Long-Chain Visual Reasoning with Multimodal Large Language Models [[📑Paper]](https://arxiv.org/abs/2411.14432)[[🖥️Code]](https://github.com/dongyh20/Insight-V) | sft for agent                                        | Iterative DPO                                                | Various VQA                                                  |
| 24.11            | Enhancing the Reasoning Ability of Multimodal Large Language Models via Mixed Preference Optimization [[📑Paper]](https://arxiv.org/abs/2411.10442) | -                                                    | MPO                                                          | Various VQA                                                  |
| 25.01            | Virgo: A Preliminary Exploration on Reproducing o1-like MLLM [[📑Paper]](https://arxiv.org/abs/2501.01904)[[🖥️Code]](https://github.com/RUCAIBox/Virgo) | 2k Text data from R1/QwQ and visual data from QvQ/SD | -                                                            | Math & MMMU                                                  |
| 25.01            | InternLM-XComposer2.5-Reward: A Simple Yet Effective Multi-Modal Reward Model [[📑Paper]](https://arxiv.org/abs/2501.12368)[[🖥️Code]](https://github.com/InternLM/InternLM-XComposer) | -                                                    | PPO                                                          | Reward & Various VQA                                         |
| 25.01            | LlamaV-o1: Rethinking Step-By-Step Visual Reasoning in LLMs [[📑Paper]](https://arxiv.org/abs/2501.06186)[[🖥️Code]](https://github.com/mbzuai-oryx/LlamaV-o1) | LLaVA-CoT-100k & PixMo [13] subset                   | -                                                            | VRC-Bench & Various VQA                                      |
| 25.02            | MM-RLHF: The Next Step Forward in Multimodal LLM Alignment [[📑Paper]](https://arxiv.org/abs/2502.10391)[[🖥️Code]](https://mm-rlhf.github.io/) | -                                                    | DPO with 120k fine-grained, human-annotated preference comparison pairs. | Reward & Various VQA                                         |
| 25.02            | OmniAlign-V: Towards Enhanced Alignment of MLLMs with Human Preference [[📑Paper]](https://arxiv.org/abs/2502.18411)[[🖥️Code]](https://github.com/PhoenixZ810/OmniAlign-V) | 200k sft data                                        | DPO                                                          | Alignment & Various VQA                                      |
| 25.02            | Multimodal Open R1 [[🖥️Code]](https://github.com/EvolvingLMMs-Lab/open-r1-multimodal) | -                                                    | GRPO                                                         | Mathvista-mini, MMMU                                         |
| 25.02            | VLM-R1: A stable and generalizable R1-style Large Vision-Language Model [[🖥️Code]](https://github.com/om-ai-lab/VLM-R1/tree/main?tab=readme-ov-file) | -                                                    | GRPO                                                         | Referring Expression Comprehension                           |
| 25.02            | R1-V: Reinforcing Super Generalization Ability in Vision Language Models with Less Than $3 [[🖥️Code]](https://github.com/Deep-Agent/R1-V) | -                                                    | GRPO                                                         | Item Counting, Number Related Reasoning and Geometry Reasoning |
| 25.03            | EasyR1: An Efficient, Scalable, Multi-Modality RL Training Framework [[🖥️Code]](https://github.com/hiyouga/EasyR1) | -                                                    | GRPO                                                         | Geometry3K                                                   |
| 25.03            | Unified Reward Model for Multimodal Understanding and Generation [[📑Paper]](https://arxiv.org/abs/2503.05236)[[🖥️Code]](https://codegoat24.github.io/UnifiedReward/) | -                                                    | DPO                                                          | Various VQA & Generation                                     |
| 25.03            | MM-EUREKA: Exploring Visual Aha Moment with Rule-based Large-scale Reinforcement Learning [[📑Paper]](https://arxiv.org/abs/2503.07365)[[🖥️Code]](https://github.com/ModalMinds/MM-EUREKA) | -                                                    | RLOO                                                         | Math                                                         |
| 25.03            | R1-Zero’s “Aha Moment” in Visual Reasoning on a 2B Non-SFT Model [[📑Paper]](https://arxiv.org/abs/2503.05132)[[🖥️Code]](https://github.com/turningpoint-ai/VisualThinker-R1-Zero) | -                                                    | GRPO                                                         | CVBench                                                      |
| 25.03            | Seg-Zero: Reasoning-Chain Guided Segmentation via Cognitive Reinforcement [[📑Paper]](https://arxiv.org/abs/2503.06520)[[🖥️Code]](https://github.com/dvlab-research/Seg-Zero) | -                                                    | GRPO                                                         | RefCOCO&ReasonSeg                                            |
| 25.03            | Vision-R1: Incentivizing Reasoning Capability in Multimodal Large Language Models [[📑Paper]](https://arxiv.org/abs/2503.06749)[[🖥️Code]](https://github.com/Osilly/Vision-R1) | -                                                    | GRPO                                                         | Math                                                         |
| 25.03            | Boosting the Generalization and Reasoning of Vision Language Models with Curriculum Reinforcement Learning [[📑Paper]](https://arxiv.org/pdf/2503.07065) | Self-Improvement Training                            | GRPO                                                         | Detection, Classification, Math                              |
| 25.03            | LMM-R1: Empowering 3B LMMs with Strong Reasoning Abilities Through Two-Stage Rule-Based RL [[📑Paper]](https://link.zhihu.com/?target=https%3A//arxiv.org/pdf/2503.07536)[[🖥️Code]](https://github.com/TideDra/lmm-r1) | -                                                    | PPO                                                          | Math, Sokoban-Global, Football-Online                        |
| 25.03            | Visual-RFT: Visual Reinforcement Fine-Tuning [[📑Paper]](https://arxiv.org/abs/2503.01785)[[🖥️Code]](https://github.com/Liuziyu77/Visual-RFT) | -                                                    | GRPO                                                         | Detection, Grounding, Classification                         |
| 25.03            | VisRL: Intention-Driven Visual Perception via Reinforced Reasoning [[📑Paper]](https://arxiv.org/pdf/2503.07523)[[🖥️Code]](https://github.com/zhangquanchen/VisRL) | warm up                                              | DPO                                                          | Various VQA                                                  |
| 25.03 (CVPR2025) | GFlowVLM: Enhancing Multi-step Reasoning in Vision-Language Models with Generative Flow Networks [[📑Paper]](https://arxiv.org/pdf/2503.06514) | -                                                    | GFlowNets                                                    | NumberLine (NL) and BlackJack (BJ)                           |
| 25.03            | MMR1: Advancing the Frontiers of Multimodal Reasoning [[🖥️Code]](https://github.com/LengSicong/MMR1) | -                                                    | GRPO                                                         | Math                                                         |
| 25.03            | R1-Onevision: Advancing Generalized Multimodal Reasoning through Cross-Modal Formalization [[📑Paper]](https://yangyi-vai.notion.site/r1-onevision)[[🖥️Code]](https://github.com/Fancy-MLLM/R1-Onevision) | ongoing                                              | ongoing                                                      | ongoing                                                      |

### Video MLLM

| Date  | Project                                                      | SFT           | RL   | Task                |
| ----- | ------------------------------------------------------------ | ------------- | ---- | ------------------- |
| 25.01 | Temporal Preference Optimization for Long-Form Video Understanding [[📑Paper]](https://arxiv.org/abs/2501.13919)[[🖥️Code]](https://ruili33.github.io/tpo_website/) | -             | DPO  | various video QA    |
| 25.01 | Tarsier2: Advancing Large Vision-Language Models from Detailed Video Description to Comprehensive Video Understanding [[📑Paper]](https://arxiv.org/abs/2501.07888)[[🖥️Code]]() | main training | DPO  | Video caption & QA  |
| 25.02 | video-SALMONN-o1: Reasoning-enhanced Audio-visual Large Language Model [[📑Paper]](https://arxiv.org/abs/2502.11775) | cold start    | DPO  | various video QA    |
| 25.02 | Open-R1-Video[[🖥️Code]](https://github.com/Wang-Xiaodong1899/Open-R1-Video) | -             | GRPO | LongVideoBench      |
| 25.02 | Video-R1: Towards Super Reasoning Ability in Video Understanding [[🖥️Code]](https://github.com/tulerfeng/Video-R1) | -             | GRPO | DVD-counting        |
| 25.03 | R1-Omni: Explainable Omni-Multimodal Emotion Recognition with Reinforcement Learning [[📑Paper]](https://arxiv.org/abs/2503.05379)[[🖥️Code]](https://github.com/HumanMLLM/R1-Omni) | cold start    | GRPO | Emotion recognition |

### Image/Video Generation

| Date  | Proj                                                                                                                          | Comment                                                    |
| ----- | ----------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| 25.02 | [C-Drag:Chain-of-Thought Driven Motion Controller for Video Generation](https://arxiv.org/pdf/2502.19868)                     | Calculate simple motion vector with LLM.                   |
| 25.01 | [Can We Generate Images with CoT? Let's Verify and Reinforce Image Generation Step by Step](https://arxiv.org/pdf/2501.13926) | Potential Assessment Reward Model for AR Image Generation. |
| 25.01 | [Imagine while Reasoning in Space: Multimodal Visualization-of-Thought](https://arxiv.org/pdf/2501.07542)                     | Visualization-of-Thought                                   |
| 25.01 | [ReFocus: Visual Editing as a Chain of Thought for Structured Image Understanding](https://arxiv.org/pdf/2501.05452)          | Draw something!                                            |
| 24.12 | [EVLM: Self-Reflective Multimodal Reasoning for Cross-Dimensional Visual Editing](https://arxiv.org/pdf/2412.10566)           | Thinking in text space with a caption model.               |



### LLM

| Date | Project                                                      | Comment |
| ---- | ------------------------------------------------------------ | ------- |
|      | Multimodal Chain-of-Thought Reasoning in Language Models [[🖥️Code]](https://github.com/amazon-science/mm-cot) |         |



## Data
| Date  | Project                                                      | Comment          |
| ----- | ------------------------------------------------------------ | ---------------- |
| 24.11 | VideoEspresso: A Large-Scale Chain-of-Thought Dataset for Fine-Grained  Video Reasoning via Core Frame Selection[[📑Paper\]](https://arxiv.org/abs/2411.14794)[[🖥️Code\]](https://github.com/hshjerry/VideoEspresso) | various video QA |
| 25.03 | Integrating Chain-of-Thought for Multimodal Alignment: A Study on 3D Vision-Language Learning[[📑Paper\]](https://arxiv.org/pdf/2503.06232)[[Data\]]() | 3D-CoT Benchmark |

