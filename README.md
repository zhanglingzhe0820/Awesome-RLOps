# Awesome-RLOps

Papers and open resources on **operations management throughout the LLM reinforcement learning training lifecycle**.

**312 papers · 5 stages · 18 topics · 11 open-source resources**  
Last updated: 2026-11-16

<a id="our-survey"></a>

## Our Survey

Our survey organizes LLM RLOps around Training Setup, Experience Collection, Reward Computation, Policy Optimization, and Model Evaluation. It connects resource and execution management with feedback reliability, learning stability, failure recovery, and validation of training outcomes.

The manuscript is being prepared; its paper link and citation will be added when public.

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
- [Contributing](#contributing)
- [Citation](#citation)

All papers are indexed together by their main operational contribution. Categories describe operational contributions; a system may contribute to several topics and is listed under its main contribution. Entries are ordered by publication year, newest first. A dash in the Code column means that an official code link has not been verified for that entry.

<a id="training-setup"></a>

## Training Setup

Prepare resources, configuration, the starting model, and training inputs.

41 papers

<a id="computational-resources"></a>

### Computational Resources

Estimate resource demand, predict compute returns, and allocate training budgets.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [ECHO-2: A Large-Scale Distributed Rollout Framework for Cost-Efficient Reinforcement Learning](https://arxiv.org/abs/2602.02192) | arXiv 2026 | — |
| [IsoCompute Playbook: Optimally Scaling Sampling Compute for LLM RL](https://arxiv.org/abs/2603.12151) | arXiv 2026 | — |
| [On Effectiveness and Efficiency of Agentic Tool-calling and RL Training](https://arxiv.org/abs/2606.00135) | arXiv 2026 | — |
| [Scaling Behaviors of LLM Reinforcement Learning Post-Training: An Empirical Study in Mathematical Reasoning](https://arxiv.org/abs/2509.25300) | ACL 2026 | — |
| [sGPO: Trading Inference FLOPs for Training Efficiency in RLVR](https://arxiv.org/abs/2606.08854) | arXiv 2026 | — |
| [The Art of Scaling Reinforcement Learning Compute for LLMs](https://arxiv.org/abs/2510.13786) | ICLR 2026 | — |
| [The Rollout Infrastructure Tax in Coding-Agent Reinforcement Learning](https://arxiv.org/abs/2607.01415) | arXiv 2026 | — |
| [Agent RL Scaling Law: Agent RL with Spontaneous Code Execution for Mathematical Problem Solving](https://arxiv.org/abs/2505.07773) | arXiv 2025 | — |
| [Predictive Scaling Laws for Efficient GRPO Training of Large Reasoning Models](https://arxiv.org/abs/2507.18014) | arXiv 2025 | — |
| [Does RLHF Scale? Exploring the Impacts From Data, Model, and Method](https://arxiv.org/abs/2412.06000) | arXiv 2024 | — |

<a id="run-configuration"></a>

### Run Configuration

Compare, search, and validate executable training configurations.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [AlignTune: Modular Toolkit for Post-Training Alignment of Large Language Models](https://arxiv.org/abs/2602.09621) | arXiv 2026 | — |
| [Automatic Configuration of LLM Post-Training Pipelines](https://arxiv.org/abs/2603.18773) | arXiv 2026 | — |
| [Efficient Hyperparameter Optimization for LLM Reinforcement Learning](https://arxiv.org/abs/2606.03073) | ACL 2026 | — |
| [How Much Online RL is Enough? Informative Rollouts for Offline Preference Optimization in RLVR](https://arxiv.org/abs/2605.21266) | arXiv 2026 | — |
| [How to Train Your LLM Web Agent: A Statistical Diagnosis](https://arxiv.org/abs/2507.04103) | NeurIPS 2026 | — |
| [MemFactory: Unified Inference & Training Framework for Agent Memory](https://arxiv.org/abs/2603.29493) | arXiv 2026 | — |
| [NebulaExp-8B: An Empirical Post-Training Pipeline via Full-Scale Ablation Research](https://arxiv.org/abs/2606.26671) | arXiv 2026 | — |
| [Towards Robust Reinforcement Learning for Small-Scale Language Model Agents](https://arxiv.org/abs/2607.25091) | arXiv 2026 | — |
| [UnityMAS-O: A General RL Optimization Framework for LLM-Based Multi-Agent Systems](https://arxiv.org/abs/2605.26646) | arXiv 2026 | — |
| [When Do Larger Batches Help Scale LLM Reinforcement Learning?](https://arxiv.org/abs/2608.29296) | arXiv 2026 | — |
| [JustRL: Scaling a 1.5B LLM with a Simple RL Recipe](https://arxiv.org/abs/2512.16649) | arXiv 2025 | — |
| [Nemotron-Cascade: Scaling Cascaded Reinforcement Learning for General-Purpose Reasoning Models](https://arxiv.org/abs/2512.13607) | arXiv 2025 | — |
| [Unpacking DPO and PPO: Disentangling Best Practices for Learning from Preference Feedback](https://arxiv.org/abs/2406.09279) | NeurIPS 2024 | — |

<a id="base-model"></a>

### Base Model

Select and prepare a model checkpoint suitable for the intended RL run.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Clipping Low-Probability Tokens in SFT Yields a Generalizable Initialization for RL](https://proceedings.mlr.press/v306/liu26bm.html) | ICML 2026 | — |
| [Good SFT Optimizes for SFT, Better SFT Prepares for Reinforcement Learning](https://arxiv.org/abs/2602.01058) | arXiv 2026 | — |
| [Quagmires in SFT-RL Post-Training: When High SFT Scores Mislead and What to Use Instead](https://arxiv.org/abs/2510.01624) | ICLR 2026 | — |
| [SFT Overtraining Predicts Rank Inversion via Entropy Collapse Under RLVR](https://arxiv.org/abs/2606.18487) | arXiv 2026 | — |
| [Teaching Thinking Models to Reason with Tools: A Full-Pipeline Recipe for Tool-Integrated Reasoning](https://arxiv.org/abs/2605.06326) | arXiv 2026 | — |
| [When RL Fails after SFT: Rejuvenating Model Plasticity for Robust SFT-to-RL Handoff](https://arxiv.org/abs/2606.09932) | arXiv 2026 | — |
| [SimpleRL-Zoo: Investigating and Taming Zero Reinforcement Learning for Open Base Models in the Wild](https://arxiv.org/abs/2503.18892) | arXiv 2025 | — |

<a id="training-data"></a>

### Training Data

Select informative tasks, validate input quality, and allocate annotation effort.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Agent-World: Scaling Real-World Environment Synthesis for Evolving General Agent Intelligence](https://arxiv.org/abs/2604.18292) | arXiv 2026 | — |
| [DE-Venus: A Data-Efficient RLVR Framework for Large Language Models](https://arxiv.org/abs/2609.03324) | arXiv 2026 | — |
| [SCALECUA: Scaling Computer Use Agents with Verifiable Task Synthesis and Efficient Online RL](https://arxiv.org/abs/2607.11185) | arXiv 2026 | — |
| [Scaling Near-Optimal SFT-RL Annotation Budget Allocation from Small to Large LLMs](https://arxiv.org/abs/2609.01573) | EMNLP 2026 | — |
| [Smart Picks in the Dark: Towards Efficient RLVR for Reasoning via Tracing Metacognitive Pivots](https://arxiv.org/abs/2606.04503) | arXiv 2026 | — |
| [Survive or Collapse: The Asymmetric Roles of Data Gating and Reward Grounding in Self-Play RL](https://arxiv.org/abs/2605.22217) | arXiv 2026 | — |
| [Teach the Way It Thinks: Guiding LLM Post-training Data Engineering with Sparse Autoencoders](https://arxiv.org/abs/2605.27354) | arXiv 2026 | — |
| [UFO-RL: Uncertainty-Focused Optimization for Efficient Reinforcement Learning Data Selection](https://arxiv.org/abs/2505.12457) | NeurIPS 2026 | — |
| [INTELLECT-2: A Reasoning Model Trained Through Globally Decentralized Reinforcement Learning](https://arxiv.org/abs/2505.07291) | arXiv 2025 | — |
| [Towards High Data Efficiency in Reinforcement Learning with Verifiable Reward](https://arxiv.org/abs/2509.01321) | arXiv 2025 | — |
| [Truth in the Few: High-Value Data Selection for Efficient Multi-Modal Reasoning](https://arxiv.org/abs/2506.04755) | arXiv 2025 | — |

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
| [BOTS: A Unified Framework for Bayesian Online Task Selection in LLM Reinforcement Finetuning](https://arxiv.org/abs/2510.26374) | ICLR 2026 | — |
| [Can Prompt Difficulty be Online Predicted for Accelerating RL Finetuning of Reasoning Models?](https://arxiv.org/abs/2507.04632) | KDD 2026 | — |
| [Cross-Epoch Adaptive Rollout Optimization for RL Post-Training](https://arxiv.org/abs/2606.05606) | arXiv 2026 | — |
| [DARTS: Distribution-Aware Active Rollout Trajectory Shaping for Accelerating LLM Reinforcement Learning](https://arxiv.org/abs/2605.30859) | arXiv 2026 | — |
| [Dual-Loop Self-Evolution via Verifiable Emotion Feedback for Multi-Turn Empathetic Dialogue](https://arxiv.org/abs/2608.10626) | arXiv 2026 | — |
| [Early Verdicts, Better Budgets: Sequential Adaptive Rollout Allocation for Compute-Efficient RLVR](https://arxiv.org/abs/2607.26253) | arXiv 2026 | — |
| [Efficient RLVR Scheduling via Graph-Structured Online Difficulty Estimation](https://arxiv.org/abs/2608.17941) | arXiv 2026 | — |
| [Efficient RLVR Training via Weighted Mutual Information Data Selection](https://arxiv.org/abs/2603.01907) | arXiv 2026 | — |
| [HarnessBandit: Joint Learnability-Transferability Scheduling for Multi-Harness Agentic Reinforcement Learning](https://arxiv.org/abs/2609.13739) | arXiv 2026 | — |
| [Kalman Meets Curriculum: Efficient Dynamic Prompt Selection for Adaptive RL Finetuning](https://arxiv.org/abs/2607.27610) | arXiv 2026 | — |
| [LEAP: Lean Environment-Feedback via Adaptive Pruning for Code RL in GPU Kernel Generation](https://arxiv.org/abs/2608.01804) | arXiv 2026 | — |
| [Learning as Reasoning Unfolds: Progressive Rollout Allocation for Efficient Reinforcement Learning](https://arxiv.org/abs/2607.22002) | arXiv 2026 | — |
| [Learning-Zone Energy: Online Data Selection for Efficient RL Post-Training](https://arxiv.org/abs/2605.17003) | arXiv 2026 | — |
| [LEEPS: Latent-Guided Explore-Exploit Prompt Sampling for Efficient RLVR in Large Language Models](https://arxiv.org/abs/2607.28077) | arXiv 2026 | — |
| [Optimizing What Policies Learn From: Recoverability-aware Rollout Intervention Learning](https://arxiv.org/abs/2608.05080) | arXiv 2026 | — |
| [PAIR: Pairwise-Aware Inclusion Reweighting for Adaptive Rollout Allocation in RLVR](https://arxiv.org/abs/2608.11368) | arXiv 2026 | — |
| [Prompt Curriculum Learning for Efficient LLM Post-Training](https://arxiv.org/abs/2510.01135) | ICLR 2026 | — |
| [Prune as You Generate: Online Rollout Pruning for Faster and Better RLVR](https://arxiv.org/abs/2603.24840) | ACL 2026 | — |
| [Selective Rollout: Mid-Trajectory Termination for Multi-Sample Agent RL](https://arxiv.org/abs/2605.05802) | arXiv 2026 | — |
| [SENTINEL: Failure-Driven Reinforcement Learning for Training Tool-Using Language Model Agents](https://arxiv.org/abs/2606.12908) | arXiv 2026 | — |
| [Small Generalizable Prompt Predictive Models Can Steer Efficient RL Post-Training of Large Reasoning Models](https://arxiv.org/abs/2602.01970) | arXiv 2026 | — |
| [Spend Your Rollouts Where It Counts: Rollout Allocation for Group-Based RL Post-Training](https://arxiv.org/abs/2605.26606) | arXiv 2026 | — |
| [ThinkPrior: Zero-Rollout Difficulty Priors for Cold-Start Prompt Selection in RLVR](https://arxiv.org/abs/2609.09075) | arXiv 2026 | — |
| [TRACE: A Unified Rollout Budget Allocation Framework for Efficient Agentic Reinforcement Learning](https://arxiv.org/abs/2606.11119) | arXiv 2026 | — |
| [Train at Moving Edge: Online-Verified Prompt Selection for Efficient RL Training of Large Reasoning Model](https://arxiv.org/abs/2603.25184) | arXiv 2026 | — |
| [Train Less, Learn More: Adaptive Efficient Rollout Optimization for Group-Based Reinforcement Learning](https://arxiv.org/abs/2602.14338) | arXiv 2026 | — |
| [Where to Spend Rollouts: Hit-Utility Optimal Rollout Allocation for Group-Based RLVR](https://arxiv.org/abs/2605.07114) | arXiv 2026 | — |
| [Act Only When It Pays: Efficient Reinforcement Learning for LLM Reasoning via Selective Rollouts](https://arxiv.org/abs/2506.02177) | NeurIPS 2025 | — |
| [Data-Efficient RLVR via Off-Policy Influence Guidance](https://arxiv.org/abs/2510.26491) | arXiv 2025 | — |
| [OptPO: Optimal Rollout Allocation for Test-time Policy Optimization](https://arxiv.org/abs/2512.02882) | arXiv 2025 | — |
| [Reinforce-Ada: An Adaptive Sampling Framework under Non-linear RL Objectives](https://arxiv.org/abs/2510.04996) | arXiv 2025 | — |

<a id="rollout-execution-optimization"></a>

### Rollout Execution Optimization

Improve generation throughput, scheduling, and resource use.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Accelerating Long-Tail Generation in Synchronous RLHF Training via Adaptive Tensor Parallelism](https://arxiv.org/abs/2605.23945) | arXiv 2026 | — |
| [Accelerating RL Post-Training Rollouts via System-Integrated Speculative Decoding](https://arxiv.org/abs/2604.26779) | arXiv 2026 | — |
| [AReaL: A Large-Scale Asynchronous Reinforcement Learning System for Language Reasoning](https://arxiv.org/abs/2505.24298) | NeurIPS 2026 | [![GitHub](https://img.shields.io/github/stars/areal-project/AReaL?style=flat&label=GitHub)](https://github.com/areal-project/AReaL) |
| [Breaking Entropy Bounds: Accelerating RL Training via MTP with Rejection Sampling](https://arxiv.org/abs/2606.12370) | arXiv 2026 | — |
| [BubbleSpec: Turning Long-Tail Bubbles into Speculative Rollout Drafts for Synchronous Reinforcement Learning](https://arxiv.org/abs/2605.08862) | arXiv 2026 | — |
| [DORA: A Scalable Asynchronous Reinforcement Learning System for Language Model Training](https://arxiv.org/abs/2604.26256) | arXiv 2026 | — |
| [DynaResize: Runtime GPU Reallocation for Disaggregated LLM Post-Training](https://arxiv.org/abs/2607.22614) | arXiv 2026 | — |
| [EfficientRollout: System-Aware Self-Speculative Decoding for RL Rollouts](https://arxiv.org/abs/2606.18967) | arXiv 2026 | — |
| [Heddle: A Distributed Orchestration System for Agentic RL Rollout](https://arxiv.org/abs/2603.28101) | arXiv 2026 | — |
| [Moebius: Serving Mixture-of-Expert Models with Seamless Runtime Parallelism Switch](https://arxiv.org/abs/2606.26607) | arXiv 2026 | — |
| [RLHFless: Serverless Computing for Efficient RLHF](https://arxiv.org/abs/2602.22718) | arXiv 2026 | — |
| [ROSE: Rollout On Serving GPUs via Cooperative Elasticity for Agentic RL](https://arxiv.org/abs/2605.06534) | arXiv 2026 | — |
| [Scheduling Mixed RL Rollouts Beyond Prefix Locality](https://arxiv.org/abs/2608.11152) | arXiv 2026 | — |
| [SortedRL: Accelerating RL Training for LLMs through Online Length-Aware Scheduling](https://arxiv.org/abs/2603.23414) | arXiv 2026 | — |
| [SPARK: Learning from Verification in Speculative GRPO Rollouts](https://arxiv.org/abs/2608.04962) | arXiv 2026 | — |
| [SRT: Accelerating Reinforcement Learning via Speculative Rollout with Tree-Structured Cache](https://arxiv.org/abs/2601.09083) | arXiv 2026 | — |
| [TailSieve: Partial-Rollout-Guided Tail Routing for LLM Rollouts](https://arxiv.org/abs/2608.22788) | arXiv 2026 | — |
| [ThunderAgent: A Simple, Fast and Program-Aware Agentic Inference System](https://arxiv.org/abs/2602.13692) | arXiv 2026 | — |
| [AgentRL: Scaling Agentic Reinforcement Learning with a Multi-Turn, Multi-Task Framework](https://arxiv.org/abs/2510.04206) | arXiv 2025 | — |
| [APRIL: Active Partial Rollouts in Reinforcement Learning to Tame Long-tail Generation](https://arxiv.org/abs/2509.18521) | arXiv 2025 | — |
| [Beat the long tail: Distribution-Aware Speculative Decoding for RL Training](https://arxiv.org/abs/2511.13841) | arXiv 2025 | — |
| [Beyond Ten Turns: Unlocking Long-Horizon Agentic Search with Large-Scale Asynchronous RL](https://arxiv.org/abs/2508.07976) | arXiv 2025 | — |
| [CoPRIS: Efficient and Stable Reinforcement Learning via Concurrency-Controlled Partial Rollout with Importance Sampling](https://arxiv.org/abs/2511.05589) | arXiv 2025 | — |
| [DistRL: An Asynchronous Distributed Reinforcement Learning Framework for On-Device Control Agents](https://arxiv.org/abs/2410.14803) | ICLR 2025 | — |
| [EARL: Efficient Agentic Reinforcement Learning Systems for Large Language Models](https://arxiv.org/abs/2510.05943) | arXiv 2025 | — |
| [Efficient Multi-turn RL for GUI Agents via Decoupled Training and Adaptive Data Curation](https://arxiv.org/abs/2509.23866) | arXiv 2025 | — |
| [FastGRPO: Accelerating Policy Optimization via Concurrency-aware Speculative Decoding and Online Draft Learning](https://arxiv.org/abs/2509.21792) | arXiv 2025 | — |
| [History Rhymes: Accelerating LLM Reinforcement Learning with RhymeRL](https://arxiv.org/abs/2508.18588) | arXiv 2025 | — |
| [Infinite Sampling: Efficient and Stable Grouped RL Training for Large Language Models](https://arxiv.org/abs/2506.22950) | arXiv 2025 | — |
| [Kimi k1.5: Scaling Reinforcement Learning with LLMs](https://arxiv.org/abs/2501.12599) | arXiv 2025 | — |
| [Klear-AgentForge: Forging Agentic Intelligence through Posttraining Scaling](https://arxiv.org/abs/2511.05951) | arXiv 2025 | — |
| [Native Parallel Reasoner: Reasoning in Parallelism via Self-Distilled Reinforcement Learning](https://arxiv.org/abs/2512.07461) | arXiv 2025 | — |
| [OPPO: Accelerating PPO-based RLHF via Pipeline Overlap](https://arxiv.org/abs/2509.25762) | arXiv 2025 | — |
| [Part II: ROLL Flash -- Accelerating RLVR and Agentic Training with Asynchrony](https://arxiv.org/abs/2510.11345) | arXiv 2025 | — |
| [QeRL: Beyond Efficiency -- Quantization-enhanced Reinforcement Learning for LLMs](https://arxiv.org/abs/2510.11696) | arXiv 2025 | — |
| [RECON: Reasoning with Condensation for Efficient Retrieval-Augmented Generation](https://arxiv.org/abs/2510.10448) | arXiv 2025 | — |
| [ReSpec: Towards Optimizing Speculative Decoding in Reinforcement Learning Systems](https://arxiv.org/abs/2510.26475) | arXiv 2025 | — |
| [RLBoost: Harvesting Preemptible Resources for Cost-Efficient Reinforcement Learning on LLMs](https://arxiv.org/abs/2510.19225) | arXiv 2025 | — |
| [RLHFSpec: Breaking the Efficiency Bottleneck in RLHF Training via Adaptive Drafting](https://arxiv.org/abs/2512.04752) | arXiv 2025 | — |
| [RollPacker: Mitigating Long-Tail Rollouts for Fast, Synchronous RL Post-Training](https://arxiv.org/abs/2509.21009) | arXiv 2025 | — |
| [Scaling RL to Long Videos](https://arxiv.org/abs/2507.07966) | arXiv 2025 | — |
| [SkyRL-Agent: Efficient RL Training for Multi-turn LLM Agent](https://arxiv.org/abs/2511.16108) | arXiv 2025 | — |
| [SPEC-RL: Accelerating On-Policy Reinforcement Learning with Speculative Rollouts](https://arxiv.org/abs/2509.23232) | arXiv 2025 | — |
| [StreamRL: Scalable, Heterogeneous, and Elastic RL for LLMs with Disaggregated Stream Generation](https://arxiv.org/abs/2504.15930) | arXiv 2025 | — |
| [Taming the Long-Tail: Efficient Reasoning RL Training with Adaptive Drafter](https://arxiv.org/abs/2511.16665) | arXiv 2025 | — |
| [The Markovian Thinker: Architecture-Agnostic Linear Scaling of Reasoning](https://arxiv.org/abs/2510.06557) | arXiv 2025 | — |
| [TreePO: Bridging the Gap of Policy Optimization and Efficacy and Inference Efficiency with Heuristic Tree-based Modeling](https://arxiv.org/abs/2508.17445) | arXiv 2025 | — |
| [OpenRLHF: An Easy-to-use, Scalable and High-performance RLHF Framework](https://arxiv.org/abs/2405.11143) | arXiv 2024 | [![GitHub](https://img.shields.io/github/stars/OpenRLHF/OpenRLHF?style=flat&label=GitHub)](https://github.com/OpenRLHF/OpenRLHF) |

<a id="environment-reliability"></a>

### Environment Reliability

Maintain interaction availability, isolation, reproducibility, and simulator fidelity.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [ARL-Tangram: Unleash the Resource Efficiency in Agentic Reinforcement Learning](https://arxiv.org/abs/2603.13019) | arXiv 2026 | — |
| [Belayer: Efficient Fault Tolerance for LLM Agentic RL Training](https://arxiv.org/abs/2608.14635) | arXiv 2026 | — |
| [Crab: A Semantics-Aware Checkpoint/Restore Runtime for Agent Sandboxes](https://arxiv.org/abs/2604.28138) | arXiv 2026 | — |
| [DeepSeek Elastic Compute (DSec): A Sandbox Infrastructure for Effective Agentic Training at Scale](https://arxiv.org/abs/2609.22978) | arXiv 2026 | — |
| [DeltaBox: Scaling Stateful AI Agents with Millisecond-Level Sandbox Checkpoint/Rollback](https://arxiv.org/abs/2605.22781) | arXiv 2026 | — |
| [LiteResearcher: A Scalable Agentic RL Training Framework for Deep Research Agent](https://arxiv.org/abs/2604.17931) | arXiv 2026 | — |
| [MCP-Universe RL: A Framework for Training MCP Tool-Use Agents via Reinforcement Learning](https://arxiv.org/abs/2608.22167) | arXiv 2026 | — |
| [One Frozen Simulator Is Not Enough: Simulator Collapse in Multi-Agent RL](https://arxiv.org/abs/2608.12253) | arXiv 2026 | — |
| [Orchard: An Open-Source Agentic Modeling Framework](https://arxiv.org/abs/2605.15040) | arXiv 2026 | — |
| [ProRL Agent: Rollout-as-a-Service for RL Training of Multi-Turn LLM Agents](https://arxiv.org/abs/2603.18815) | arXiv 2026 | — |
| [REDSearcher: A Scalable and Cost-Efficient Framework for Long-Horizon Search Agents](https://arxiv.org/abs/2602.14234) | arXiv 2026 | — |
| [Synthetic Sandbox for Training Machine Learning Engineering Agents](https://arxiv.org/abs/2604.04872) | arXiv 2026 | — |
| [Weblica: Scalable and Reproducible Training Environments for Visual Web Agents](https://arxiv.org/abs/2605.06761) | arXiv 2026 | — |
| [AgentFly: Scaling Agentic Reinforcement Learning with Unified Resource System](https://arxiv.org/abs/2507.14897) | arXiv 2025 | — |
| [RepoForge: Training a SOTA Fast-thinking SWE Agent with an End-to-End Data Curation Pipeline Synergizing SFT and RL at Scale](https://arxiv.org/abs/2508.01550) | arXiv 2025 | — |
| [RLFactory: A Plug-and-Play Reinforcement Learning Post-Training Framework for LLM Multi-Turn Tool-Use](https://arxiv.org/abs/2509.06980) | arXiv 2025 | — |
| [Scaling Agentic Reinforcement Learning for Tool-Integrated Reasoning in VLMs](https://arxiv.org/abs/2511.19773) | arXiv 2025 | — |
| [WebSailor-V2: Bridging the Chasm to Proprietary Agents via Synthetic Data and Scalable Reinforcement Learning](https://arxiv.org/abs/2509.13305) | arXiv 2025 | — |
| [Youtu-Agent: Scaling Agent Productivity with Automated Generation and Hybrid Policy Optimization](https://arxiv.org/abs/2512.24615) | arXiv 2025 | — |

<a id="trajectory-lifecycle-management"></a>

### Trajectory Lifecycle Management

Represent, admit, store, deliver, replay, and retire collected trajectories.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Agent Lightning v1.0: Towards Harnessed Agentic RL](https://arxiv.org/abs/2608.17528) | arXiv 2026 | [![GitHub](https://img.shields.io/github/stars/microsoft/agent-lightning?style=flat&label=GitHub)](https://github.com/microsoft/agent-lightning) |
| [AgentJet: A Distributed Swarm Training Framework for Agentic Reinforcement Learning](https://arxiv.org/abs/2606.04484) | arXiv 2026 | — |
| [AgentWorld: A Data Factory for Training LLM Agents from Multi-Turn Interactions](https://arxiv.org/abs/2606.09138) | arXiv 2026 | — |
| [Complementary RL: Towards Efficient Experience-Driven Agent Learning](https://arxiv.org/abs/2603.17621) | arXiv 2026 | — |
| [Contextual Rollout Bandits for Reinforcement Learning with Verifiable Rewards](https://arxiv.org/abs/2602.08499) | arXiv 2026 | — |
| [Efficient RL Training for LLMs with Experience Replay](https://arxiv.org/abs/2604.08706) | arXiv 2026 | — |
| [GEOALIGN: Geometric Rollout Curation for Robust LLM Reinforcement Learning](https://arxiv.org/abs/2606.26917) | arXiv 2026 | — |
| [Headroom-Drift Replay: A Primitive for Principled Replay Control in GRPO](https://arxiv.org/abs/2609.03941) | arXiv 2026 | — |
| [KV-streams for Efficient Compaction in Agentic Reinforcement Learning](https://arxiv.org/abs/2609.35750) | arXiv 2026 | — |
| [Learning from the Right Rollouts: Data Attribution for PPO-based LLM Post-Training](https://arxiv.org/abs/2604.01597) | arXiv 2026 | — |
| [Polar: Agentic RL on Any Harness at Scale](https://arxiv.org/abs/2605.24220) | arXiv 2026 | — |
| [Rollout-Level Advantage-Prioritized Experience Replay for GRPO](https://arxiv.org/abs/2606.04560) | arXiv 2026 | — |
| [StaleFlow: Staleness-Aware Data Management for Mitigating Data Skewness in Fully Disaggregated RL Post-Training](https://arxiv.org/abs/2601.12784) | arXiv 2026 | — |
| [Where Does Staleness Accumulate? Pool Aware Effective Staleness Control for Asynchronous RL in LLM Post-Training](https://arxiv.org/abs/2609.36830) | arXiv 2026 | — |
| [A Snapshot of Influence: A Local Data Attribution Framework for Online Reinforcement Learning](https://arxiv.org/abs/2505.19281) | NeurIPS 2025 | — |
| [Agent Lightning: Train ANY AI Agents with Reinforcement Learning](https://arxiv.org/abs/2508.03680) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/microsoft/agent-lightning?style=flat&label=GitHub)](https://github.com/microsoft/agent-lightning) |
| [Agent-R1: A Unified and Modular Framework for Agentic Reinforcement Learning](https://arxiv.org/abs/2511.14460) | arXiv 2025 | — |
| [AsyncFlow: An Asynchronous Streaming RL Framework for Efficient LLM Post-Training](https://arxiv.org/abs/2507.01663) | arXiv 2025 | — |
| [Improving Data Efficiency for LLM Reinforcement Fine-tuning Through Difficulty-targeted Online Data Selection and Rollout Replay](https://arxiv.org/abs/2506.05316) | NeurIPS 2025 | — |
| [Improving Sampling Efficiency in RLVR through Adaptive Rollout and Response Reuse](https://arxiv.org/abs/2509.25808) | arXiv 2025 | — |
| [Not All Rollouts are Useful: Down-Sampling Rollouts in LLM Reinforcement Learning](https://arxiv.org/abs/2504.13818) | arXiv 2025 | — |
| [Sharing is Caring: Efficient LM Post-Training with Collective RL Experience Sharing](https://arxiv.org/abs/2509.08721) | arXiv 2025 | — |
| [Tool-R1: Sample-Efficient Reinforcement Learning for Agentic Tool Use](https://arxiv.org/abs/2509.12867) | arXiv 2025 | — |
| [ToolBrain: A Flexible Reinforcement Learning Framework for Agentic Tools](https://arxiv.org/abs/2510.00023) | arXiv 2025 | — |
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
| [ARES: Adaptive Red-Teaming and End-to-End Repair of Policy-Reward System](https://arxiv.org/abs/2604.18789) | arXiv 2026 | — |
| [How Far Can Unsupervised RLVR Scale LLM Training?](https://arxiv.org/abs/2603.08660) | arXiv 2026 | — |
| [WebGym: Scaling Training Environments for Visual Web Agents with Realistic Tasks](https://arxiv.org/abs/2601.02439) | arXiv 2026 | — |
| [When RLHF Fails: A Mechanistic Taxonomy of Reward Hacking, Collapse, and Evaluator Gaming](https://arxiv.org/abs/2606.03238) | arXiv 2026 | — |
| [Reward Model Overoptimisation in Iterated RLHF](https://arxiv.org/abs/2505.18126) | arXiv 2025 | — |
| [(N,K)-Puzzle: A Cost-Efficient Testbed for Benchmarking Reinforcement Learning Algorithms in Generative Language Model](https://arxiv.org/abs/2403.07191) | arXiv 2024 | — |
| [Improving Reinforcement Learning from Human Feedback with Efficient Reward Model Ensemble](https://arxiv.org/abs/2401.16635) | arXiv 2024 | — |
| [ODIN: Disentangled Reward Mitigates Hacking in RLHF](https://arxiv.org/abs/2402.07319) | arXiv 2024 | — |
| [Post-hoc Reward Calibration: A Case Study on Length Bias](https://arxiv.org/abs/2409.17407) | arXiv 2024 | — |
| [WARM: On the Benefits of Weight Averaged Reward Models](https://arxiv.org/abs/2401.12187) | arXiv 2024 | — |
| [Reward Model Ensembles Help Mitigate Overoptimization](https://arxiv.org/abs/2310.02743) | arXiv 2023 | — |
| [Training a Helpful and Harmless Assistant with Reinforcement Learning from Human Feedback](https://arxiv.org/abs/2204.05862) | arXiv 2022 | — |

<a id="programmatic-verifiers"></a>

### Programmatic Verifiers

Maintain verifier execution, specification adequacy, and integrity.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Automating Formal Verification with Reinforcement Learning and Recursive Inference](https://arxiv.org/abs/2605.30914) | arXiv 2026 | — |
| [CATCH: A Controllable Analysis Testbed for Reward Hacking in Coding RL](https://arxiv.org/abs/2609.39533) | arXiv 2026 | — |
| [Countdown-Code: A Testbed for Studying The Emergence and Generalization of Reward Hacking in RLVR](https://arxiv.org/abs/2603.07084) | arXiv 2026 | — |
| [Evaluating Rollout-Verified Reinforcement Fine-Tuning of a Reasoning Model for Multi-Zone Variable-Air-Volume Control](https://arxiv.org/abs/2607.27914) | arXiv 2026 | — |
| [LLMs Gaming Verifiers: RLVR can Lead to Reward Hacking](https://arxiv.org/abs/2604.15149) | arXiv 2026 | — |
| [Reward Hacking in Language Model Agents: Revisiting AI Safety Gridworlds](https://arxiv.org/abs/2606.15385) | arXiv 2026 | — |

<a id="reward-signals"></a>

### Reward Signals

Compose, attribute, and correct the feedback supplied to learning.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [AgentCPM-Explore: Realizing Long-Horizon Deep Exploration for Edge-Scale Agents](https://arxiv.org/abs/2602.06485) | arXiv 2026 | — |
| [CacheRL:Multi-Turn Tool-Calling Agents via Cached Rollouts and Hybrid Reward](https://arxiv.org/abs/2606.14179) | arXiv 2026 | — |
| [Multimodal Reward Hacking in Reinforcement Learning](https://arxiv.org/abs/2607.09492) | arXiv 2026 | — |
| [Peak-Then-Collapse and the Four Interface Channels of Knowledge-Graph Tool Use](https://arxiv.org/abs/2605.26037) | arXiv 2026 | — |
| [Scaling Automatic Research Agents via World Models](https://arxiv.org/abs/2608.12564) | arXiv 2026 | — |
| [FAPO: Flawed-Aware Policy Optimization for Efficient and Reliable Reasoning](https://arxiv.org/abs/2510.22543) | arXiv 2025 | — |
| [Reinforcement Learning from User Feedback](https://arxiv.org/abs/2505.14946) | arXiv 2025 | — |
| [Reinforcement Learning with Verifiable yet Noisy Rewards under Imperfect Verifiers](https://arxiv.org/abs/2510.00915) | arXiv 2025 | — |
| [Scaling Reinforcement Learning for Content Moderation with Large Language Models](https://arxiv.org/abs/2512.20061) | arXiv 2025 | — |
| [Stop Summation: Min-Form Credit Assignment Is All Process Reward Model Needs for Reasoning](https://arxiv.org/abs/2504.15275) | arXiv 2025 | — |
| [Safe RLHF: Safe Reinforcement Learning from Human Feedback](https://arxiv.org/abs/2310.12773) | arXiv 2023 | — |

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
| [AREAL-DTA: Dynamic Tree Attention for Efficient Reinforcement Learning of Large Language Models](https://arxiv.org/abs/2602.00482) | arXiv 2026 | — |
| [AuroraRL: Fast, Fault-Tolerant, and Cost-Efficient Reinforcement Learning over Decentralized Network](https://arxiv.org/abs/2602.11456) | arXiv 2026 | — |
| [Bidirectional Resource Scheduling for Disaggregated and Asynchronous RL Post-Training](https://arxiv.org/abs/2607.09207) | arXiv 2026 | — |
| [FlexMARL: Graph-Driven Rollout-Training Co-Design for LLM-Based Multi-Agent Reinforcement Learning](https://arxiv.org/abs/2602.09578) | arXiv 2026 | — |
| [Harnessing Routing Foresight for Micro-step-level MoE load balancing in RL Post-training](https://arxiv.org/abs/2606.11867) | arXiv 2026 | — |
| [JigsawRL: Assembling RL Pipelines for Efficient LLM Post-Training](https://arxiv.org/abs/2604.23838) | arXiv 2026 | — |
| [Libra: Efficient Resource Management for Agentic RL Post-Training](https://arxiv.org/abs/2606.03077) | arXiv 2026 | — |
| [MARLaaS: Multi-Tenant Asynchronous Reinforcement Learning as a Service](https://arxiv.org/abs/2605.08527) | arXiv 2026 | — |
| [MinT: Managed Infrastructure for Training and Serving Millions of LLMs](https://arxiv.org/abs/2605.13779) | arXiv 2026 | — |
| [Nereus: Adaptive Parallelism for LLM Post-Training](https://arxiv.org/abs/2609.34645) | arXiv 2026 | — |
| [PlexRL: Cluster-Level Orchestration of Serviceized LLM Execution for RLVR](https://arxiv.org/abs/2605.20863) | arXiv 2026 | — |
| [PrefixFlow: Training-Time KV Caching for Schedule-Level Prefix Reuse in LLM RL Training](https://arxiv.org/abs/2606.01143) | arXiv 2026 | — |
| [QwenGyre: An Elastic Reinforcement Learning Framework for Training xLong-Horizon Agents](https://arxiv.org/abs/2609.33848) | arXiv 2026 | — |
| [Relax: An Asynchronous Reinforcement Learning Engine for Omni-Modal Post-Training at Scale](https://arxiv.org/abs/2604.11554) | arXiv 2026 | — |
| [ReLibra: Routing-Replay-Guided Load Balancing for MoE Training in Reinforcement Learning](https://arxiv.org/abs/2605.08639) | arXiv 2026 | — |
| [RolloutPipe: Overlapping Pipelined Rollout and Training in Disaggregated On-Policy LLM Reinforcement Learning](https://arxiv.org/abs/2606.26997) | arXiv 2026 | — |
| [Splitting Prompt Prefill from Response Replay for Context-Parallel Long-Context LLM Post-Training](https://arxiv.org/abs/2609.33133) | arXiv 2026 | — |
| [TensorHub: Scalable and Elastic Weight Transfer for LLM RL Training](https://arxiv.org/abs/2604.09107) | arXiv 2026 | — |
| [TENT: A Declarative Slice Spraying Engine for Performant and Resilient Data Movement in Disaggregated LLM Serving](https://arxiv.org/abs/2604.00368) | arXiv 2026 | — |
| [TideRL: Boosting Agentic RL Goodput with Readiness-Aware Scheduling](https://arxiv.org/abs/2608.10402) | arXiv 2026 | — |
| [Understanding and Exploiting Weight Update Sparsity for Communication-Efficient Distributed RL](https://arxiv.org/abs/2602.03839) | arXiv 2026 | — |
| [WeightBridge: An Efficient Weight Transfer Library for Reinforcement Learning](https://arxiv.org/abs/2609.25442) | arXiv 2026 | — |
| [AReaL-Hex: Accommodating Asynchronous RL Training over Heterogeneous GPUs](https://arxiv.org/abs/2511.00796) | arXiv 2025 | — |
| [DiRL: An Efficient Post-Training Framework for Diffusion Language Models](https://arxiv.org/abs/2512.22234) | arXiv 2025 | — |
| [DistFlow: A Fully Distributed RL Framework for Scalable and Efficient LLM Post-Training](https://arxiv.org/abs/2507.13833) | arXiv 2025 | — |
| [HetRL: Efficient Reinforcement Learning for LLMs in Heterogeneous Environments](https://arxiv.org/abs/2512.12476) | arXiv 2025 | — |
| [HybridFlow: A Flexible and Efficient RLHF Framework](https://arxiv.org/abs/2409.19256) | EuroSys 2025 | [![GitHub](https://img.shields.io/github/stars/verl-project/verl?style=flat&label=GitHub)](https://github.com/verl-project/verl) |
| [LlamaRL: A Distributed Asynchronous Reinforcement Learning Framework for Efficient Large-scale LLM Training](https://arxiv.org/abs/2505.24034) | arXiv 2025 | — |
| [MarsRL: Advancing Multi-Agent Reasoning System via Reinforcement Learning with Agentic Pipeline Parallelism](https://arxiv.org/abs/2511.11373) | arXiv 2025 | — |
| [MindSpeed RL: Distributed Dataflow for Scalable and Efficient RL Training on Ascend NPU Cluster](https://arxiv.org/abs/2507.19017) | arXiv 2025 | — |
| [Pangu Embedded: An Efficient Dual-system LLM Reasoner with Metacognition](https://arxiv.org/abs/2505.22375) | arXiv 2025 | — |
| [RLinf: Flexible and Efficient Large-scale Reinforcement Learning via Macro-to-Micro Flow Transformation](https://arxiv.org/abs/2509.15965) | arXiv 2025 | [![GitHub](https://img.shields.io/github/stars/RLinf/RLinf?style=flat&label=GitHub)](https://github.com/RLinf/RLinf) |
| [RLLaVA: An RL-central Framework for Language and Vision Assistants](https://arxiv.org/abs/2512.21450) | arXiv 2025 | — |
| [RollArt: Disaggregated Multi-Task Agentic RL Training at Scale](https://arxiv.org/abs/2512.22560) | arXiv 2025 | — |
| [Tree Training: Accelerating Agentic LLMs Training via Shared Prefix Reuse](https://arxiv.org/abs/2511.00413) | arXiv 2025 | — |
| [NeMo-Aligner: Scalable Toolkit for Efficient Model Alignment](https://arxiv.org/abs/2405.01481) | arXiv 2024 | — |
| [Optimizing RLHF Training for Large Language Models with Stage Fusion](https://arxiv.org/abs/2409.13221) | arXiv 2024 | — |
| [Parameter Efficient Reinforcement Learning from Human Feedback](https://arxiv.org/abs/2403.10704) | arXiv 2024 | — |
| [ReaL: Efficient RLHF Training of Large Language Models with Parameter Reallocation](https://arxiv.org/abs/2406.14088) | arXiv 2024 | — |
| [An Adaptive Placement and Parallelism Framework for Accelerating RLHF Training](https://arxiv.org/abs/2312.11819) | arXiv 2023 | — |
| [DeepSpeed-Chat: Easy, Fast and Affordable RLHF Training of ChatGPT-like Models at All Scales](https://arxiv.org/abs/2308.01320) | arXiv 2023 | [![GitHub](https://img.shields.io/github/stars/deepspeedai/DeepSpeedExamples?style=flat&label=GitHub)](https://github.com/deepspeedai/DeepSpeedExamples) |
| [Efficient RLHF: Reducing the Memory Usage of PPO](https://arxiv.org/abs/2309.00754) | arXiv 2023 | — |
| [trlX: A Framework for Large Scale Reinforcement Learning from Human Feedback](https://aclanthology.org/2023.emnlp-main.530/) | EMNLP 2023 | [![GitHub](https://img.shields.io/github/stars/CarperAI/trlx?style=flat&label=GitHub)](https://github.com/CarperAI/trlx) |

<a id="policy-consistency"></a>

### Policy Consistency

Control staleness, numerical discrepancies, and divergent execution paths.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Cool the Sampler, Not the Learner: Sampling Temperature Moves the Staleness Cliff of Importance-Corrected GRPO](https://arxiv.org/abs/2609.36953) | arXiv 2026 | — |
| [Diagnosing Training Inference Mismatch in LLM Reinforcement Learning via a Zero-Mismatch Reference](https://arxiv.org/abs/2605.14220) | arXiv 2026 | — |
| [FP8-RL: A Practical and Stable Low-Precision Stack for LLM Reinforcement Learning](https://arxiv.org/abs/2601.18150) | arXiv 2026 | — |
| [How Off-Policy Can GRPO Be? Mu-GRPO for Efficient LLM Reinforcement Learning](https://arxiv.org/abs/2605.17570) | arXiv 2026 | — |
| [Jackpot: Optimal Budgeted Rejection Sampling for Extreme Actor-Policy Mismatch Reinforcement Learning](https://arxiv.org/abs/2602.06107) | arXiv 2026 | — |
| [Jet-RL: Enabling On-Policy FP8 Reinforcement Learning with Unified Training and Rollout Precision Flow](https://arxiv.org/abs/2601.14243) | arXiv 2026 | — |
| [LEGO-RL: Harness-Native Reinforcement Learning for Coding Agents](https://arxiv.org/abs/2608.17393) | arXiv 2026 | — |
| [Missing Old Logits in Asynchronous Agentic RL: Semantic Mismatch and Repair Methods for Off-Policy Correction](https://arxiv.org/abs/2605.12070) | arXiv 2026 | — |
| [QaRL: Rollout-Aligned Quantization-Aware RL for Fast and Stable Training under Training--Inference Mismatch](https://arxiv.org/abs/2604.07853) | arXiv 2026 | — |
| [QUADS: Stabilizing NVFP4 Reinforcement Learning for MoE via QUantization-error Alignment across Dual Sides](https://arxiv.org/abs/2607.15810) | arXiv 2026 | — |
| [QuRL: Efficient Reinforcement Learning with Quantized Rollout](https://arxiv.org/abs/2602.13953) | arXiv 2026 | — |
| [Scaling Laws for Collapse in Asynchronous GRPO](https://arxiv.org/abs/2607.01083) | arXiv 2026 | — |
| [Sparrow: Sparse Rollout for Stable and Efficient Long-context RL of Large Language Models](https://arxiv.org/abs/2606.08446) | arXiv 2026 | — |
| [Sparse-RL: Breaking the Memory Wall in LLM Reinforcement Learning via Stable Sparse Rollouts](https://arxiv.org/abs/2601.10079) | arXiv 2026 | — |
| [Defeating the Training-Inference Mismatch via FP16](https://arxiv.org/abs/2510.26788) | arXiv 2025 | — |
| [Deterministic Inference across Tensor Parallel Sizes That Eliminates Training-Inference Mismatch](https://arxiv.org/abs/2511.17826) | arXiv 2025 | — |
| [Each Prompt Matters: Scaling Reinforcement Learning Without Wasting Rollouts on Hundred-Billion-Scale MoE](https://arxiv.org/abs/2512.07710) | arXiv 2025 | — |
| [Echo: Decoupling Inference and Training for Large-Scale RL Alignment on Heterogeneous Swarms](https://arxiv.org/abs/2508.05387) | arXiv 2025 | — |
| [MiniMax-M1: Scaling Test-Time Compute Efficiently with Lightning Attention](https://arxiv.org/abs/2506.13585) | arXiv 2025 | — |
| [Periodic Asynchrony: An On-Policy Approach for Accelerating LLM Reinforcement Learning](https://arxiv.org/abs/2511.18871) | arXiv 2025 | — |
| [Stabilizing MoE Reinforcement Learning by Aligning Training and Inference Routers](https://arxiv.org/abs/2510.11370) | arXiv 2025 | — |
| [Trajectory Balance with Asynchrony: Decoupling Exploration and Learning for Fast, Scalable LLM Post-Training](https://arxiv.org/abs/2503.18929) | arXiv 2025 | — |
| [Asynchronous RLHF: Faster and More Efficient Off-Policy RL for Language Models](https://arxiv.org/abs/2410.18252) | arXiv 2024 | — |

<a id="learning-stability"></a>

### Learning Stability

Regulate updates and preserve exploration and useful learning signals.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Abstention as an Action Can Kill Both the Reward Gradient and the KL Anchor: Collapse Law and Repair for Error-Penalized Reinforcement Learning](https://arxiv.org/abs/2608.00301) | arXiv 2026 | — |
| [Advantage Collapse in Group Relative Policy Optimization: Diagnosis and Mitigation](https://arxiv.org/abs/2605.21125) | arXiv 2026 | — |
| [DAPO: An Open-Source LLM Reinforcement Learning System at Scale](https://arxiv.org/abs/2503.14476) | NeurIPS 2026 | — |
| [Dr. MAS: Stable Reinforcement Learning for Multi-Agent LLM Systems](https://arxiv.org/abs/2602.08847) | arXiv 2026 | — |
| [Explore More, Drift Less: Outcome-Only Reinforcement Learning Can Suffice for Long-Horizon Interactive Agents](https://arxiv.org/abs/2609.01245) | arXiv 2026 | — |
| [GRPO Training Dynamics for Small Language Models](https://arxiv.org/abs/2609.39321) | arXiv 2026 | — |
| [MoE Proxy Models for Low-Cost Failure Reproduction and Diagnosis in LLM RL Post-Training](https://arxiv.org/abs/2608.10823) | arXiv 2026 | — |
| [Performance, Efficiency and Collapse -- Advantages and Challenges in Offline Post-training of Code LLMs](https://arxiv.org/abs/2609.11956) | arXiv 2026 | — |
| [Probing RLVR training instability through the lens of objective-level hacking](https://arxiv.org/abs/2602.01103) | arXiv 2026 | — |
| [RAGEN-2: Reasoning Collapse in Agentic RL](https://arxiv.org/abs/2604.06268) | arXiv 2026 | — |
| [Self-Improvement Can Self-Regress: The Rise-and-Collapse Failure Mode of LLM Self-Training](https://arxiv.org/abs/2606.21090) | arXiv 2026 | — |
| [The Dark Room in the Reward Channel: Dense Prediction Rewards Collapse GRPO-Trained LLM Agents -- and The Channel, Not the Content, Decides What Works](https://arxiv.org/abs/2607.21273) | arXiv 2026 | — |
| [Towards Robust LLM Post-Training: Automatic Failure Management for Reinforcement Fine-Tuning](https://arxiv.org/abs/2605.04431) | arXiv 2026 | — |
| [Understanding Diversity Collapse in RLVR via the Lens of Overtraining](https://arxiv.org/abs/2606.15455) | arXiv 2026 | — |
| [When Does Multi-Agent RL Improve LLM Workflows? Workflow, Scale, and Policy-Sharing Tradeoffs](https://arxiv.org/abs/2605.24202) | arXiv 2026 | — |
| [Failure Modes of Maximum Entropy RLHF](https://arxiv.org/abs/2509.20265) | arXiv 2025 | — |
| [GLM-4.5V and GLM-4.1V-Thinking: Towards Versatile Multimodal Reasoning with Scalable Reinforcement Learning](https://arxiv.org/abs/2507.01006) | arXiv 2025 | — |
| [RAGEN: Understanding Self-Evolution in LLM Agents via Multi-Turn Reinforcement Learning](https://arxiv.org/abs/2504.20073) | arXiv 2025 | — |
| [Scaling Up RL: Unlocking Diverse Reasoning in LLMs via Prolonged Training](https://arxiv.org/abs/2507.12507) | arXiv 2025 | — |
| [ChatGLM-RLHF: Practices of Aligning Large Language Models with Human Feedback](https://arxiv.org/abs/2404.00934) | arXiv 2024 | — |

<a id="training-recovery"></a>

### Training Recovery

Preserve checkpoints and isolate or recover from runtime failures.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Laminar: A Scalable Asynchronous RL Post-Training Framework](https://arxiv.org/abs/2510.12633) | EuroSys 2026 | — |
| [Role-Based Fault Tolerance System for LLM RL Post-Training](https://arxiv.org/abs/2512.22492) | arXiv 2025 | — |
| [WeChat-YATT: A Scalable, Simple, Efficient, and Production Ready Training Library](https://arxiv.org/abs/2508.07970) | arXiv 2025 | — |

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
| [Agent^2 RL-Bench: Can LLM Agents Engineer Agentic RL Post-Training?](https://arxiv.org/abs/2604.10547) | arXiv 2026 | — |
| [DataFlex-RL: An Evaluation Platform for RLVR Data Policies](https://arxiv.org/abs/2609.06107) | arXiv 2026 | — |
| [From Reward Signal to Visual Utility: A Controlled Audit of Medical VLM Post-Training](https://arxiv.org/abs/2609.31450) | arXiv 2026 | — |
| [Measuring Reward Hacking and Reasoning-Answer Decoupling Under Position-Confounded Optimization](https://arxiv.org/abs/2608.15445) | arXiv 2026 | — |
| [Reach or Solve? Deep Diving into Agentic RL Gains with Checkpoint Handoffs](https://arxiv.org/abs/2609.19636) | arXiv 2026 | — |
| [A Sober Look at Progress in Language Model Reasoning: Pitfalls and Paths to Reproducibility](https://arxiv.org/abs/2504.07086) | arXiv 2025 | — |
| [Local Coherence or Global Validity? Investigating RLVR Traces in Math Domains](https://arxiv.org/abs/2510.18176) | arXiv 2025 | — |
| [Rethinking RL Scaling for Vision Language Models: A Transparent, From-Scratch Framework and Comprehensive Evaluation Scheme](https://arxiv.org/abs/2504.02587) | arXiv 2025 | — |

<a id="risk-auditing"></a>

### Risk Auditing

Audit regressions, unsafe behavior, privacy exposure, and reasoning monitorability.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [Detecting RLVR Training Data via Structural Convergence of Reasoning](https://arxiv.org/abs/2602.11792) | arXiv 2026 | — |
| [GRPO Beyond English: A Large-Scale Study of GRPO in Non-English and Multilingual Settings](https://arxiv.org/abs/2608.13698) | arXiv 2026 | — |
| [How LLM Task-Adaptation Reshapes Alignment: A Multi-dimensional Study of Behavioral and Representational Drift](https://arxiv.org/abs/2607.22676) | arXiv 2026 | — |
| [Length Penalties Make Chain-of-Thought Less Monitorable](https://arxiv.org/abs/2607.09786) | arXiv 2026 | — |
| [Monitorability as a Free Gift: How RLVR Spontaneously Aligns Reasoning](https://arxiv.org/abs/2602.03978) | arXiv 2026 | — |
| [No Free Efficiency: Revisiting the Trade-off Between Training Efficiency and Model Vulnerability](https://arxiv.org/abs/2609.33898) | arXiv 2026 | — |
| [Where does output diversity collapse in post-training?](https://arxiv.org/abs/2604.16027) | arXiv 2026 | — |
| [Auditing Data Membership in Reinforcement Learning With Verifiable Rewards](https://arxiv.org/abs/2511.14045) | arXiv 2025 | — |
| [Auditing language models for hidden objectives](https://arxiv.org/abs/2503.10965) | arXiv 2025 | — |
| [Cross-lingual Collapse: How Language-Centric Foundation Models Shape Reasoning in Large Language Models](https://arxiv.org/abs/2506.05850) | arXiv 2025 | — |
| [Detecting Data Contamination from Reinforcement Learning Post-training for Large Language Models](https://arxiv.org/abs/2510.09259) | arXiv 2025 | — |
| [Mapping Post-Training Forgetting in Language Models at Scale](https://arxiv.org/abs/2510.17776) | arXiv 2025 | — |
| [Natural Emergent Misalignment from Reward Hacking in Production RL](https://arxiv.org/abs/2511.18397) | arXiv 2025 | — |

<a id="version-acceptance"></a>

### Version Acceptance

Use evaluation evidence to retain checkpoints and accept or reject changes.

| Paper | Venue | Code |
| --- | :---: | :---: |
| [CharacterFlywheel: Scaling Iterative Improvement of Engaging and Steerable LLMs in Production](https://arxiv.org/abs/2603.01973) | arXiv 2026 | — |
| [EvalStop: Using World Feedback to Detect and Correct Reward Overoptimization in Multi-Tenant RLHF Platforms](https://arxiv.org/abs/2606.04145) | arXiv 2026 | — |
| [EvoTrainer: Co-Evolving LLM Policies and Training Harnesses for Autonomous Agentic Reinforcement Learning](https://arxiv.org/abs/2606.03108) | arXiv 2026 | — |
| [MERA: Model Evolution and Routing with Skill Adaptation for Agentic Systems at Scale](https://arxiv.org/abs/2608.10333) | arXiv 2026 | — |
| [SafeEvolve: Harness-Policy Co-Evolution from Agent Experience for Safety Alignment](https://arxiv.org/abs/2609.02786) | arXiv 2026 | — |
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

<a id="contributing"></a>

## Contributing

Paper suggestions, official code links, publication updates, and corrections are welcome through issues or pull requests.

<a id="citation"></a>

## Citation

