# Awesome-RLOps

<a id="our-survey"></a>

## Our Survey

Our survey organizes LLM RLOps around Training Setup, Experience Collection, Reward Computation, Policy Optimization, and Model Evaluation. It connects resource and execution management with feedback reliability, learning stability, failure recovery, and validation of training outcomes.

<a id="taxonomy"></a>

## Taxonomy

- [Training Setup](#training-setup)
  - [Computational Resources](#computational-resources)
  - [Run Configuration](#run-configuration)
  - [Base Model](#base-model)
  - [Training Data](#training-data)
- [Experience Collection](#experience-collection)
  - [Sampling Budget Control](#sampling-budget-control)
  - [Rollout Execution Optimization](#rollout-execution-optimization)
  - [Environment Reliability](#environment-reliability)
  - [Trajectory Lifecycle Management](#trajectory-lifecycle-management)
- [Reward Computation](#reward-computation)
  - [Learned Evaluators](#learned-evaluators)
  - [Programmatic Verifiers](#programmatic-verifiers)
  - [Reward Signals](#reward-signals)
- [Policy Optimization](#policy-optimization)
  - [Update Execution](#update-execution)
  - [Policy Consistency](#policy-consistency)
  - [Learning Stability](#learning-stability)
  - [Training Recovery](#training-recovery)
- [Model Evaluation](#model-evaluation)
  - [Capability Validation](#capability-validation)
  - [Risk Auditing](#risk-auditing)
  - [Version Acceptance](#version-acceptance)
- [Open-source Resources](#open-source-resources)
- [Related Surveys](#related-surveys)
- [Citation](#citation)

Papers are indexed by their main operational contribution; a system may contribute to several topics. Entries are ordered by venue year, newest first, or preprint year when no formal venue is confirmed. Venue links point to publication or acceptance evidence; workshop and special-track papers are labeled explicitly. In the Code column, `Pending` denotes an announced release that is not yet available, and — means no accessible official implementation was verified. Component-only releases are labeled by scope.

<a id="training-setup"></a>

## Training Setup

Prepare resources, configuration, the starting model, and training inputs.

41 papers

<a id="computational-resources"></a>

### Computational Resources

Estimate resource demand, predict compute returns, and allocate training budgets.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [ECHO-2: A Large-Scale Distributed Rollout Framework for Cost-Efficient Reinforcement Learning](https://arxiv.org/abs/2602.02192) | [NeurIPS 2026 (accepted)](https://arxiv.org/abs/2602.02192) | — |
| [IsoCompute Playbook: Optimally Scaling Sampling Compute for LLM RL](https://arxiv.org/abs/2603.12151) | [ICML 2026](https://proceedings.mlr.press/v306/cheng26n.html) | — |
| [On Effectiveness and Efficiency of Agentic Tool-calling and RL Training](https://arxiv.org/abs/2606.00135) | [ICML 2026](https://proceedings.mlr.press/v306/liu26de.html) | — |
| [Scaling Behaviors of LLM Reinforcement Learning Post-Training: An Empirical Study in Mathematical Reasoning](https://arxiv.org/abs/2509.25300) | [ACL 2026](https://aclanthology.org/2026.acl-long.1444/) | [![GitHub](https://img.shields.io/github/stars/tanzelin430/The-Scaling-Law-for-Reinforcement-Learning?style=flat&label=GitHub)](https://github.com/tanzelin430/The-Scaling-Law-for-Reinforcement-Learning) |
| [sGPO: Trading Inference FLOPs for Training Efficiency in RLVR](https://arxiv.org/abs/2606.08854) | arXiv 2026 | — |
| [The Art of Scaling Reinforcement Learning Compute for LLMs](https://arxiv.org/abs/2510.13786) | [ICLR 2026](https://proceedings.iclr.cc/paper_files/paper/2026/hash/75ea88aca02640cca54c1231db8cacdd-Abstract-Conference.html) | — |
| [The Rollout Infrastructure Tax in Coding-Agent Reinforcement Learning](https://arxiv.org/abs/2607.01415) | arXiv 2026 | — |
| [Agent RL Scaling Law: Agent RL with Spontaneous Code Execution for Mathematical Problem Solving](https://arxiv.org/abs/2505.07773) | [NeurIPS 2025](https://proceedings.neurips.cc/paper_files/paper/2025/hash/0adea62f2f98c5035aded00d4b2064e6-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/yyht/openrlhf_async_pipline?style=flat&label=GitHub)](https://github.com/yyht/openrlhf_async_pipline) |
| [Predictive Scaling Laws for Efficient GRPO Training of Large Reasoning Models](https://arxiv.org/abs/2507.18014) | arXiv 2025 | — |
| [Does RLHF Scale? Exploring the Impacts From Data, Model, and Method](https://arxiv.org/abs/2412.06000) | arXiv 2024 | — |

<a id="run-configuration"></a>

### Run Configuration

Compare, search, and validate executable training configurations.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [AlignTune: Modular Toolkit for Post-Training Alignment of Large Language Models](https://arxiv.org/abs/2602.09621) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/Lexsi-Labs/aligntune?style=flat&label=GitHub)](https://github.com/Lexsi-Labs/aligntune) |
| [Automatic Configuration of LLM Post-Training Pipelines](https://arxiv.org/abs/2603.18773) | [EMNLP 2026](https://aclanthology.org/2026.emnlp-main.2324/) | — |
| [Efficient Hyperparameter Optimization for LLM Reinforcement Learning](https://arxiv.org/abs/2606.03073) | [ACL 2026](https://aclanthology.org/2026.acl-long.1271/) | — |
| [How Much Online RL is Enough? Informative Rollouts for Offline Preference Optimization in RLVR](https://arxiv.org/abs/2605.21266) | arXiv 2026 | — |
| [MemFactory: Unified Inference & Training Framework for Agent Memory](https://arxiv.org/abs/2603.29493) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/MemTensor/MemFactory?style=flat&label=GitHub)](https://github.com/MemTensor/MemFactory) |
| [NebulaExp-8B: An Empirical Post-Training Pipeline via Full-Scale Ablation Research](https://arxiv.org/abs/2606.26671) | arXiv 2026 | — |
| [Towards Robust Reinforcement Learning for Small-Scale Language Model Agents](https://arxiv.org/abs/2607.25091) | [IEEE SMC 2026](https://arxiv.org/abs/2607.25091) | [![GitHub](https://img.shields.io/github/stars/rezwanh001/SLM-RL-Agents?style=flat&label=GitHub)](https://github.com/rezwanh001/SLM-RL-Agents) |
| [UnityMAS-O: A General RL Optimization Framework for LLM-Based Multi-Agent Systems](https://arxiv.org/abs/2605.26646) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/chenyiqun/UnityMAS-O?style=flat&label=GitHub)](https://github.com/chenyiqun/UnityMAS-O) |
| [When Do Larger Batches Help Scale LLM Reinforcement Learning?](https://arxiv.org/abs/2608.29296) | arXiv 2026 | — |
| [How to Train Your LLM Web Agent: A Statistical Diagnosis](https://arxiv.org/abs/2507.04103) | [NeurIPS 2025](https://proceedings.nips.cc/paper_files/paper/2025/hash/4d239452d41ded07139801d7c966c629-Abstract-Conference.html) | — |
| [JustRL: Scaling a 1.5B LLM with a Simple RL Recipe](https://arxiv.org/abs/2512.16649) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/thunlp/JustRL?style=flat&label=GitHub)](https://github.com/thunlp/JustRL) |
| [Nemotron-Cascade: Scaling Cascaded Reinforcement Learning for General-Purpose Reasoning Models](https://arxiv.org/abs/2512.13607) | arXiv 2025 | — |
| [Unpacking DPO and PPO: Disentangling Best Practices for Learning from Preference Feedback](https://arxiv.org/abs/2406.09279) | [NeurIPS 2024](https://papers.nips.cc/paper_files/paper/2024/hash/404df2480b6eef0486a1679e371894b0-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/hamishivi/EasyLM?style=flat&label=GitHub)](https://github.com/hamishivi/EasyLM) |

<a id="base-model"></a>

### Base Model

Select and prepare a model checkpoint suitable for the intended RL run.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Clipping Low-Probability Tokens in SFT Yields a Generalizable Initialization for RL](https://proceedings.mlr.press/v306/liu26bm.html) | [ICML 2026](https://proceedings.mlr.press/v306/liu26bm.html) | [![GitHub](https://img.shields.io/github/stars/LTSure/on-policy-cold-start?style=flat&label=GitHub)](https://github.com/LTSure/on-policy-cold-start) |
| [Good SFT Optimizes for SFT, Better SFT Prepares for Reinforcement Learning](https://arxiv.org/abs/2602.01058) | [ICML 2026](https://proceedings.mlr.press/v306/zhang26hd.html) | — |
| [Quagmires in SFT-RL Post-Training: When High SFT Scores Mislead and What to Use Instead](https://arxiv.org/abs/2510.01624) | [ICLR 2026](https://proceedings.iclr.cc/paper_files/paper/2026/hash/5d6ae8ba43ecb378030753c4408ef9bd-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/feiyang-k/SFT-RL-ICLR?style=flat&label=GitHub)](https://github.com/feiyang-k/SFT-RL-ICLR) |
| [SFT Overtraining Predicts Rank Inversion via Entropy Collapse Under RLVR](https://arxiv.org/abs/2606.18487) | [ICML 2026 (DL4C Workshop)](https://arxiv.org/abs/2606.18487) | [![GitHub](https://img.shields.io/github/stars/siddharthaphale/entropy-collapse-rlvr?style=flat&label=GitHub)](https://github.com/siddharthaphale/entropy-collapse-rlvr) |
| [Teaching Thinking Models to Reason with Tools: A Full-Pipeline Recipe for Tool-Integrated Reasoning](https://arxiv.org/abs/2605.06326) | arXiv 2026 | — |
| [When RL Fails after SFT: Rejuvenating Model Plasticity for Robust SFT-to-RL Handoff](https://arxiv.org/abs/2606.09932) | arXiv 2026 | — |
| [SimpleRL-Zoo: Investigating and Taming Zero Reinforcement Learning for Open Base Models in the Wild](https://arxiv.org/abs/2503.18892) | [COLM 2025](https://arxiv.org/abs/2503.18892) | [![GitHub](https://img.shields.io/github/stars/hkust-nlp/simpleRL-reason?style=flat&label=GitHub)](https://github.com/hkust-nlp/simpleRL-reason) |

<a id="training-data"></a>

### Training Data

Select informative tasks, validate input quality, and allocate annotation effort.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Agent-World: Scaling Real-World Environment Synthesis for Evolving General Agent Intelligence](https://arxiv.org/abs/2604.18292) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/RUC-NLPIR/Agent-World?style=flat&label=GitHub)](https://github.com/RUC-NLPIR/Agent-World) |
| [DE-Venus: A Data-Efficient RLVR Framework for Large Language Models](https://arxiv.org/abs/2609.03324) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/ZJU-DIG/DE-Venus?style=flat&label=GitHub)](https://github.com/ZJU-DIG/DE-Venus) |
| [SCALECUA: Scaling Computer Use Agents with Verifiable Task Synthesis and Efficient Online RL](https://arxiv.org/abs/2607.11185) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/THUDM/SCALE-CUA?style=flat&label=GitHub)](https://github.com/THUDM/SCALE-CUA) |
| [Scaling Near-Optimal SFT-RL Annotation Budget Allocation from Small to Large LLMs](https://arxiv.org/abs/2609.01573) | [EMNLP 2026](https://arxiv.org/abs/2609.01573) | — |
| [Smart Picks in the Dark: Towards Efficient RLVR for Reasoning via Tracing Metacognitive Pivots](https://arxiv.org/abs/2606.04503) | [NeurIPS 2026 (accepted)](https://arxiv.org/abs/2606.04503) | [![GitHub](https://img.shields.io/github/stars/gczhu/PivotTrace?style=flat&label=GitHub)](https://github.com/gczhu/PivotTrace) |
| [Survive or Collapse: The Asymmetric Roles of Data Gating and Reward Grounding in Self-Play RL](https://arxiv.org/abs/2605.22217) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/UCSB-AI/self-play-data-gating?style=flat&label=GitHub)](https://github.com/UCSB-AI/self-play-data-gating) |
| [Teach the Way It Thinks: Guiding LLM Post-training Data Engineering with Sparse Autoencoders](https://arxiv.org/abs/2605.27354) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/THUAIS-Lab/SAERL?style=flat&label=GitHub)](https://github.com/THUAIS-Lab/SAERL) |
| [Towards High Data Efficiency in Reinforcement Learning with Verifiable Reward](https://arxiv.org/abs/2509.01321) | [ICLR 2026](https://proceedings.iclr.cc/paper_files/paper/2026/hash/374050dc3f211267bd6bf0ea24eae184-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/txy77/DEPO?style=flat&label=GitHub)](https://github.com/txy77/DEPO) |
| [INTELLECT-2: A Reasoning Model Trained Through Globally Decentralized Reinforcement Learning](https://arxiv.org/abs/2505.07291) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/PrimeIntellect-ai/prime-rl?style=flat&label=GitHub)](https://github.com/PrimeIntellect-ai/prime-rl) |
| [Truth in the Few: High-Value Data Selection for Efficient Multi-Modal Reasoning](https://arxiv.org/abs/2506.04755) | arXiv 2025 | [Pending](https://github.com/Leo-ssl/RAP) |
| [UFO-RL: Uncertainty-Focused Optimization for Efficient Reinforcement Learning Data Selection](https://arxiv.org/abs/2505.12457) | [NeurIPS 2025](https://proceedings.neurips.cc/paper_files/paper/2025/hash/010a19805b0159022a8b29d735bb545f-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/zy125413/UFO_RL?style=flat&label=GitHub)](https://github.com/zy125413/UFO_RL) |

[Back to taxonomy](#taxonomy)

<a id="experience-collection"></a>

## Experience Collection

Produce, execute, and manage the experience supplied to training.

124 papers

<a id="sampling-budget-control"></a>

### Sampling Budget Control

Select tasks, allocate rollout effort, and stop unproductive generation.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Apriel-Reasoner: RL Post-Training for General-Purpose and Efficient Reasoning](https://arxiv.org/abs/2604.02007) | arXiv 2026 | — |
| [BOTS: A Unified Framework for Bayesian Online Task Selection in LLM Reinforcement Finetuning](https://arxiv.org/abs/2510.26374) | [ICLR 2026](https://openreview.net/forum?id=rQXBw8fn3Z) | [![GitHub](https://img.shields.io/github/stars/agentscope-ai/Trinity-RFT?style=flat&label=GitHub)](https://github.com/agentscope-ai/Trinity-RFT/tree/main/examples/bots) |
| [Can Prompt Difficulty be Online Predicted for Accelerating RL Finetuning of Reasoning Models?](https://arxiv.org/abs/2507.04632) | [KDD 2026](https://doi.org/10.1145/3770854.3780263) | [![GitHub](https://img.shields.io/github/stars/thu-rllab/MoPPS?style=flat&label=GitHub)](https://github.com/thu-rllab/MoPPS) |
| [Cross-Epoch Adaptive Rollout Optimization for RL Post-Training](https://arxiv.org/abs/2606.05606) | arXiv 2026 | — |
| [DARTS: Distribution-Aware Active Rollout Trajectory Shaping for Accelerating LLM Reinforcement Learning](https://arxiv.org/abs/2605.30859) | [ICML 2026](https://proceedings.mlr.press/v306/wang26w.html) | [![GitHub](https://img.shields.io/github/stars/AFDWang/DARTS?style=flat&label=GitHub)](https://github.com/AFDWang/DARTS) |
| [Data-Efficient RLVR via Off-Policy Influence Guidance](https://arxiv.org/abs/2510.26491) | [ACL 2026](https://aclanthology.org/2026.acl-long.2141/) | [![GitHub](https://img.shields.io/github/stars/thu-coai/CROPI?style=flat&label=GitHub)](https://github.com/thu-coai/CROPI) |
| [Dual-Loop Self-Evolution via Verifiable Emotion Feedback for Multi-Turn Empathetic Dialogue](https://arxiv.org/abs/2608.10626) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/Jasvina/DualLoop-EmoRL?style=flat&label=GitHub)](https://github.com/Jasvina/DualLoop-EmoRL) |
| [Early Verdicts, Better Budgets: Sequential Adaptive Rollout Allocation for Compute-Efficient RLVR](https://arxiv.org/abs/2607.26253) | arXiv 2026 | — |
| [Efficient RLVR Scheduling via Graph-Structured Online Difficulty Estimation](https://arxiv.org/abs/2608.17941) | arXiv 2026 | — |
| [Efficient RLVR Training via Weighted Mutual Information Data Selection](https://arxiv.org/abs/2603.01907) | arXiv 2026 | — |
| [HarnessBandit: Joint Learnability-Transferability Scheduling for Multi-Harness Agentic Reinforcement Learning](https://arxiv.org/abs/2609.13739) | arXiv 2026 | — |
| [Kalman Meets Curriculum: Efficient Dynamic Prompt Selection for Adaptive RL Finetuning](https://arxiv.org/abs/2607.27610) | arXiv 2026 | — |
| [LEAP: Lean Environment-Feedback via Adaptive Pruning for Code RL in GPU Kernel Generation](https://arxiv.org/abs/2608.01804) | arXiv 2026 | — |
| [Learning as Reasoning Unfolds: Progressive Rollout Allocation for Efficient Reinforcement Learning](https://arxiv.org/abs/2607.22002) | arXiv 2026 | — |
| [Learning-Zone Energy: Online Data Selection for Efficient RL Post-Training](https://arxiv.org/abs/2605.17003) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/Stellaris167/LZE?style=flat&label=GitHub)](https://github.com/Stellaris167/LZE) |
| [LEEPS: Latent-Guided Explore-Exploit Prompt Sampling for Efficient RLVR in Large Language Models](https://arxiv.org/abs/2607.28077) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/ShuangLiangX/LEEPS?style=flat&label=GitHub)](https://github.com/ShuangLiangX/LEEPS) |
| [Optimizing What Policies Learn From: Recoverability-aware Rollout Intervention Learning](https://arxiv.org/abs/2608.05080) | arXiv 2026 | — |
| [PAIR: Pairwise-Aware Inclusion Reweighting for Adaptive Rollout Allocation in RLVR](https://arxiv.org/abs/2608.11368) | arXiv 2026 | — |
| [Prompt Curriculum Learning for Efficient LLM Post-Training](https://arxiv.org/abs/2510.01135) | [ICLR 2026](https://openreview.net/pdf/33b6a4fd2066a3c9dd58eb0b4ce0d887c1c8d102.pdf) | — |
| [Prune as You Generate: Online Rollout Pruning for Faster and Better RLVR](https://arxiv.org/abs/2603.24840) | [ACL 2026](https://aclanthology.org/2026.acl-long.632/) | [![GitHub](https://img.shields.io/github/stars/Hsu1023/ARRoL?style=flat&label=GitHub)](https://github.com/Hsu1023/ARRoL) |
| [Selective Rollout: Mid-Trajectory Termination for Multi-Sample Agent RL](https://arxiv.org/abs/2605.05802) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/zhiyuanZhai20/selective-rollout?style=flat&label=GitHub)](https://github.com/zhiyuanZhai20/selective-rollout) |
| [SENTINEL: Failure-Driven Reinforcement Learning for Training Tool-Using Language Model Agents](https://arxiv.org/abs/2606.12908) | arXiv 2026 | — |
| [Small Generalizable Prompt Predictive Models Can Steer Efficient RL Post-Training of Large Reasoning Models](https://arxiv.org/abs/2602.01970) | [ICML 2026](https://proceedings.mlr.press/v306/qu26f.html) | [![GitHub](https://img.shields.io/github/stars/thu-rllab/GPS?style=flat&label=GitHub)](https://github.com/thu-rllab/GPS) |
| [Spend Your Rollouts Where It Counts: Rollout Allocation for Group-Based RL Post-Training](https://arxiv.org/abs/2605.26606) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/databricks/pilot-commit?style=flat&label=GitHub)](https://github.com/databricks/pilot-commit) |
| [ThinkPrior: Zero-Rollout Difficulty Priors for Cold-Start Prompt Selection in RLVR](https://arxiv.org/abs/2609.09075) | arXiv 2026 | — |
| [TRACE: A Unified Rollout Budget Allocation Framework for Efficient Agentic Reinforcement Learning](https://arxiv.org/abs/2606.11119) | [EMNLP 2026](https://arxiv.org/abs/2606.11119) | — |
| [Train at Moving Edge: Online-Verified Prompt Selection for Efficient RL Training of Large Reasoning Model](https://arxiv.org/abs/2603.25184) | [NeurIPS 2026 (accepted)](https://arxiv.org/abs/2603.25184) | — |
| [Train Less, Learn More: Adaptive Efficient Rollout Optimization for Group-Based Reinforcement Learning](https://arxiv.org/abs/2602.14338) | arXiv 2026 | — |
| [Where to Spend Rollouts: Hit-Utility Optimal Rollout Allocation for Group-Based RLVR](https://arxiv.org/abs/2605.07114) | arXiv 2026 | — |
| [Act Only When It Pays: Efficient Reinforcement Learning for LLM Reasoning via Selective Rollouts](https://arxiv.org/abs/2506.02177) | [NeurIPS 2025](https://proceedings.neurips.cc/paper_files/paper/2025/hash/b42fb82fc3ffb88b872c4714f093875d-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/Infini-AI-Lab/GRESO?style=flat&label=GitHub)](https://github.com/Infini-AI-Lab/GRESO) |
| [OptPO: Optimal Rollout Allocation for Test-time Policy Optimization](https://arxiv.org/abs/2512.02882) | arXiv 2025 | — |
| [Reinforce-Ada: An Adaptive Sampling Framework under Non-linear RL Objectives](https://arxiv.org/abs/2510.04996) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/RLHFlow/Reinforce-Ada?style=flat&label=GitHub)](https://github.com/RLHFlow/Reinforce-Ada) |

<a id="rollout-execution-optimization"></a>

### Rollout Execution Optimization

Improve generation throughput, scheduling, and resource use.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Accelerating Long-Tail Generation in Synchronous RLHF Training via Adaptive Tensor Parallelism](https://arxiv.org/abs/2605.23945) | arXiv 2026 | — |
| [Accelerating RL Post-Training Rollouts via System-Integrated Speculative Decoding](https://arxiv.org/abs/2604.26779) | arXiv 2026 | — |
| [Beat the long tail: Distribution-Aware Speculative Decoding for RL Training](https://arxiv.org/abs/2511.13841) | [MLSys 2026](https://proceedings.mlsys.org/paper_files/paper/2026/hash/cbc4ab80cd77aa0eb87da062fbcddb46-Abstract-Conference.html) | — |
| [Breaking Entropy Bounds: Accelerating RL Training via MTP with Rejection Sampling](https://arxiv.org/abs/2606.12370) | arXiv 2026 | [Code PR](https://github.com/sgl-project/sglang/pull/26312) |
| [BubbleSpec: Turning Long-Tail Bubbles into Speculative Rollout Drafts for Synchronous Reinforcement Learning](https://arxiv.org/abs/2605.08862) | [ICML 2026](https://proceedings.mlr.press/v306/xu26bc.html) | — |
| [DORA: A Scalable Asynchronous Reinforcement Learning System for Language Model Training](https://arxiv.org/abs/2604.26256) | arXiv 2026 | — |
| [DynaResize: Runtime GPU Reallocation for Disaggregated LLM Post-Training](https://arxiv.org/abs/2607.22614) | arXiv 2026 | — |
| [EfficientRollout: System-Aware Self-Speculative Decoding for RL Rollouts](https://arxiv.org/abs/2606.18967) | [NeurIPS 2026 (accepted)](https://arxiv.org/abs/2606.18967) | [![GitHub](https://img.shields.io/github/stars/furiosa-ai/EfficientRollout?style=flat&label=GitHub)](https://github.com/furiosa-ai/EfficientRollout) |
| [FastGRPO: Accelerating Policy Optimization via Concurrency-aware Speculative Decoding and Online Draft Learning](https://arxiv.org/abs/2509.21792) | [ICLR 2026](https://proceedings.iclr.cc/paper_files/paper/2026/hash/61674667d642ae52f6bb281bea90ee29-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/yedaotian9/FastGRPO?style=flat&label=GitHub)](https://github.com/yedaotian9/FastGRPO) |
| [Heddle: A Distributed Orchestration System for Agentic RL Rollout](https://arxiv.org/abs/2603.28101) | arXiv 2026 | — |
| [History Rhymes: Accelerating LLM Reinforcement Learning with RhymeRL](https://arxiv.org/abs/2508.18588) | [ASPLOS 2026](https://www.asplos-conference.org/asplos2026/program/) | — |
| [Moebius: Serving Mixture-of-Expert Models with Seamless Runtime Parallelism Switch](https://arxiv.org/abs/2606.26607) | arXiv 2026 | — |
| [Native Parallel Reasoner: Reasoning in Parallelism via Self-Distilled Reinforcement Learning](https://arxiv.org/abs/2512.07461) | [ICML 2026](https://proceedings.mlr.press/v306/wu26ai.html) | [![GitHub](https://img.shields.io/github/stars/bigai-nlco/Native-Parallel-Reasoner?style=flat&label=GitHub)](https://github.com/bigai-nlco/Native-Parallel-Reasoner) |
| [OPPO: Accelerating PPO-based RLHF via Pipeline Overlap](https://arxiv.org/abs/2509.25762) | [ICLR 2026](https://proceedings.iclr.cc/paper_files/paper/2026/hash/6b4fd4a4607f57fe65b5e276bdb17ed1-Abstract-Conference.html) | — |
| [QeRL: Beyond Efficiency -- Quantization-enhanced Reinforcement Learning for LLMs](https://arxiv.org/abs/2510.11696) | [ICLR 2026](https://proceedings.iclr.cc/paper_files/paper/2026/hash/a15a2ece7f0663d1ba7db91103ac61c9-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/NVlabs/QeRL?style=flat&label=GitHub)](https://github.com/NVlabs/QeRL) |
| [ReSpec: Towards Optimizing Speculative Decoding in Reinforcement Learning Systems](https://arxiv.org/abs/2510.26475) | [MLSys 2026](https://proceedings.mlsys.org/paper_files/paper/2026/hash/dcb38c6ad7911842ab31081be9540b89-Abstract-Conference.html) | — |
| [RLBoost: Harvesting Preemptible Resources for Cost-Efficient Reinforcement Learning on LLMs](https://arxiv.org/abs/2510.19225) | [NSDI 2026](https://www.usenix.org/conference/nsdi26/presentation/wu-yongji) | [![GitHub](https://img.shields.io/github/stars/Terra-Flux/PolyRL?style=flat&label=GitHub)](https://github.com/Terra-Flux/PolyRL) |
| [RLHFless: Serverless Computing for Efficient RLHF](https://arxiv.org/abs/2602.22718) | arXiv 2026 | — |
| [ROSE: Rollout On Serving GPUs via Cooperative Elasticity for Agentic RL](https://arxiv.org/abs/2605.06534) | arXiv 2026 | — |
| [Scheduling Mixed RL Rollouts Beyond Prefix Locality](https://arxiv.org/abs/2608.11152) | arXiv 2026 | — |
| [SortedRL: Accelerating RL Training for LLMs through Online Length-Aware Scheduling](https://arxiv.org/abs/2603.23414) | arXiv 2026 | — |
| [SPARK: Learning from Verification in Speculative GRPO Rollouts](https://arxiv.org/abs/2608.04962) | arXiv 2026 | — |
| [SRT: Accelerating Reinforcement Learning via Speculative Rollout with Tree-Structured Cache](https://arxiv.org/abs/2601.09083) | arXiv 2026 | — |
| [TailSieve: Partial-Rollout-Guided Tail Routing for LLM Rollouts](https://arxiv.org/abs/2608.22788) | arXiv 2026 | — |
| [The Markovian Thinker: Architecture-Agnostic Linear Scaling of Reasoning](https://arxiv.org/abs/2510.06557) | [ICLR 2026](https://proceedings.iclr.cc/paper_files/paper/2026/hash/4dd0cfda282c778a21b38fd1d637f37b-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/McGill-NLP/the-markovian-thinker?style=flat&label=GitHub)](https://github.com/McGill-NLP/the-markovian-thinker) |
| [ThunderAgent: A Simple, Fast and Program-Aware Agentic Inference System](https://arxiv.org/abs/2602.13692) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/ThunderAgent-org/ThunderAgent?style=flat&label=GitHub)](https://github.com/ThunderAgent-org/ThunderAgent) |
| [AgentRL: Scaling Agentic Reinforcement Learning with a Multi-Turn, Multi-Task Framework](https://arxiv.org/abs/2510.04206) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/THUDM/AgentRL?style=flat&label=GitHub)](https://github.com/THUDM/AgentRL) |
| [APRIL: Active Partial Rollouts in Reinforcement Learning to Tame Long-tail Generation](https://arxiv.org/abs/2509.18521) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/RLsys-Foundation/APRIL?style=flat&label=GitHub)](https://github.com/RLsys-Foundation/APRIL) |
| [AReaL: A Large-Scale Asynchronous Reinforcement Learning System for Language Reasoning](https://arxiv.org/abs/2505.24298) | [NeurIPS 2025](https://proceedings.neurips.cc/paper_files/paper/2025/hash/33c00862bfa29ac72ecf630a41e19352-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/areal-project/AReaL?style=flat&label=GitHub)](https://github.com/areal-project/AReaL) |
| [Beyond Ten Turns: Unlocking Long-Horizon Agentic Search with Large-Scale Asynchronous RL](https://arxiv.org/abs/2508.07976) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/inclusionAI/ASearcher?style=flat&label=GitHub)](https://github.com/inclusionAI/ASearcher) |
| [CoPRIS: Efficient and Stable Reinforcement Learning via Concurrency-Controlled Partial Rollout with Importance Sampling](https://arxiv.org/abs/2511.05589) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/777pomingzi/CoPRIS?style=flat&label=GitHub)](https://github.com/777pomingzi/CoPRIS) |
| [DistRL: An Asynchronous Distributed Reinforcement Learning Framework for On-Device Control Agents](https://arxiv.org/abs/2410.14803) | [ICLR 2025](https://proceedings.iclr.cc/paper_files/paper/2025/hash/b9e472cd579c83e2f6aa3459f46aac28-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/ai-agents-2030/DistRL-open?style=flat&label=GitHub)](https://github.com/ai-agents-2030/DistRL-open) |
| [EARL: Efficient Agentic Reinforcement Learning Systems for Large Language Models](https://arxiv.org/abs/2510.05943) | arXiv 2025 | — |
| [Efficient Multi-turn RL for GUI Agents via Decoupled Training and Adaptive Data Curation](https://arxiv.org/abs/2509.23866) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/Computer-use-agents/dart-gui?style=flat&label=GitHub)](https://github.com/Computer-use-agents/dart-gui) |
| [Infinite Sampling: Efficient and Stable Grouped RL Training for Large Language Models](https://arxiv.org/abs/2506.22950) | arXiv 2025 | — |
| [Kimi k1.5: Scaling Reinforcement Learning with LLMs](https://arxiv.org/abs/2501.12599) | arXiv 2025 | — |
| [Klear-AgentForge: Forging Agentic Intelligence through Posttraining Scaling](https://arxiv.org/abs/2511.05951) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/Kwai-Klear/Klear-AgentForge?style=flat&label=GitHub)](https://github.com/Kwai-Klear/Klear-AgentForge) |
| [OpenRLHF: An Easy-to-use, Scalable and High-performance RLHF Framework](https://arxiv.org/abs/2405.11143) | [EMNLP 2025 (Demo)](https://aclanthology.org/2025.emnlp-demos.48/) | [![GitHub](https://img.shields.io/github/stars/OpenRLHF/OpenRLHF?style=flat&label=GitHub)](https://github.com/OpenRLHF/OpenRLHF) |
| [Part II: ROLL Flash -- Accelerating RLVR and Agentic Training with Asynchrony](https://arxiv.org/abs/2510.11345) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/alibaba/ROLL?style=flat&label=GitHub)](https://github.com/alibaba/ROLL) |
| [RECON: Reasoning with Condensation for Efficient Retrieval-Augmented Generation](https://arxiv.org/abs/2510.10448) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/minhengwang/RECON?style=flat&label=GitHub)](https://github.com/minhengwang/RECON) |
| [RLHFSpec: Breaking the Efficiency Bottleneck in RLHF Training via Adaptive Drafting](https://arxiv.org/abs/2512.04752) | arXiv 2025 | — |
| [RollPacker: Mitigating Long-Tail Rollouts for Fast, Synchronous RL Post-Training](https://arxiv.org/abs/2509.21009) | arXiv 2025 | — |
| [Scaling RL to Long Videos](https://arxiv.org/abs/2507.07966) | [NeurIPS 2025](https://proceedings.neurips.cc/paper_files/paper/2025/hash/fc2865a2fdd5fd401050d37ee4946850-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/NVlabs/nano-rl?style=flat&label=GitHub)](https://github.com/NVlabs/nano-rl) |
| [SkyRL-Agent: Efficient RL Training for Multi-turn LLM Agent](https://arxiv.org/abs/2511.16108) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/NovaSky-AI/SkyRL?style=flat&label=GitHub)](https://github.com/NovaSky-AI/SkyRL) |
| [SPEC-RL: Accelerating On-Policy Reinforcement Learning with Speculative Rollouts](https://arxiv.org/abs/2509.23232) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/ShopeeLLM/Spec-RL?style=flat&label=GitHub)](https://github.com/ShopeeLLM/Spec-RL) |
| [StreamRL: Scalable, Heterogeneous, and Elastic RL for LLMs with Disaggregated Stream Generation](https://arxiv.org/abs/2504.15930) | arXiv 2025 | — |
| [Taming the Long-Tail: Efficient Reasoning RL Training with Adaptive Drafter](https://arxiv.org/abs/2511.16665) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/mit-han-lab/fastrl?style=flat&label=GitHub)](https://github.com/mit-han-lab/fastrl) |
| [TreePO: Bridging the Gap of Policy Optimization and Efficacy and Inference Efficiency with Heuristic Tree-based Modeling](https://arxiv.org/abs/2508.17445) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/multimodal-art-projection/TreePO?style=flat&label=GitHub)](https://github.com/multimodal-art-projection/TreePO) |

<a id="environment-reliability"></a>

### Environment Reliability

Maintain interaction availability, isolation, reproducibility, and simulator fidelity.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [ARL-Tangram: Unleash the Resource Efficiency in Agentic Reinforcement Learning](https://arxiv.org/abs/2603.13019) | arXiv 2026 | — |
| [Belayer: Efficient Fault Tolerance for LLM Agentic RL Training](https://arxiv.org/abs/2608.14635) | arXiv 2026 | — |
| [Crab: A Semantics-Aware Checkpoint/Restore Runtime for Agent Sandboxes](https://arxiv.org/abs/2604.28138) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/open-agent-infra/crab?style=flat&label=GitHub)](https://github.com/open-agent-infra/crab) |
| [DeepSeek Elastic Compute (DSec): A Sandbox Infrastructure for Effective Agentic Training at Scale](https://arxiv.org/abs/2609.22978) | arXiv 2026 | [Storage component](https://github.com/kvcache-ai/AgentENV/tree/main/storage/overlaybd) |
| [DeltaBox: Scaling Stateful AI Agents with Millisecond-Level Sandbox Checkpoint/Rollback](https://arxiv.org/abs/2605.22781) | [SIGOPS ATC 2026](https://arxiv.org/abs/2605.22781) | [![GitHub](https://img.shields.io/github/stars/delta-box/delta-box-ae?style=flat&label=GitHub)](https://github.com/delta-box/delta-box-ae) |
| [LiteResearcher: A Scalable Agentic RL Training Framework for Deep Research Agent](https://arxiv.org/abs/2604.17931) | [COLM 2026](https://arxiv.org/abs/2604.17931) | [![GitHub](https://img.shields.io/github/stars/simplexai-labs/LiteResearcher?style=flat&label=GitHub)](https://github.com/simplexai-labs/LiteResearcher) |
| [MCP-Universe RL: A Framework for Training MCP Tool-Use Agents via Reinforcement Learning](https://arxiv.org/abs/2608.22167) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/SalesforceAIResearch/MCP-Universe?style=flat&label=GitHub)](https://github.com/SalesforceAIResearch/MCP-Universe/tree/main/mcpuniverse/rl) |
| [One Frozen Simulator Is Not Enough: Simulator Collapse in Multi-Agent RL](https://arxiv.org/abs/2608.12253) | [EMNLP 2026](https://aclanthology.org/2026.emnlp-main.790/) | [![GitHub](https://img.shields.io/github/stars/CHATS-lab/scope_usim?style=flat&label=GitHub)](https://github.com/CHATS-lab/scope_usim) |
| [Orchard: An Open-Source Agentic Modeling Framework](https://arxiv.org/abs/2605.15040) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/microsoft/Orchard-Agentic?style=flat&label=GitHub)](https://github.com/microsoft/Orchard-Agentic) |
| [ProRL Agent: Rollout-as-a-Service for RL Training of Multi-Turn LLM Agents](https://arxiv.org/abs/2603.18815) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/NVIDIA-NeMo/ProRL-Agent-Server?style=flat&label=GitHub)](https://github.com/NVIDIA-NeMo/ProRL-Agent-Server) |
| [REDSearcher: A Scalable and Cost-Efficient Framework for Long-Horizon Search Agents](https://arxiv.org/abs/2602.14234) | arXiv 2026 | [Pending](https://github.com/RedSearchAgent/REDSearcher) |
| [Synthetic Sandbox for Training Machine Learning Engineering Agents](https://arxiv.org/abs/2604.04872) | arXiv 2026 | — |
| [Weblica: Scalable and Reproducible Training Environments for Visual Web Agents](https://arxiv.org/abs/2605.06761) | arXiv 2026 | — |
| [AgentFly: Scaling Agentic Reinforcement Learning with Unified Resource System](https://arxiv.org/abs/2507.14897) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/Agent-One-Lab/AgentFly?style=flat&label=GitHub)](https://github.com/Agent-One-Lab/AgentFly) |
| [RepoForge: Training a SOTA Fast-thinking SWE Agent with an End-to-End Data Curation Pipeline Synergizing SFT and RL at Scale](https://arxiv.org/abs/2508.01550) | arXiv 2025 | — |
| [RLFactory: A Plug-and-Play Reinforcement Learning Post-Training Framework for LLM Multi-Turn Tool-Use](https://arxiv.org/abs/2509.06980) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/Simple-Efficient/RL-Factory?style=flat&label=GitHub)](https://github.com/Simple-Efficient/RL-Factory) |
| [Scaling Agentic Reinforcement Learning for Tool-Integrated Reasoning in VLMs](https://arxiv.org/abs/2511.19773) | arXiv 2025 | [Environment / SFT](https://github.com/Lucanyc/VISTA-Gym) |
| [WebSailor-V2: Bridging the Chasm to Proprietary Agents via Synthetic Data and Scalable Reinforcement Learning](https://arxiv.org/abs/2509.13305) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/Alibaba-NLP/DeepResearch?style=flat&label=GitHub)](https://github.com/Alibaba-NLP/DeepResearch) |
| [Youtu-Agent: Scaling Agent Productivity with Automated Generation and Hybrid Policy Optimization](https://arxiv.org/abs/2512.24615) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/TencentCloudADP/youtu-agent?style=flat&label=GitHub)](https://github.com/TencentCloudADP/youtu-agent) |

<a id="trajectory-lifecycle-management"></a>

### Trajectory Lifecycle Management

Represent, admit, store, deliver, replay, and retire collected trajectories.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [StaleFlow: Staleness-Aware Data Management for Mitigating Data Skewness in Fully Disaggregated RL Post-Training](https://arxiv.org/abs/2601.12784) | [SIGMOD 2027 (accepted)](https://ccchengff.github.io/publications/) | [![GitHub](https://img.shields.io/github/stars/psrl-project/psrl?style=flat&label=GitHub)](https://github.com/psrl-project/psrl) |
| [Agent Lightning v1.0: Towards Harnessed Agentic RL](https://arxiv.org/abs/2608.17528) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/microsoft/agent-lightning?style=flat&label=GitHub)](https://github.com/microsoft/agent-lightning) |
| [AgentJet: A Distributed Swarm Training Framework for Agentic Reinforcement Learning](https://arxiv.org/abs/2606.04484) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/modelscope/AgentJet?style=flat&label=GitHub)](https://github.com/modelscope/AgentJet) |
| [AgentWorld: A Data Factory for Training LLM Agents from Multi-Turn Interactions](https://arxiv.org/abs/2606.09138) | [ICDM 2026 (Demo, accepted)](https://arxiv.org/abs/2606.09138) | [![GitHub](https://img.shields.io/github/stars/AgentR1/Claw-R1?style=flat&label=GitHub)](https://github.com/AgentR1/Claw-R1) |
| [Complementary RL: Towards Efficient Experience-Driven Agent Learning](https://arxiv.org/abs/2603.17621) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/pUmpKin-Co/ComplementaryRL?style=flat&label=GitHub)](https://github.com/pUmpKin-Co/ComplementaryRL) |
| [Contextual Rollout Bandits for Reinforcement Learning with Verifiable Rewards](https://arxiv.org/abs/2602.08499) | [ICML 2026](https://proceedings.mlr.press/v306/lu26aj.html) | [![GitHub](https://img.shields.io/github/stars/lxd99/CBS_public?style=flat&label=GitHub)](https://github.com/lxd99/CBS_public) |
| [Efficient RL Training for LLMs with Experience Replay](https://arxiv.org/abs/2604.08706) | [ICML 2026](https://proceedings.mlr.press/v306/arnal26a.html) | — |
| [GEOALIGN: Geometric Rollout Curation for Robust LLM Reinforcement Learning](https://arxiv.org/abs/2606.26917) | [ICML 2026](https://proceedings.mlr.press/v306/zhou26ad.html) | [![GitHub](https://img.shields.io/github/stars/SYSUzhouting/Trinity-RFT?style=flat&label=GitHub)](https://github.com/SYSUzhouting/Trinity-RFT) |
| [Headroom-Drift Replay: A Primitive for Principled Replay Control in GRPO](https://arxiv.org/abs/2609.03941) | [COLM 2026](https://arxiv.org/abs/2609.03941) | — |
| [KV-streams for Efficient Compaction in Agentic Reinforcement Learning](https://arxiv.org/abs/2609.35750) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/Emilianopp/KV-streams?style=flat&label=GitHub)](https://github.com/Emilianopp/KV-streams) |
| [Learning from the Right Rollouts: Data Attribution for PPO-based LLM Post-Training](https://arxiv.org/abs/2604.01597) | arXiv 2026 | — |
| [Not All Rollouts are Useful: Down-Sampling Rollouts in LLM Reinforcement Learning](https://arxiv.org/abs/2504.13818) | [TMLR 2026](https://arxiv.org/abs/2504.13818) | [![GitHub](https://img.shields.io/github/stars/YixuanEvenXu/pods?style=flat&label=GitHub)](https://github.com/YixuanEvenXu/pods) |
| [Polar: Agentic RL on Any Harness at Scale](https://arxiv.org/abs/2605.24220) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/NVIDIA-NeMo/ProRL-Agent-Server?style=flat&label=GitHub)](https://github.com/NVIDIA-NeMo/ProRL-Agent-Server) |
| [Rollout-Level Advantage-Prioritized Experience Replay for GRPO](https://arxiv.org/abs/2606.04560) | [EMNLP 2026 (Findings)](https://aclanthology.org/2026.findings-emnlp.2331/) | — |
| [Where Does Staleness Accumulate? Pool Aware Effective Staleness Control for Asynchronous RL in LLM Post-Training](https://arxiv.org/abs/2609.36830) | arXiv 2026 | — |
| [A Snapshot of Influence: A Local Data Attribution Framework for Online Reinforcement Learning](https://arxiv.org/abs/2505.19281) | [NeurIPS 2025](https://proceedings.neurips.cc/paper_files/paper/2025/hash/377d0752059d3d4686aa021b664a25dd-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/LDAORL/LDA-ORL?style=flat&label=GitHub)](https://github.com/LDAORL/LDA-ORL) |
| [Agent Lightning: Train ANY AI Agents with Reinforcement Learning](https://arxiv.org/abs/2508.03680) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/microsoft/agent-lightning?style=flat&label=GitHub)](https://github.com/microsoft/agent-lightning) |
| [Agent-R1: A Unified and Modular Framework for Agentic Reinforcement Learning](https://arxiv.org/abs/2511.14460) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/AgentR1/Agent-R1?style=flat&label=GitHub)](https://github.com/AgentR1/Agent-R1) |
| [AsyncFlow: An Asynchronous Streaming RL Framework for Efficient LLM Post-Training](https://arxiv.org/abs/2507.01663) | arXiv 2025 | [TransferQueue](https://github.com/Ascend/TransferQueue) |
| [Improving Data Efficiency for LLM Reinforcement Fine-tuning Through Difficulty-targeted Online Data Selection and Rollout Replay](https://arxiv.org/abs/2506.05316) | [NeurIPS 2025](https://proceedings.neurips.cc/paper_files/paper/2025/hash/fd54731cc635e2ed6033e8a0e193eddf-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/ASTRAL-Group/data-efficient-llm-rl?style=flat&label=GitHub)](https://github.com/ASTRAL-Group/data-efficient-llm-rl) |
| [Improving Sampling Efficiency in RLVR through Adaptive Rollout and Response Reuse](https://arxiv.org/abs/2509.25808) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/horizon-llm/adaptive-rollout?style=flat&label=GitHub)](https://github.com/horizon-llm/adaptive-rollout) |
| [Sharing is Caring: Efficient LM Post-Training with Collective RL Experience Sharing](https://arxiv.org/abs/2509.08721) | arXiv 2025 | — |
| [Tool-R1: Sample-Efficient Reinforcement Learning for Agentic Tool Use](https://arxiv.org/abs/2509.12867) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/YBYBZhang/Tool-R1?style=flat&label=GitHub)](https://github.com/YBYBZhang/Tool-R1) |
| [ToolBrain: A Flexible Reinforcement Learning Framework for Agentic Tools](https://arxiv.org/abs/2510.00023) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/ToolBrain/ToolBrain?style=flat&label=GitHub)](https://github.com/ToolBrain/ToolBrain) |
| [Trinity-RFT: A General-Purpose and Unified Framework for Reinforcement Fine-Tuning of Large Language Models](https://arxiv.org/abs/2505.17826) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/agentscope-ai/Trinity-RFT?style=flat&label=GitHub)](https://github.com/agentscope-ai/Trinity-RFT) |

[Back to taxonomy](#taxonomy)

<a id="reward-computation"></a>

## Reward Computation

Maintain the reliability of feedback sources and training reward signals.

30 papers

<a id="learned-evaluators"></a>

### Learned Evaluators

Calibrate model-based scores, manage uncertainty, and improve evaluator robustness.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [AgentOmnia: Scaling Agentic Models for Full-Scenario Applications](https://arxiv.org/abs/2607.23124) | arXiv 2026 | — |
| [ARES: Adaptive Red-Teaming and End-to-End Repair of Policy-Reward System](https://arxiv.org/abs/2604.18789) | [ACL 2026](https://aclanthology.org/2026.acl-long.1985/) | — |
| [How Far Can Unsupervised RLVR Scale LLM Training?](https://arxiv.org/abs/2603.08660) | [ICLR 2026](https://arxiv.org/abs/2603.08660) | [![GitHub](https://img.shields.io/github/stars/PRIME-RL/TTRL?style=flat&label=GitHub)](https://github.com/PRIME-RL/TTRL) |
| [WebGym: Scaling Training Environments for Visual Web Agents with Realistic Tasks](https://arxiv.org/abs/2601.02439) | arXiv 2026 | — |
| [When RLHF Fails: A Mechanistic Taxonomy of Reward Hacking, Collapse, and Evaluator Gaming](https://arxiv.org/abs/2606.03238) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/zabahana/rlhf-failure-modes-diagnostics?style=flat&label=GitHub)](https://github.com/zabahana/rlhf-failure-modes-diagnostics) |
| [Post-hoc Reward Calibration: A Case Study on Length Bias](https://arxiv.org/abs/2409.17407) | [ICLR 2025](https://proceedings.iclr.cc/paper_files/paper/2025/hash/5d50c76fdf75c24ece568fc84a7125fb-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/ZeroYuHuang/Reward-Calibration?style=flat&label=GitHub)](https://github.com/ZeroYuHuang/Reward-Calibration) |
| [Reward Model Overoptimisation in Iterated RLHF](https://arxiv.org/abs/2505.18126) | arXiv 2025 | — |
| [(N,K)-Puzzle: A Cost-Efficient Testbed for Benchmarking Reinforcement Learning Algorithms in Generative Language Model](https://arxiv.org/abs/2403.07191) | arXiv 2024 | — |
| [Improving Reinforcement Learning from Human Feedback with Efficient Reward Model Ensemble](https://arxiv.org/abs/2401.16635) | arXiv 2024 | — |
| [ODIN: Disentangled Reward Mitigates Hacking in RLHF](https://arxiv.org/abs/2402.07319) | [ICML 2024](https://proceedings.mlr.press/v235/chen24bn.html) | [![GitHub](https://img.shields.io/github/stars/Lichang-Chen/ODIN?style=flat&label=GitHub)](https://github.com/Lichang-Chen/ODIN) |
| [Reward Model Ensembles Help Mitigate Overoptimization](https://arxiv.org/abs/2310.02743) | [ICLR 2024](https://proceedings.iclr.cc/paper_files/paper/2024/hash/dda7f9378a210c25e470e19304cce85d-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/tlc4418/llm_optimization?style=flat&label=GitHub)](https://github.com/tlc4418/llm_optimization) |
| [WARM: On the Benefits of Weight Averaged Reward Models](https://arxiv.org/abs/2401.12187) | [ICML 2024](https://proceedings.mlr.press/v235/rame24a.html) | — |
| [Training a Helpful and Harmless Assistant with Reinforcement Learning from Human Feedback](https://arxiv.org/abs/2204.05862) | arXiv 2022 | — |

<a id="programmatic-verifiers"></a>

### Programmatic Verifiers

Maintain verifier execution, specification adequacy, and integrity.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Automating Formal Verification with Reinforcement Learning and Recursive Inference](https://arxiv.org/abs/2605.30914) | [Master's thesis 2026](https://arxiv.org/abs/2605.30914) | — |
| [CATCH: A Controllable Analysis Testbed for Reward Hacking in Coding RL](https://arxiv.org/abs/2609.39533) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/THUAIS-Lab/CATCH?style=flat&label=GitHub)](https://github.com/THUAIS-Lab/CATCH) |
| [Countdown-Code: A Testbed for Studying The Emergence and Generalization of Reward Hacking in RLVR](https://arxiv.org/abs/2603.07084) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/zohaib-khan5040/Countdown-Code?style=flat&label=GitHub)](https://github.com/zohaib-khan5040/Countdown-Code) |
| [Evaluating Rollout-Verified Reinforcement Fine-Tuning of a Reasoning Model for Multi-Zone Variable-Air-Volume Control](https://arxiv.org/abs/2607.27914) | [Energy and AI 2026](https://doi.org/10.1016/j.egyai.2026.100933) | — |
| [LLMs Gaming Verifiers: RLVR can Lead to Reward Hacking](https://arxiv.org/abs/2604.15149) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/ml-research/llms-gaming-verifiers?style=flat&label=GitHub)](https://github.com/ml-research/llms-gaming-verifiers) |
| [Reward Hacking in Language Model Agents: Revisiting AI Safety Gridworlds](https://arxiv.org/abs/2606.15385) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/asparius/verl-agent-safety?style=flat&label=GitHub)](https://github.com/asparius/verl-agent-safety) |

<a id="reward-signals"></a>

### Reward Signals

Compose, attribute, and correct the feedback supplied to learning.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [AgentCPM-Explore: Realizing Long-Horizon Deep Exploration for Edge-Scale Agents](https://arxiv.org/abs/2602.06485) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/OpenBMB/AgentCPM?style=flat&label=GitHub)](https://github.com/OpenBMB/AgentCPM/tree/main/AgentCPM-Explore) |
| [CacheRL:Multi-Turn Tool-Calling Agents via Cached Rollouts and Hybrid Reward](https://arxiv.org/abs/2606.14179) | arXiv 2026 | — |
| [FAPO: Flawed-Aware Policy Optimization for Efficient and Reliable Reasoning](https://arxiv.org/abs/2510.22543) | [ICLR 2026](https://arxiv.org/abs/2510.22543) | [![GitHub](https://img.shields.io/github/stars/yyDing1/FAPO?style=flat&label=GitHub)](https://github.com/yyDing1/FAPO) |
| [Multimodal Reward Hacking in Reinforcement Learning](https://arxiv.org/abs/2607.09492) | [EMNLP 2026 (Findings)](https://aclanthology.org/2026.findings-emnlp.980/) | [![GitHub](https://img.shields.io/github/stars/Theodyy/MLLM-Reward-Hacking?style=flat&label=GitHub)](https://github.com/Theodyy/MLLM-Reward-Hacking) |
| [Peak-Then-Collapse and the Four Interface Channels of Knowledge-Graph Tool Use](https://arxiv.org/abs/2605.26037) | [EMNLP 2026](https://aclanthology.org/2026.emnlp-main.443/) | [![GitHub](https://img.shields.io/github/stars/TiandaSun/KG_GRPO?style=flat&label=GitHub)](https://github.com/TiandaSun/KG_GRPO) |
| [Scaling Automatic Research Agents via World Models](https://arxiv.org/abs/2608.12564) | arXiv 2026 | [Reference implementation](https://github.com/xiyuanyang45/WMRL) |
| [Scaling Reinforcement Learning for Content Moderation with Large Language Models](https://arxiv.org/abs/2512.20061) | [EMNLP 2026 (Industry)](https://aclanthology.org/2026.emnlp-industry.17/) | — |
| [Reinforcement Learning from User Feedback](https://arxiv.org/abs/2505.14946) | arXiv 2025 | — |
| [Reinforcement Learning with Verifiable yet Noisy Rewards under Imperfect Verifiers](https://arxiv.org/abs/2510.00915) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/caixq1996/noisy-RLVR?style=flat&label=GitHub)](https://github.com/caixq1996/noisy-RLVR) |
| [Stop Summation: Min-Form Credit Assignment Is All Process Reward Model Needs for Reasoning](https://arxiv.org/abs/2504.15275) | [NeurIPS 2025](https://papers.nips.cc/paper_files/paper/2025/hash/be91eb86eb74efc055cff83e953f86ce-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/CJReinforce/PURE?style=flat&label=GitHub)](https://github.com/CJReinforce/PURE) |
| [Safe RLHF: Safe Reinforcement Learning from Human Feedback](https://arxiv.org/abs/2310.12773) | [ICLR 2024](https://proceedings.iclr.cc/paper_files/paper/2024/hash/dd1577afd396928ed64216f3f1fd5556-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/PKU-Alignment/safe-rlhf?style=flat&label=GitHub)](https://github.com/PKU-Alignment/safe-rlhf) |

[Back to taxonomy](#taxonomy)

<a id="policy-optimization"></a>

## Policy Optimization

Execute policy updates with consistency, stable learning, and recoverable state.

89 papers

<a id="update-execution"></a>

### Update Execution

Manage orchestration, memory, computation, and parameter transfer.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [AREAL-DTA: Dynamic Tree Attention for Efficient Reinforcement Learning of Large Language Models](https://arxiv.org/abs/2602.00482) | [ICML 2026](https://proceedings.mlr.press/v306/zhang26hr.html) | [![GitHub](https://img.shields.io/github/stars/areal-project/AReaL?style=flat&label=GitHub)](https://github.com/areal-project/AReaL/tree/feat/dta) |
| [AuroraRL: Fast, Fault-Tolerant, and Cost-Efficient Reinforcement Learning over Decentralized Network](https://arxiv.org/abs/2602.11456) | arXiv 2026 | — |
| [Bidirectional Resource Scheduling for Disaggregated and Asynchronous RL Post-Training](https://arxiv.org/abs/2607.09207) | arXiv 2026 | — |
| [DistFlow: A Fully Distributed RL Framework for Scalable and Efficient LLM Post-Training](https://arxiv.org/abs/2507.13833) | [ICML 2026](https://proceedings.mlr.press/v306/wang26jl.html) | [![GitHub](https://img.shields.io/github/stars/sii-research/siiRL?style=flat&label=GitHub)](https://github.com/sii-research/siiRL) |
| [FlexMARL: Graph-Driven Rollout-Training Co-Design for LLM-Based Multi-Agent Reinforcement Learning](https://arxiv.org/abs/2602.09578) | arXiv 2026 | — |
| [Harnessing Routing Foresight for Micro-step-level MoE load balancing in RL Post-training](https://arxiv.org/abs/2606.11867) | arXiv 2026 | — |
| [HetRL: Efficient Reinforcement Learning for LLMs in Heterogeneous Environments](https://arxiv.org/abs/2512.12476) | [MLSys 2026](https://proceedings.mlsys.org/paper_files/paper/2026/hash/5321b1dabcd2be188d796c21b733e8c7-Abstract-Conference.html) | — |
| [JigsawRL: Assembling RL Pipelines for Efficient LLM Post-Training](https://arxiv.org/abs/2604.23838) | arXiv 2026 | — |
| [Libra: Efficient Resource Management for Agentic RL Post-Training](https://arxiv.org/abs/2606.03077) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/NetX-lab/Libra?style=flat&label=GitHub)](https://github.com/NetX-lab/Libra) |
| [MARLaaS: Multi-Tenant Asynchronous Reinforcement Learning as a Service](https://arxiv.org/abs/2605.08527) | arXiv 2026 | — |
| [MinT: Managed Infrastructure for Training and Serving Millions of LLMs](https://arxiv.org/abs/2605.13779) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/verl-project/verl-mint?style=flat&label=GitHub)](https://github.com/verl-project/verl-mint) |
| [Nereus: Adaptive Parallelism for LLM Post-Training](https://arxiv.org/abs/2609.34645) | arXiv 2026 | — |
| [PlexRL: Cluster-Level Orchestration of Serviceized LLM Execution for RLVR](https://arxiv.org/abs/2605.20863) | arXiv 2026 | — |
| [PrefixFlow: Training-Time KV Caching for Schedule-Level Prefix Reuse in LLM RL Training](https://arxiv.org/abs/2606.01143) | [SIGOPS ATC 2026](https://arxiv.org/abs/2606.01143) | — |
| [QwenGyre: An Elastic Reinforcement Learning Framework for Training xLong-Horizon Agents](https://arxiv.org/abs/2609.33848) | arXiv 2026 | — |
| [Relax: An Asynchronous Reinforcement Learning Engine for Omni-Modal Post-Training at Scale](https://arxiv.org/abs/2604.11554) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/redai-studio/Relax?style=flat&label=GitHub)](https://github.com/redai-studio/Relax) |
| [ReLibra: Routing-Replay-Guided Load Balancing for MoE Training in Reinforcement Learning](https://arxiv.org/abs/2605.08639) | arXiv 2026 | — |
| [RLinf: Flexible and Efficient Large-scale Reinforcement Learning via Macro-to-Micro Flow Transformation](https://arxiv.org/abs/2509.15965) | [OSDI 2026](https://www.usenix.org/conference/osdi26/presentation/yu-chao) | [![GitHub](https://img.shields.io/github/stars/RLinf/RLinf?style=flat&label=GitHub)](https://github.com/RLinf/RLinf) |
| [RollArt: Disaggregated Multi-Task Agentic RL Training at Scale](https://arxiv.org/abs/2512.22560) | [OSDI 2026](https://www.usenix.org/conference/osdi26/presentation/gao) | — |
| [RolloutPipe: Overlapping Pipelined Rollout and Training in Disaggregated On-Policy LLM Reinforcement Learning](https://arxiv.org/abs/2606.26997) | [ICCC 2026](https://arxiv.org/abs/2606.26997) | — |
| [Splitting Prompt Prefill from Response Replay for Context-Parallel Long-Context LLM Post-Training](https://arxiv.org/abs/2609.33133) | arXiv 2026 | — |
| [TensorHub: Scalable and Elastic Weight Transfer for LLM RL Training](https://arxiv.org/abs/2604.09107) | [SOSP 2026](https://doi.org/10.1145/3830418.3843859) | — |
| [TENT: A Declarative Slice Spraying Engine for Performant and Resilient Data Movement in Disaggregated LLM Serving](https://arxiv.org/abs/2604.00368) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/kvcache-ai/Mooncake?style=flat&label=GitHub)](https://github.com/kvcache-ai/Mooncake) |
| [TideRL: Boosting Agentic RL Goodput with Readiness-Aware Scheduling](https://arxiv.org/abs/2608.10402) | arXiv 2026 | — |
| [Understanding and Exploiting Weight Update Sparsity for Communication-Efficient Distributed RL](https://arxiv.org/abs/2602.03839) | arXiv 2026 | — |
| [WeightBridge: An Efficient Weight Transfer Library for Reinforcement Learning](https://arxiv.org/abs/2609.25442) | arXiv 2026 | — |
| [AReaL-Hex: Accommodating Asynchronous RL Training over Heterogeneous GPUs](https://arxiv.org/abs/2511.00796) | arXiv 2025 | — |
| [DiRL: An Efficient Post-Training Framework for Diffusion Language Models](https://arxiv.org/abs/2512.22234) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/OpenMOSS/DiRL?style=flat&label=GitHub)](https://github.com/OpenMOSS/DiRL) |
| [HybridFlow: A Flexible and Efficient RLHF Framework](https://arxiv.org/abs/2409.19256) | [EuroSys 2025](https://doi.org/10.1145/3689031.3696075) | [![GitHub](https://img.shields.io/github/stars/verl-project/verl?style=flat&label=GitHub)](https://github.com/verl-project/verl) |
| [LlamaRL: A Distributed Asynchronous Reinforcement Learning Framework for Efficient Large-scale LLM Training](https://arxiv.org/abs/2505.24034) | arXiv 2025 | — |
| [MarsRL: Advancing Multi-Agent Reasoning System via Reinforcement Learning with Agentic Pipeline Parallelism](https://arxiv.org/abs/2511.11373) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/liushulinle/MarsRL?style=flat&label=GitHub)](https://github.com/liushulinle/MarsRL) |
| [MindSpeed RL: Distributed Dataflow for Scalable and Efficient RL Training on Ascend NPU Cluster](https://arxiv.org/abs/2507.19017) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/Ascend/MindSpeed-RL?style=flat&label=GitHub)](https://github.com/Ascend/MindSpeed-RL) |
| [Optimizing RLHF Training for Large Language Models with Stage Fusion](https://arxiv.org/abs/2409.13221) | [NSDI 2025](https://www.usenix.org/conference/nsdi25/presentation/zhong) | — |
| [Pangu Embedded: An Efficient Dual-system LLM Reasoner with Metacognition](https://arxiv.org/abs/2505.22375) | arXiv 2025 | — |
| [ReaL: Efficient RLHF Training of Large Language Models with Parameter Reallocation](https://arxiv.org/abs/2406.14088) | [MLSys 2025](https://proceedings.mlsys.org/paper_files/paper/2025/file/3b3889d313ba9476c12c2d77ea66b24f-Paper-Conference.pdf) | [![GitHub](https://img.shields.io/github/stars/openpsi-project/ReaLHF?style=flat&label=GitHub)](https://github.com/openpsi-project/ReaLHF) |
| [RLLaVA: An RL-central Framework for Language and Vision Assistants](https://arxiv.org/abs/2512.21450) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/TinyLoopX/RLLaVA?style=flat&label=GitHub)](https://github.com/TinyLoopX/RLLaVA) |
| [Tree Training: Accelerating Agentic LLMs Training via Shared Prefix Reuse](https://arxiv.org/abs/2511.00413) | arXiv 2025 | — |
| [NeMo-Aligner: Scalable Toolkit for Efficient Model Alignment](https://arxiv.org/abs/2405.01481) | [COLM 2024](https://arxiv.org/abs/2405.01481) | [![GitHub](https://img.shields.io/github/stars/NVIDIA/NeMo-Aligner?style=flat&label=GitHub)](https://github.com/NVIDIA/NeMo-Aligner) |
| [Parameter Efficient Reinforcement Learning from Human Feedback](https://arxiv.org/abs/2403.10704) | arXiv 2024 | — |
| [An Adaptive Placement and Parallelism Framework for Accelerating RLHF Training](https://arxiv.org/abs/2312.11819) | arXiv 2023 | — |
| [DeepSpeed-Chat: Easy, Fast and Affordable RLHF Training of ChatGPT-like Models at All Scales](https://arxiv.org/abs/2308.01320) | arXiv 2023 | [![GitHub](https://img.shields.io/github/stars/deepspeedai/DeepSpeedExamples?style=flat&label=GitHub)](https://github.com/deepspeedai/DeepSpeedExamples/tree/master/applications/DeepSpeed-Chat) |
| [Efficient RLHF: Reducing the Memory Usage of PPO](https://arxiv.org/abs/2309.00754) | arXiv 2023 | — |
| [trlX: A Framework for Large Scale Reinforcement Learning from Human Feedback](https://aclanthology.org/2023.emnlp-main.530/) | [EMNLP 2023](https://aclanthology.org/2023.emnlp-main.530/) | [![GitHub](https://img.shields.io/github/stars/CarperAI/trlx?style=flat&label=GitHub)](https://github.com/CarperAI/trlx) |

<a id="policy-consistency"></a>

### Policy Consistency

Control staleness, numerical discrepancies, and divergent execution paths.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Cool the Sampler, Not the Learner: Sampling Temperature Moves the Staleness Cliff of Importance-Corrected GRPO](https://arxiv.org/abs/2609.36953) | arXiv 2026 | — |
| [Deterministic Inference across Tensor Parallel Sizes That Eliminates Training-Inference Mismatch](https://arxiv.org/abs/2511.17826) | [ICML 2026](https://proceedings.mlr.press/v306/zhang26ag.html) | [![GitHub](https://img.shields.io/github/stars/nanomaoli/llm_reproducibility?style=flat&label=GitHub)](https://github.com/nanomaoli/llm_reproducibility) |
| [Diagnosing Training Inference Mismatch in LLM Reinforcement Learning via a Zero-Mismatch Reference](https://arxiv.org/abs/2605.14220) | arXiv 2026 | — |
| [FP8-RL: A Practical and Stable Low-Precision Stack for LLM Reinforcement Learning](https://arxiv.org/abs/2601.18150) | arXiv 2026 | — |
| [How Off-Policy Can GRPO Be? Mu-GRPO for Efficient LLM Reinforcement Learning](https://arxiv.org/abs/2605.17570) | arXiv 2026 | — |
| [Jackpot: Optimal Budgeted Rejection Sampling for Extreme Actor-Policy Mismatch Reinforcement Learning](https://arxiv.org/abs/2602.06107) | [ICLR 2026](https://arxiv.org/abs/2602.06107) | [![GitHub](https://img.shields.io/github/stars/Infini-AI-Lab/jackpot?style=flat&label=GitHub)](https://github.com/Infini-AI-Lab/jackpot) |
| [Jet-RL: Enabling On-Policy FP8 Reinforcement Learning with Unified Training and Rollout Precision Flow](https://arxiv.org/abs/2601.14243) | arXiv 2026 | — |
| [LEGO-RL: Harness-Native Reinforcement Learning for Coding Agents](https://arxiv.org/abs/2608.17393) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/LegoX/Lego-RL?style=flat&label=GitHub)](https://github.com/LegoX/Lego-RL) |
| [Missing Old Logits in Asynchronous Agentic RL: Semantic Mismatch and Repair Methods for Off-Policy Correction](https://arxiv.org/abs/2605.12070) | arXiv 2026 | — |
| [QaRL: Rollout-Aligned Quantization-Aware RL for Fast and Stable Training under Training--Inference Mismatch](https://arxiv.org/abs/2604.07853) | [ACL 2026 (Findings)](https://aclanthology.org/2026.findings-acl.841/) | — |
| [QUADS: Stabilizing NVFP4 Reinforcement Learning for MoE via QUantization-error Alignment across Dual Sides](https://arxiv.org/abs/2607.15810) | arXiv 2026 | — |
| [QuRL: Efficient Reinforcement Learning with Quantized Rollout](https://arxiv.org/abs/2602.13953) | [ICLR 2026](https://arxiv.org/abs/2602.13953) | — |
| [Scaling Laws for Collapse in Asynchronous GRPO](https://arxiv.org/abs/2607.01083) | arXiv 2026 | — |
| [Sparrow: Sparse Rollout for Stable and Efficient Long-context RL of Large Language Models](https://arxiv.org/abs/2606.08446) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/Infini-AI-Lab/Sparrow?style=flat&label=GitHub)](https://github.com/Infini-AI-Lab/Sparrow) |
| [Sparse-RL: Breaking the Memory Wall in LLM Reinforcement Learning via Stable Sparse Rollouts](https://arxiv.org/abs/2601.10079) | [ACL 2026](https://aclanthology.org/2026.acl-long.2000/) | [![GitHub](https://img.shields.io/github/stars/RUCKBReasoning/Sparse-RL?style=flat&label=GitHub)](https://github.com/RUCKBReasoning/Sparse-RL) |
| [Stabilizing MoE Reinforcement Learning by Aligning Training and Inference Routers](https://arxiv.org/abs/2510.11370) | [ICML 2026](https://proceedings.mlr.press/v306/ma26aw.html) | — |
| [Asynchronous RLHF: Faster and More Efficient Off-Policy RL for Language Models](https://arxiv.org/abs/2410.18252) | [ICLR 2025](https://proceedings.iclr.cc/paper_files/paper/2025/hash/0b99315234cc95e6ef281f9155b68832-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/mnoukhov/async_rlhf?style=flat&label=GitHub)](https://github.com/mnoukhov/async_rlhf) |
| [Defeating the Training-Inference Mismatch via FP16](https://arxiv.org/abs/2510.26788) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/sail-sg/Precision-RL?style=flat&label=GitHub)](https://github.com/sail-sg/Precision-RL) |
| [Each Prompt Matters: Scaling Reinforcement Learning Without Wasting Rollouts on Hundred-Billion-Scale MoE](https://arxiv.org/abs/2512.07710) | arXiv 2025 | — |
| [Echo: Decoupling Inference and Training for Large-Scale RL Alignment on Heterogeneous Swarms](https://arxiv.org/abs/2508.05387) | arXiv 2025 | — |
| [MiniMax-M1: Scaling Test-Time Compute Efficiently with Lightning Attention](https://arxiv.org/abs/2506.13585) | arXiv 2025 | [Model / inference](https://github.com/MiniMax-AI/MiniMax-M1) |
| [Periodic Asynchrony: An On-Policy Approach for Accelerating LLM Reinforcement Learning](https://arxiv.org/abs/2511.18871) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/janelu9/EasyLLM?style=flat&label=GitHub)](https://github.com/janelu9/EasyLLM) |
| [Trajectory Balance with Asynchrony: Decoupling Exploration and Learning for Fast, Scalable LLM Post-Training](https://arxiv.org/abs/2503.18929) | [NeurIPS 2025](https://proceedings.neurips.cc/paper_files/paper/2025/hash/a58e6bd468ae63efd8c95035ea55ee41-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/bbartoldson/TBA?style=flat&label=GitHub)](https://github.com/bbartoldson/TBA) |

<a id="learning-stability"></a>

### Learning Stability

Regulate updates and preserve exploration and useful learning signals.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Abstention as an Action Can Kill Both the Reward Gradient and the KL Anchor: Collapse Law and Repair for Error-Penalized Reinforcement Learning](https://arxiv.org/abs/2608.00301) | arXiv 2026 | — |
| [Advantage Collapse in Group Relative Policy Optimization: Diagnosis and Mitigation](https://arxiv.org/abs/2605.21125) | [ICML 2026](https://arxiv.org/abs/2605.21125) | [![GitHub](https://img.shields.io/github/stars/hexixiang/Advantage-Collapse-Rate?style=flat&label=GitHub)](https://github.com/hexixiang/Advantage-Collapse-Rate) |
| [Dr. MAS: Stable Reinforcement Learning for Multi-Agent LLM Systems](https://arxiv.org/abs/2602.08847) | [NeurIPS 2026 (accepted)](https://arxiv.org/abs/2602.08847) | [![GitHub](https://img.shields.io/github/stars/langfengQ/DrMAS?style=flat&label=GitHub)](https://github.com/langfengQ/DrMAS) |
| [Explore More, Drift Less: Outcome-Only Reinforcement Learning Can Suffice for Long-Horizon Interactive Agents](https://arxiv.org/abs/2609.01245) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/AlibabaResearch/SignalCoverageRL?style=flat&label=GitHub)](https://github.com/AlibabaResearch/SignalCoverageRL) |
| [GRPO Training Dynamics for Small Language Models](https://arxiv.org/abs/2609.39321) | arXiv 2026 | — |
| [MoE Proxy Models for Low-Cost Failure Reproduction and Diagnosis in LLM RL Post-Training](https://arxiv.org/abs/2608.10823) | arXiv 2026 | — |
| [Performance, Efficiency and Collapse -- Advantages and Challenges in Offline Post-training of Code LLMs](https://arxiv.org/abs/2609.11956) | arXiv 2026 | — |
| [Probing RLVR training instability through the lens of objective-level hacking](https://arxiv.org/abs/2602.01103) | [ICML 2026](https://proceedings.mlr.press/v306/dong26b.html) | — |
| [RAGEN-2: Reasoning Collapse in Agentic RL](https://arxiv.org/abs/2604.06268) | [ICML 2026](https://proceedings.mlr.press/v306/wang26bn.html) | [![GitHub](https://img.shields.io/github/stars/mll-lab-nu/RAGEN?style=flat&label=GitHub)](https://github.com/mll-lab-nu/RAGEN) |
| [Self-Improvement Can Self-Regress: The Rise-and-Collapse Failure Mode of LLM Self-Training](https://arxiv.org/abs/2606.21090) | arXiv 2026 | — |
| [The Dark Room in the Reward Channel: Dense Prediction Rewards Collapse GRPO-Trained LLM Agents -- and The Channel, Not the Content, Decides What Works](https://arxiv.org/abs/2607.21273) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/RobertWangWang/verl-agent?style=flat&label=GitHub)](https://github.com/RobertWangWang/verl-agent) |
| [Towards Robust LLM Post-Training: Automatic Failure Management for Reinforcement Fine-Tuning](https://arxiv.org/abs/2605.04431) | arXiv 2026 | — |
| [Understanding Diversity Collapse in RLVR via the Lens of Overtraining](https://arxiv.org/abs/2606.15455) | arXiv 2026 | — |
| [When Does Multi-Agent RL Improve LLM Workflows? Workflow, Scale, and Policy-Sharing Tradeoffs](https://arxiv.org/abs/2605.24202) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/XHMY/marl-llm-workflows?style=flat&label=GitHub)](https://github.com/XHMY/marl-llm-workflows) |
| [DAPO: An Open-Source LLM Reinforcement Learning System at Scale](https://arxiv.org/abs/2503.14476) | [NeurIPS 2025](https://proceedings.nips.cc/paper_files/paper/2025/hash/a4277440d50f1f15d2cb4c14f7e0c0d2-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/verl-project/verl-recipe?style=flat&label=GitHub)](https://github.com/verl-project/verl-recipe/tree/main/dapo) |
| [Failure Modes of Maximum Entropy RLHF](https://arxiv.org/abs/2509.20265) | arXiv 2025 | — |
| [GLM-4.5V and GLM-4.1V-Thinking: Towards Versatile Multimodal Reasoning with Scalable Reinforcement Learning](https://arxiv.org/abs/2507.01006) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/zai-org/GLM-V?style=flat&label=GitHub)](https://github.com/zai-org/GLM-V) |
| [RAGEN: Understanding Self-Evolution in LLM Agents via Multi-Turn Reinforcement Learning](https://arxiv.org/abs/2504.20073) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/mll-lab-nu/RAGEN?style=flat&label=GitHub)](https://github.com/mll-lab-nu/RAGEN) |
| [Scaling Up RL: Unlocking Diverse Reasoning in LLMs via Prolonged Training](https://arxiv.org/abs/2507.12507) | arXiv 2025 | — |
| [ChatGLM-RLHF: Practices of Aligning Large Language Models with Human Feedback](https://arxiv.org/abs/2404.00934) | arXiv 2024 | — |

<a id="training-recovery"></a>

### Training Recovery

Preserve checkpoints and isolate or recover from runtime failures.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Laminar: A Scalable Asynchronous RL Post-Training Framework](https://arxiv.org/abs/2510.12633) | [EuroSys 2026](https://doi.org/10.1145/3767295.3803580) | [![GitHub](https://img.shields.io/github/stars/verl-project/laminar?style=flat&label=GitHub)](https://github.com/verl-project/laminar) |
| [Role-Based Fault Tolerance System for LLM RL Post-Training](https://arxiv.org/abs/2512.22492) | arXiv 2025 | — |
| [WeChat-YATT: A Scalable, Simple, Efficient, and Production Ready Training Library](https://arxiv.org/abs/2508.07970) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/tencent/WeChat-YATT?style=flat&label=GitHub)](https://github.com/tencent/WeChat-YATT) |

[Back to taxonomy](#taxonomy)

<a id="model-evaluation"></a>

## Model Evaluation

Validate gains and risks to inform checkpoint and change acceptance.

28 papers

<a id="capability-validation"></a>

### Capability Validation

Establish evaluation validity, gain attribution, and reproducibility.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Agent^2 RL-Bench: Can LLM Agents Engineer Agentic RL Post-Training?](https://arxiv.org/abs/2604.10547) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/microsoft/RD-Agent?style=flat&label=GitHub)](https://github.com/microsoft/RD-Agent/tree/main/rdagent/scenarios/rl/autorl_bench) |
| [DataFlex-RL: An Evaluation Platform for RLVR Data Policies](https://arxiv.org/abs/2609.06107) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/haolpku/DataFlex-RL?style=flat&label=GitHub)](https://github.com/haolpku/DataFlex-RL) |
| [From Reward Signal to Visual Utility: A Controlled Audit of Medical VLM Post-Training](https://arxiv.org/abs/2609.31450) | arXiv 2026 | — |
| [Measuring Reward Hacking and Reasoning-Answer Decoupling Under Position-Confounded Optimization](https://arxiv.org/abs/2608.15445) | [COLM 2026 (AI Measurement Science Workshop)](https://arxiv.org/abs/2608.15445) | — |
| [Reach or Solve? Deep Diving into Agentic RL Gains with Checkpoint Handoffs](https://arxiv.org/abs/2609.19636) | arXiv 2026 | — |
| [A Sober Look at Progress in Language Model Reasoning: Pitfalls and Paths to Reproducibility](https://arxiv.org/abs/2504.07086) | [COLM 2025](https://arxiv.org/abs/2504.07086) | [![GitHub](https://img.shields.io/github/stars/bethgelab/sober-reasoning?style=flat&label=GitHub)](https://github.com/bethgelab/sober-reasoning) |
| [Local Coherence or Global Validity? Investigating RLVR Traces in Math Domains](https://arxiv.org/abs/2510.18176) | arXiv 2025 | — |
| [Rethinking RL Scaling for Vision Language Models: A Transparent, From-Scratch Framework and Comprehensive Evaluation Scheme](https://arxiv.org/abs/2504.02587) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/GAIR-NLP/MAYE?style=flat&label=GitHub)](https://github.com/GAIR-NLP/MAYE) |

<a id="risk-auditing"></a>

### Risk Auditing

Audit regressions, unsafe behavior, privacy exposure, and reasoning monitorability.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Detecting Data Contamination from Reinforcement Learning Post-training for Large Language Models](https://arxiv.org/abs/2510.09259) | [ICLR 2026](https://arxiv.org/abs/2510.09259) | [![GitHub](https://img.shields.io/github/stars/yongding-tao/RL-Data-Contamination?style=flat&label=GitHub)](https://github.com/yongding-tao/RL-Data-Contamination) |
| [Detecting RLVR Training Data via Structural Convergence of Reasoning](https://arxiv.org/abs/2602.11792) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/StevenZHB/Detect_RLVR_Data?style=flat&label=GitHub)](https://github.com/StevenZHB/Detect_RLVR_Data) |
| [GRPO Beyond English: A Large-Scale Study of GRPO in Non-English and Multilingual Settings](https://arxiv.org/abs/2608.13698) | arXiv 2026 | — |
| [How LLM Task-Adaptation Reshapes Alignment: A Multi-dimensional Study of Behavioral and Representational Drift](https://arxiv.org/abs/2607.22676) | arXiv 2026 | — |
| [Length Penalties Make Chain-of-Thought Less Monitorable](https://arxiv.org/abs/2607.09786) | arXiv 2026 | — |
| [Mapping Post-Training Forgetting in Language Models at Scale](https://arxiv.org/abs/2510.17776) | [ICLR 2026](https://proceedings.iclr.cc/paper_files/paper/2026/hash/bc1c5e5fb8ed1ef9b9b5abced2022e40-Abstract-Conference.html) | [![GitHub](https://img.shields.io/github/stars/post-forget/post-forget?style=flat&label=GitHub)](https://github.com/post-forget/post-forget) |
| [Monitorability as a Free Gift: How RLVR Spontaneously Aligns Reasoning](https://arxiv.org/abs/2602.03978) | [ICML 2026](https://proceedings.mlr.press/v306/xiong26b.html) | [![GitHub](https://img.shields.io/github/stars/polaris-73/monitorability_as_a_free_gift?style=flat&label=GitHub)](https://github.com/polaris-73/monitorability_as_a_free_gift) |
| [No Free Efficiency: Revisiting the Trade-off Between Training Efficiency and Model Vulnerability](https://arxiv.org/abs/2609.33898) | arXiv 2026 | — |
| [Where does output diversity collapse in post-training?](https://arxiv.org/abs/2604.16027) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/ckarouzos/where-diversity-collapses?style=flat&label=GitHub)](https://github.com/ckarouzos/where-diversity-collapses) |
| [Auditing Data Membership in Reinforcement Learning With Verifiable Rewards](https://arxiv.org/abs/2511.14045) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/Y-L-LIU/Divergence-in-Behavior-Attack?style=flat&label=GitHub)](https://github.com/Y-L-LIU/Divergence-in-Behavior-Attack) |
| [Auditing language models for hidden objectives](https://arxiv.org/abs/2503.10965) | arXiv 2025 | — |
| [Cross-lingual Collapse: How Language-Centric Foundation Models Shape Reasoning in Large Language Models](https://arxiv.org/abs/2506.05850) | arXiv 2025 | — |
| [Natural Emergent Misalignment from Reward Hacking in Production RL](https://arxiv.org/abs/2511.18397) | arXiv 2025 | — |

<a id="version-acceptance"></a>

### Version Acceptance

Use evaluation evidence to retain checkpoints and accept or reject changes.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [CharacterFlywheel: Scaling Iterative Improvement of Engaging and Steerable LLMs in Production](https://arxiv.org/abs/2603.01973) | arXiv 2026 | — |
| [EvalStop: Using World Feedback to Detect and Correct Reward Overoptimization in Multi-Tenant RLHF Platforms](https://arxiv.org/abs/2606.04145) | arXiv 2026 | — |
| [EvoTrainer: Co-Evolving LLM Policies and Training Harnesses for Autonomous Agentic Reinforcement Learning](https://arxiv.org/abs/2606.03108) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/AlibabaResearch/DAMO-ConvAI?style=flat&label=GitHub)](https://github.com/AlibabaResearch/DAMO-ConvAI/tree/main/EvoTrainer) |
| [MERA: Model Evolution and Routing with Skill Adaptation for Agentic Systems at Scale](https://arxiv.org/abs/2608.10333) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/yh-yao/MERA-Evolve?style=flat&label=GitHub)](https://github.com/yh-yao/MERA-Evolve) |
| [SafeEvolve: Harness-Policy Co-Evolution from Agent Experience for Safety Alignment](https://arxiv.org/abs/2609.02786) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/MaoPopovich/SafeEvolve?style=flat&label=GitHub)](https://github.com/MaoPopovich/SafeEvolve) |
| [VACE: Validation-Gated Alternating Co-Evolution of Agent Models and Harnesses](https://arxiv.org/abs/2609.37105) | arXiv 2026 | — |
| [Uncertainty-Guided Checkpoint Selection for Reinforcement Finetuning of Large Language Models](https://arxiv.org/abs/2511.09864) | arXiv 2025 | — |

[Back to taxonomy](#taxonomy)

<a id="open-source-resources"></a>

## Open-source Resources

| Project | Operational role | Repository |
| --- | --- | :---: |
| [verl](https://github.com/verl-project/verl) | Flexible distributed RL post-training and HybridFlow execution. | [![GitHub](https://img.shields.io/github/stars/verl-project/verl?style=flat&label=GitHub)](https://github.com/verl-project/verl) |
| [OpenRLHF](https://github.com/OpenRLHF/OpenRLHF) | Distributed RLHF and agentic RL training infrastructure. | [![GitHub](https://img.shields.io/github/stars/OpenRLHF/OpenRLHF?style=flat&label=GitHub)](https://github.com/OpenRLHF/OpenRLHF) |
| [AReaL](https://github.com/areal-project/AReaL) | Asynchronous RL training for language models and agents. | [![GitHub](https://img.shields.io/github/stars/areal-project/AReaL?style=flat&label=GitHub)](https://github.com/areal-project/AReaL) |
| [Trinity-RFT](https://github.com/agentscope-ai/Trinity-RFT) | General-purpose reinforcement fine-tuning workflows. | [![GitHub](https://img.shields.io/github/stars/agentscope-ai/Trinity-RFT?style=flat&label=GitHub)](https://github.com/agentscope-ai/Trinity-RFT) |
| [RLinf](https://github.com/RLinf/RLinf) | RL infrastructure with language-reasoning and agentic workloads; also supports embodied settings. | [![GitHub](https://img.shields.io/github/stars/RLinf/RLinf?style=flat&label=GitHub)](https://github.com/RLinf/RLinf) |
| [Agent Lightning](https://github.com/microsoft/agent-lightning) | Connects agent execution and trajectory collection with RL training. | [![GitHub](https://img.shields.io/github/stars/microsoft/agent-lightning?style=flat&label=GitHub)](https://github.com/microsoft/agent-lightning) |
| [NeMo RL](https://github.com/NVIDIA-NeMo/RL) | Scalable post-training infrastructure for language and multimodal models. | [![GitHub](https://img.shields.io/github/stars/NVIDIA-NeMo/RL?style=flat&label=GitHub)](https://github.com/NVIDIA-NeMo/RL) |
| [TRL](https://github.com/huggingface/trl) | Transformer post-training library with reinforcement-learning trainers. | [![GitHub](https://img.shields.io/github/stars/huggingface/trl?style=flat&label=GitHub)](https://github.com/huggingface/trl) |
| [trlX](https://github.com/CarperAI/trlx) | Distributed RLHF training framework. | [![GitHub](https://img.shields.io/github/stars/CarperAI/trlx?style=flat&label=GitHub)](https://github.com/CarperAI/trlx) |
| [DeepSpeed-Chat](https://github.com/deepspeedai/DeepSpeedExamples) | DeepSpeed examples include the DeepSpeed-Chat RLHF training pipeline. | [![GitHub](https://img.shields.io/github/stars/deepspeedai/DeepSpeedExamples?style=flat&label=GitHub)](https://github.com/deepspeedai/DeepSpeedExamples) |
| [slime](https://github.com/THUDM/slime) | RL training infrastructure focused on scalable rollout and training execution. | [![GitHub](https://img.shields.io/github/stars/THUDM/slime?style=flat&label=GitHub)](https://github.com/THUDM/slime) |

<a id="related-surveys"></a>

## Related Surveys

Reviews of earlier RLOps, AgentOps, reliability, and self-improvement safety provide complementary context.

| Survey | Year | Focus |
| --- | :---: | --- |
| [Agent System Operations: Categorization, Challenges, and Future Directions](https://arxiv.org/abs/2606.01581) | 2026 | Operations of agent systems beyond the RL training run. |
| [Diving into reliable self-evolving agents: A survey](https://wkqdzkd.github.io/Awesome-Reliable-Self-Evolving-Agents/) | 2026 | Reliability of self-evolving agents. |
| [Evolutionary Safety of Recursive Self-Improving AI: Taxonomy, Risk Discovery, and Evaluation](https://arxiv.org/abs/2609.31186) | 2026 | Safety risks and evaluation in recursive self-improvement. |
| [Safety in Self-Evolving Agents: A Survey](https://arxiv.org/abs/2610.00093) | 2026 | Safety considerations for self-evolving agents. |
| [Trustworthy Recursive Self-Improvement in the Era of Large Models: Foundation, Risks, Evaluation and Open Challenges](https://arxiv.org/abs/2610.35193) | 2026 | Trustworthiness, evaluation, and oversight across self-improvement cycles. |
| [Rlops: Development life-cycle of reinforcement learning aided open ran](https://arxiv.org/abs/2111.06978) | 2022 | Earlier RLOps lifecycle practices in Open RAN. |

<a id="citation"></a>

## Citation
