# Awesome Bandit–LLM Interaction

A structured and continuously maintained collection of research on the interaction between bandit learning and large language models.

[![Papers](https://img.shields.io/badge/papers-153-539AB9?style=flat-square)](#-literature-navigation)
[![Directions](https://img.shields.io/badge/directions-2-6C63A8?style=flat-square)](#-taxonomy)
[![Research Streams](https://img.shields.io/badge/research_streams-63-4C956C?style=flat-square)](#-taxonomy)
[![Coverage](https://img.shields.io/badge/coverage-through_August_15%2C_2026-D97706?style=flat-square)](#-corpus-at-a-glance)
[![License: MIT](https://img.shields.io/badge/license-MIT-2EA44F?style=flat-square)](LICENSE)

[Corpus at a Glance](#corpus-at-a-glance) · [Search & Review Methodology](#search--review-methodology) · [Taxonomy](#-taxonomy) · [Literature Navigation](#-literature-navigation) · [Bibliography](#-bibliography)

## 👋 About

This companion repository supports the *Bandit–LLM Interaction* survey. It organizes work in both directions: bandit methods that improve large language model systems, and LLM capabilities that augment bandit learning. The taxonomy is the source of truth for inclusion, and all citation metadata is drawn from the supplied BibTeX database.

## 📊 Corpus at a Glance

> **153 unique studies · 2 directions · 8 stages · 18 components · 63 research streams · 230 taxonomy assignments**

The survey corpus analyzed in the accompanying paper is frozen at **August 15, 2026** and contains **153 unique studies**. This repository may continue to incorporate newly released Bandit–LLM work after the survey cutoff.

Use the [Literature Navigation](#-literature-navigation) to browse papers by research stream, follow each paper's verified arXiv or official publication link, download [`references.bib`](references.bib) for citation management, or inspect [`taxonomy.yaml`](taxonomy.yaml) for the complete machine-readable classification.

## 🔍 Search & Review Methodology

### 🧩 PCC Search Framework

To provide broad and structured coverage of the rapidly evolving literature on Bandit–LLM interaction, we organized the literature search using the Population–Concept–Context (PCC) framework.

Rather than restricting retrieval to the components of our final taxonomy, PCC was used to define a broad search space around modern LLMs, genuine bandit methods, and their substantive technical interaction.

| PCC Element | Scope in This Review |
|---|---|
| Population | Modern large language models (LLMs) and LLM-based systems |
| Concept | Multi-armed bandits and related genuine bandit formulations, algorithms, and sequential decision mechanisms |
| Context | Substantive technical interaction between LLMs and bandits, either through bandit-based control of the LLM lifecycle or LLM-based augmentation of the bandit decision pipeline |

The Population and Concept dimensions were used to construct broad retrieval queries. The Context criterion was primarily applied during title/abstract screening and full-text assessment. This separation was intended to preserve recall during literature identification without prematurely restricting retrieval to the component taxonomy developed later in the review.

### 🔎 Search Strategy

The survey corpus search window was **January 1, 2022–August 15, 2026**. The cutoff defines the paper's corpus snapshot; later repository additions belong to **Post-Survey Updates**.

Primary literature sources were **Scopus**, **Web of Science Core Collection**, **ACM Digital Library**, **IEEE Xplore**, and **arXiv**. Supplementary discovery and verification used **Google Scholar**, **Semantic Scholar**, backward citation tracing, and forward citation tracing. Together these sources cover machine learning, natural language processing, information retrieval, recommender systems, data mining, operations research, and online learning.

The canonical Population terms were:

```text
"large language model" OR "large language models" OR LLM OR LLMs
OR "language model" OR "language models"
```

The canonical Concept terms were:

```text
bandit OR "multi-armed bandit" OR "multi armed bandit"
OR "contextual bandit" OR "combinatorial bandit" OR "linear bandit"
OR "bandit learning" OR "bandit algorithm" OR "Thompson sampling"
OR "upper confidence bound"
```

Canonical search logic:

```text
(Population terms) AND (Concept terms)
```

Database-specific syntax was adapted where required by individual search interfaces. These concepts document a canonical reproducible strategy, not character-for-character historical queries. Taxonomy-specific terms—such as prompting, retrieval, routing, caching, agent orchestration, reward estimation, exploration, and feedback interpretation—were not mandatory conditions in the initial broad query; they were applied during screening and synthesis.

### ✅ Eligibility Criteria

**Core principle:** A study was retained only when Bandit–LLM interaction formed a substantive part of its problem formulation, methodology, learning procedure, decision mechanism, or system design.

| Included | Excluded |
|---|---|
| Modern LLMs or LLM-based systems form part of the method or studied environment. | LLMs or bandits appear only in background, introduction, related work, baselines, or incidental implementation components. |
| A genuine bandit formulation, algorithm, exploration mechanism, or partial-feedback decision process is present. | “Bandit” is used metaphorically. |
| Bandits substantively control or adapt an LLM component, or LLMs substantively augment a bandit component. | Generic reinforcement learning is used without a genuine bandit formulation or algorithm. |
| Theoretical, methodological, empirical, systems, and negative-result studies are eligible. | Older or generic language-model work is included only because it is conceptually related. |
| Simulated users, proxy tasks, synthetic data, and synthetic environments are eligible when the interaction is methodologically substantive. | The report contains insufficient technical information to determine the substantive interaction. |
| Peer-reviewed, accepted, forthcoming, and high-quality preprint studies are eligible; no venue restriction is imposed. | Duplicate or superseded versions of the same substantive study are not counted independently. |

The final published version was preferred where available. A later conference or journal publication and its earlier preprint were treated as one substantive study unless they clearly constituted distinct technical contributions.

**Operational scope.** For **Bandit-Enhanced Large Language Models**, bandit methods adapt or control computational decisions across Pre-training → Post-training → Utilization → Evaluation. For **LLM-Enhanced Bandits**, LLMs augment Representation → Learning → Decision → Feedback. A study may belong to both directions when both interactions are methodologically substantive.

### 🔄 Review Workflow

```text
PCC Scope Definition
        ↓
Broad Literature Identification
        ↓
Backward / Forward Citation Expansion
        ↓
Deduplication and Version Consolidation
        ↓
Title / Abstract Screening
        ↓
Full-Text Eligibility Assessment
        ↓
Structured Evidence Extraction
        ↓
Component-Level Synthesis
        ↓
153 Unique Included Studies
```

Candidate studies were first screened from titles and abstracts using the PCC scope. Ambiguous studies were retained for full-text assessment rather than excluded prematurely. For eligible studies, multiple versions of the same substantive work were consolidated, with the final published version preferred where available.

Evidence extraction considered the problem formulation, Bandit–LLM intervention mechanism, bandit formulation, LLM integration, theoretical analysis, experimental setting, empirical findings, comparisons and ablations, and reported limitations. This evidence supported component-level synthesis and construction of the bidirectional taxonomy.

## 🧭 Taxonomy

The literature is organized according to where one technology intervenes in the computational process of the other. **Bandit-Enhanced Large Language Models** follow the LLM lifecycle—Pre-training, Post-training, Utilization, and Evaluation—whereas **LLM-Enhanced Bandits** follow the bandit decision pipeline—Representation, Learning, Decision, and Feedback.

The 153 unique studies correspond to 230 taxonomy assignments because multi-component and bidirectional studies may appear in multiple streams. The machine-readable source of truth is [`taxonomy.yaml`](taxonomy.yaml).

## 📚 Literature Navigation

A study may appear in multiple research streams when it contains multiple substantive intervention mechanisms. Accordingly, the corpus contains 153 unique studies but 230 taxonomy assignments.

<!-- BEGIN AUTO-GENERATED LITERATURE NAVIGATION -->
Browse by direction and expand a stage to view its components, research streams, and papers. Red buttons open verified arXiv records; blue buttons open official publication pages when no arXiv identifier is available. A paper may appear in more than one stream.

### Bandit-Enhanced Large Language Models

<details>
<summary><strong>Pre-training</strong> — 2 research streams · 2 papers</summary>

#### Pre-training

##### Adaptive data mixing

- Alon Albalak et al. *Efficient Online Data Mixing For Language Model Pre-Training*. arXiv, 2023. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2312.02406)

##### Pre-training configuration optimization

- Iñigo Urteaga et al. *Multi-armed bandits for resource efficient, online optimization of language model pre-training: the use case of dynamic masking*. Findings of ACL, 2023. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2203.13151)

</details>

<details>
<summary><strong>Post-training</strong> — 6 research streams · 29 papers</summary>

#### Fine-tuning

##### Data and curriculum scheduling

- Van Dai Do et al. *SPaCe: Unlocking Sample-Efficient Large Language Models Training With Self-Pace Curriculum Learning*. Findings of ACL, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.18653/v1/2026.findings-acl.171)
- Xiaodong Lu et al. *Contextual Rollout Bandits for Reinforcement Learning with Verifiable Rewards*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.08499)
- Darrien M. McKenzie, Nicklas Hansen, and Xiaolong Wang. *Manifold Bandits: Bayesian Curriculum Learning over the Latent Geometry of Large Language Models*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.19750)
- Haebin Shin et al. *DynamixSFT: Dynamic Mixture Optimization of Instruction Tuning Collections*. Findings of ACL, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.18653/v1/2026.findings-acl.1972)
- Zairun Yang et al. *Distribution-Value Coevolution for Adaptive RLHF Data Scheduling*. KDD, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3770855.3817990)

##### Bandit-informed policy training

- Sanxing Chen et al. *When Greedy Wins: Emergent Exploitation Bias in Meta-Bandit LLM Training*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2509.24923)
- Xiao Hu et al. *Rethinking Reinforcement fine-tuning of LLMs: A Multi-armed Bandit Learning Perspective*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2601.14599)
- Allen Nie et al. *EVOLvE: Evaluating and Optimizing LLMs For In-Context Exploration*. ICML, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2410.06238)
- Thomas Schmied et al. *LLMs are Greedy Agents: Effects of RL Fine-tuning on Decision-Making Abilities*. ICLR, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2504.16078)

##### Online adaptation and co-evolving targets

- Kaan Gönç et al. *User Feedback-based Online Learning for Intent Classification*. ICMI, 2023. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3577190.3614137)
- Zelin He et al. *ReSkill: Reconciling Skill Creation with Policy Optimization in Agentic RL*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.01619)
- Yu Xia et al. *Which LLM to Play? Convergence-Aware Online Model Selection with Time-Increasing Bandits*. The Web Conference, 2024. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3589334.3645420)

#### Alignment

##### Active preference acquisition

- Nirjhar Das et al. *Active Preference Optimization for Sample Efficient RLHF*. ECML PKDD, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1007/978-3-032-06096-9_6)
- Vikranth Dwaracherla et al. *Efficient Exploration for LLMs*. ICML, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2402.00396)
- Kaixuan Ji, Jiafan He, and Quanquan Gu. *Reinforcement Learning from Human Feedback with Active Queries*. TMLR, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2402.09401)
- Zichen Liu et al. *Sample-Efficient Alignment for LLMs*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2411.01493)
- Viraj Mehta et al. *Sample Efficient Preference Alignment in LLMs via Active Exploration*. arXiv, 2023. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2312.00267)
- Antoine Scheid et al. *Optimal Design for Reward Modeling in RLHF*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2410.17055)

##### Exploration-aware preference optimization

- Chenjia Bai et al. *Online Preference Alignment for Language Models via Count-based Exploration*. ICLR, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2501.12735)
- Long-Fei Li et al. *Provably Efficient Online RLHF with One-Pass Reward Modeling*. NeurIPS, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.52202/085713-5567)
- Gen Li and Yuling Yan. *Towards Efficient Online Exploration for Reinforcement Learning with Human Feedback*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2509.22633)
- Tengyang Xie et al. *Exploratory Preference Optimization: Harnessing Implicit Q\*-Approximation for Sample-Efficient RLHF*. ICLR, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2405.21046)
- Wei Xiong et al. *Iterative Preference Learning from Human Feedback: Bridging Theory and Practice for RLHF under KL-constraint*. ICML, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2312.11456)
- Shenao Zhang et al. *Self-Exploring Language Models: Active Preference Elicitation for Online Alignment*. TMLR, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2405.19332)

##### Preference and supervision control

- Mohammad Gheshlaghi Azar et al. *A General Theoretical Paradigm to Understand Learning from Human Preferences*. AISTATS, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2310.12036)
- Shaohua Duan et al. *Chunks as Arms: Multi-Armed Bandit-Guided Sampling for Long-Context LLM Preference Optimization*. ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2508.13993)
- Taesan Kim et al. *Don't Let Bandit Feedback Pull Continual LLM-Recommender Updates Off Target*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.18899)
- Allison Lau et al. *Personalized Adaptation via In-Context Preference Learning*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2410.14001)
- Duy Nguyen et al. *LASeR: Learning to Adaptively Select Reward Models with Multi-Arm Bandits*. NeurIPS, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2410.01735)

</details>

<details>
<summary><strong>Utilization</strong> — 24 research streams · 97 papers</summary>

#### Prompting

##### Prompt and demonstration selection

- Donghao Li et al. *Efficient Multi-objective Prompt Optimization via Pure-exploration Bandits*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.14553)
- Xiaoqiang Lin et al. *Use Your INSTINCT: INSTruction optimization for LLMs usIng Neural bandits Coupled with Transformers*. ICML, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2310.02905)
- Xiaoqiang Lin et al. *Prompt Optimization with Human Feedback*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2405.17346)
- Pingchen Lu et al. *FedPOB: Sample-Efficient Federated Prompt Optimization via Bandits*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2509.24701)
- Chengshuai Shi et al. *Efficient Prompt Optimization Through the Lens of Best Arm Identification*. NeurIPS, 2024. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.52202/079017-3161)
- Shuyang Wang, Somayeh Moazeni, and Diego Klabjan. *SOPL: A Sequential Optimal Learning Approach to Automated Prompt Engineering in Large Language Models*. Findings of ACL, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2501.03508)
- Zhaoxuan Wu et al. *Prompt Optimization with EASE? Efficient Ordering-aware Automated Selection of Exemplars*. NeurIPS, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2405.16122)
- Yuanchen Wu et al. *LLM Prompt Duel Optimizer: Efficient Label-Free Prompt Optimization*. Findings of ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2510.13907)

##### Prompt generation and refinement

- Rin Ashizawa et al. *Bandit-Based Prompt Design Strategy Selection Improves Prompt Optimizers*. Findings of ACL, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.18653/v1/2025.findings-acl.1070)
- Zhi Hong et al. *MASPOB: Bandit-Based Prompt Optimization for Multi-Agent Systems with Graph Neural Networks*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2603.02630)
- Mingze Kong et al. *Meta-Prompt Optimization for LLM-Based Sequential Decision Making*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.00728)
- Young-Joon Park et al. *TwinBandit Prompt Optimizer: Adaptive Prompt Optimization via Synergistic Dual MAB-Guided Feedback*. CIKM, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3746252.3760824)

##### Contextual and personalized prompting

- Zekai Chen, Po-Yu Chen, and Francois Buet-Golfouse. *Online Personalizing White-box LLMs Generation with Neural Bandits*. ICAIF, 2024. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3677052.3698651)
- Nicole Cho et al. *No One Size Fits All: QueryBandits for Hallucination Mitigation*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.20332)
- Shion Ishikawa et al. *Progressive Content Refinement with Decaying Reward Joint LinUCB*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2608.06750)
- Xiang Li et al. *ALSO: Adversarial Online Strategy Optimization for Social Agents*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.15768)
- Giovanni Monea et al. *LLMs Are In-Context Bandit Reinforcement Learners*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2410.05362)
- Allen Nie et al. *EVOLvE: Evaluating and Optimizing LLMs For In-Context Exploration*. ICML, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2410.06238)
- Aditya Ramesh et al. *Efficient Jailbreak Attack sequences on Large Language Models via Multi-Armed Bandit-based Context switching*. ICLR, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://www.semanticscholar.org/paper/ead828879a0379b248f224321bf4076e7c4b0434)

##### Offline and counterfactual prompt learning

- Haruka Kiyohara et al. *Prompt Optimization with Logged Bandit Data*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2504.02646)
- Haruka Kiyohara et al. *An Off-Policy Learning Approach for Steering Sentence Generation towards Personalization*. RecSys, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3705328.3748088)

##### Joint prompt and system control

- Jia Fu et al. *AutoRAG-HP: Automatic Online Hyper-Parameter Tuning for Retrieval-Augmented Generation*. Findings of ACL, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2406.19251)
- Yixuan Li et al. *Online Prompt Selection for Program Synthesis*. AAAI, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2501.05247)
- Saaduddin Mahmud et al. *Inference-Aware Prompt Optimization for Aligning Black-Box Large Language Models*. AAAI, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2508.10030)
- Halley Young and Nikolaj Björner. *Theory Under Construction: Orchestrating Language Models for Research Software Where the Specification Evolves*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.27209)

#### Retrieval

##### Retrieval configuration selection

- Yuhang Dai, Jing Li, and Bohan Li. *Relative Performance Bandits: An Adaptive RAG Framework with Reward-Aware Exploration*. 31th IEEE International Conference on Parallel and Distributed Systems, ICPADS 2025, Hefei, China, December 14-18, 2025, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1109/ICPADS67057.2025.11322957)
- Jia Fu et al. *AutoRAG-HP: Automatic Online Hyper-Parameter Tuning for Retrieval-Augmented Generation*. Findings of ACL, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2406.19251)
- Xiaqiang Tang et al. *MBA-RAG: a Bandit Approach for Adaptive Retrieval-Augmented Generation through Question Complexity*. Proceedings of the 31st International Conference on Computational Linguistics, COLING 2025, Abu Dhabi, UAE, January 19-24, 2025, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2412.01572)

##### Context and evidence selection

- Linfeng Du et al. *Optimizing User Profiles via Contextual Bandits for Retrieval-Augmented LLM Personalization*. ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2601.12078)
- Roxana Petcu et al. *Query Decomposition for RAG: Balancing Exploration-Exploitation*. Proceedings of the 19th Conference of the European Chapter of the Association for Computational Linguistics, EACL 2026 - Volume 1: Long Papers, Rabat, Morocco, March 24-29, 2026, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2510.18633)
- Hanzhuo Tan et al. *Prompt-Based Code Completion via Multi-Retrieval Augmented Generation*. ACM TOSEM, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3725812)

##### Adaptive retrieval computation

- Roi Pony et al. *Col-Bandit: Zero-Shot Query-Time Pruning for Late-Interaction Retrieval*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.02827)

##### Dynamic memory retrieval

- Junke Zhang et al. *Evolving Skill-Structured Attack Memory Enhances LLM Jailbreaking*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.29237)

#### Routing

##### Contextual model routing

- Zhenghua Bao et al. *OrcaRouter: A Production-Oriented LLM Router with Hybrid Offline-Online Learning*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.30736)
- Nihir Chadderwala. *Optimizing Life Sciences Agents in Real-Time using Reinforcement Learning*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2512.03065)
- Chao-Kai Chiang, Takashi Ishida, and Masashi Sugiyama. *LLM Routing with Dueling Feedback*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2510.00841)
- Kexin Chu, Dawei Xiang, and Wei Zhang. *Latency-Quality Routing for Functionally Equivalent Tools in LLM Agents*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.14241)
- Xiaoyan Hu, Ho-fung Leung, and Farzan Farnia. *PAK-UCB Contextual Bandit: An Online Learning Approach to Prompt-Aware Selection of Generative Models and LLMs*. ICML, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2410.13287)
- Quang H. Nguyen et al. *MetaLLM: A High-performant and Cost-efficient Dynamic Framework for Wrapping LLMs*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2407.10834)
- Son Nguyen, Xinyuan Liu, and Ransalu Senanayake. *CUPID in the Model Zoo: Online Matchmaking for Selecting Your Dream LLM*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.00846)
- Pranoy Panda et al. *Adaptive LLM Routing under Budget Constraints*. Findings of ACL, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2508.21141)
- Manhin Poon et al. *Online Multi-LLM Selection via Contextual Bandits Under Unstructured Context Evolution*. AAAI, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2506.17670)
- Ajay Narayanan Sridhar et al. *Correlation-Aware Contextual Bandits with Surrogate Rewards for LLM Routing*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2607.09015)
- M. Tsai and Phat Tran. *Reward-Based Online LLM Routing via NeuralUCB*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2603.30035)
- Xinyuan Wang et al. *MixLLM: Dynamic Routing in Mixed Large Language Models*. NAACL, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.18482)
- Zeyu Zhang et al. *Steering Frozen LLMs: Adaptive Social Alignment via Online Prompt Routing*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2603.15647)
- Thomas Ziller et al. *GreenServ: Energy-Efficient Context-Aware Dynamic Routing for Multi-Model LLM Inference*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2601.17551)

##### Cost- and resource-aware routing

- Seoungbin Bae, Junyoung Son, and Dabeen Lee. *Learning to Route and Schedule LLMs from User Retrials via Contextual Queueing Bandits*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.02061)
- Kexin Chu, Dawei Xiang, and Wei Zhang. *Latency-Quality Routing for Functionally Equivalent Tools in LLM Agents*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.14241)
- Xiangxiang Dai et al. *Cost-Effective Online Multi-LLM Selection with Versatile Reward Models*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2405.16587)
- Yin Huang, Qingsong Liu, and Jie Xu. *Online LLM Selection via Constrained Bandits with Time-Varying Demand*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.17489)
- Yang Li. *LLM Bandit: Cost-Efficient LLM Generation via Preference-Conditioned Dynamic Routing*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.02743)
- Quang H. Nguyen et al. *MetaLLM: A High-performant and Cost-efficient Dynamic Framework for Wrapping LLMs*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2407.10834)
- P. Patra et al. *Truthful Reverse Auctions for Adaptive Selection via Contextual Multi-Armed Bandits*. Proc. of the 25th International Conference on Autonomous Agents and Multiagent Systems, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.65109/MBRQ7564)
- Annette Taberner-Miller. *ParetoBandit: Budget-Paced Adaptive Routing for Non-Stationary LLM Serving*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.00136)
- Wang Wei et al. *Learning to Route LLMs from Bandit Feedback: One Policy, Many Trade-offs*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2510.07429)
- Shanglin Wu, Saatvik Kher, and Padhraic Smyth. *Learning to Assign Prediction Tasks to Agents with Capacity Constraints*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.27999)
- Xianzhi Zhang et al. *Adapter-Augmented Bandits for Online Multi-Constrained Multi-Modal Inference Scheduling*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2603.06403)
- Ling Zu, Xiyue Peng, and Xin Liu. *BARouter: A Budget-adaptive Online Large Language Model Router Framework*. The Web Conference, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3774904.3792725)

##### Sequential and combinatorial routing

- Baran Atalar. *Neural Bandit Based Optimal LLM Selection for Pipeline of Tasks*. ACM SIGMETRICS Performance Evaluation Review, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2508.09958)
- Alexandre Belloni, Yan Chen, and Yehua Wei. *Online Pandora's Box for Contextual LLM Cascading*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.07392)
- Yunlong Hou et al. *BanditSpec: Adaptive Speculative Decoding via Bandit Algorithms*. ICML, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2505.15141)
- Xiaoyan Hu et al. *PromptWise: Online Learning for Cost-Aware Prompt Assignment in Generative Models*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2505.18901)
- Jerry Huang et al. *Context-Aware Assistant Selection for Improved Inference Acceleration with Large Language Models*. EMNLP, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2408.08470)
- Kaiyu Huang et al. *UniScale: Adaptive Unified Inference Scaling via Online Joint Optimization of Model Routing and Test-Time Scaling*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.30898)
- Vasanth Rao Jadav, Shalini Sudarsan, and Vikram Isanaka. *Cost-Aware LLM Orchestration via Contextual Bandit Learning*. 2026 International Conference on Artificial Intelligence, Systems, and Emerging Technologies (ICAISET), 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1109/ICAISET66439.2026.11542012)
- Taehyeon Kim, Hojung Jung, and Se-Young Yun. *Multi-Drafter Speculative Decoding with Alignment Feedback*. Findings of ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.05417)
- Yixuan Li et al. *Online Prompt Selection for Program Synthesis*. AAAI, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2501.05247)
- Shaoang Li and Jian Li. *POLAR: Online Learning for LoRA Adapter Caching and Routing in Edge LLM Serving*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.16583)
- Xutong Liu et al. *Combinatorial Logistic Online Learning and Its Applications in Nonlinear Networked Systems*. IEEE Trans. Netw., 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1109/TON.2026.3663325)
- Jonathan Rau et al. *CoCoMaMa: Contextual Combinatorial Multi-Armed Bandit Router for Multi-Agent Systems with Volatile Arms*. Proceedings of the Second International Workshop on Hypermedia Multi-Agent Systems (HyperAgents 2025) co-located with 28th European Conference on Artificial Intelligence (ECAI 2025), Bologna, Italy, October 26, 2025, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://www.semanticscholar.org/paper/2a86869b09d5df9b42629881ce0861f20e4cab20)
- Junxiao Ren et al. *CH-RAG: Complexity-Guided Hybrid Retrieval-Augmented for Adaptive LLM Generation*. 2026 29th International Conference on Computer Supported Cooperative Work in Design (CSCWD), 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1109/CSCWD68734.2026.11582347)
- Xiaqiang Tang et al. *Adapting to Non-Stationary Environments: Multi-Armed Bandit Enhanced Retrieval-Augmented Generation on Knowledge Graphs*. AAAI, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2412.07618)
- Jinkun Xu et al. *CES: Combinatorial Experts Selection via Contextual Linear Bandits*. KDD, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3770855.3817902)

##### Adaptive routing under distribution shift

- Dingyang Chen, Qi Zhang, and Yinglun Zhu. *Efficient Sequential Decision Making with Large Language Models*. EMNLP, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2406.12125)
- Shaoang Li and Jian Li. *Near-Optimal Online Deployment and Routing for Streaming LLMs*. ICLR, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2506.17254)
- Jonathan Rau et al. *CoCoMaMa: Contextual Combinatorial Multi-Armed Bandit Router for Multi-Agent Systems with Volatile Arms*. Proceedings of the Second International Workshop on Hypermedia Multi-Agent Systems (HyperAgents 2025) co-located with 28th European Conference on Artificial Intelligence (ECAI 2025), Bologna, Italy, October 26, 2025, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://www.semanticscholar.org/paper/2a86869b09d5df9b42629881ce0861f20e4cab20)
- Annette Taberner-Miller. *ParetoBandit: Budget-Paced Adaptive Routing for Non-Stationary LLM Serving*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.00136)
- Xiaqiang Tang et al. *Adapting to Non-Stationary Environments: Multi-Armed Bandit Enhanced Retrieval-Augmented Generation on Knowledge Graphs*. AAAI, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2412.07618)
- Xinyuan Wang et al. *MixLLM: Dynamic Routing in Mixed Large Language Models*. NAACL, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.18482)
- Xinle Wu and Yao Lu. *Reward Model Routing in Alignment*. ICLR, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2510.02850)
- Yu Xia et al. *Which LLM to Play? Convergence-Aware Online Model Selection with Time-Increasing Bandits*. The Web Conference, 2024. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3589334.3645420)

#### Generation

##### Decoding-policy control

- Yunlong Hou et al. *BanditSpec: Adaptive Speculative Decoding via Bandit Algorithms*. ICML, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2505.15141)
- Kaiyu Huang et al. *UniScale: Adaptive Unified Inference Scaling via Online Joint Optimization of Model Routing and Test-Time Scaling*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.30898)
- Saaduddin Mahmud et al. *Inference-Aware Prompt Optimization for Aligning Black-Box Large Language Models*. AAAI, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2508.10030)
- Aditya Sridhar et al. *TapOut: A Bandit-Based Approach to Dynamic Speculative Decoding*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2511.02017)
- Chloe Su et al. *Learning Adaptive LLM Decoding*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2603.09065)

##### Candidate and response selection

- Allison Lau et al. *Personalized Adaptation via In-Context Preference Learning*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2410.14001)
- Zikun Qu et al. *T-POP: Test-Time Personalization with Online Preference Feedback*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2509.24696)
- Suho Shin et al. *Tokenized Bandit for LLM Decoding and Alignment*. ICML, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2506.07276)

##### Test-time compute allocation

- Sweta Karlekar et al. *Duel-Evolve: Reward-Free Test-Time Scaling via LLM Self-Preferences*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.21585)
- Duy Nguyen et al. *LASeR: Learning to Adaptively Select Reward Models with Multi-Arm Bandits*. NeurIPS, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2410.01735)
- Bowen Zuo and Yinglun Zhu. *Strategic Scaling of Test-Time Compute: A Bandit Learning Approach*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2506.12721)

##### Structured generation control

- Dezhi Ran et al. *KernelBand: Boosting LLM-based Kernel Optimization with a Hierarchical and Hardware-aware Multi-armed Bandit*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2511.18868)
- Haochen Song et al. *Tailored Behavior-Change Messaging for Physical Activity: Integrating Contextual Bandits and Large Language Models*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2506.07275)

#### Caching

##### Response-cache management

- Baran Atalar et al. *Continuous Semantic Caching for Low-Cost LLM Serving*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.20021)
- Hantao Yang et al. *LLM Cache Bandit Revisited: Addressing Query Heterogeneity for Cost-Effective LLM Inference*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2509.15515)

##### Semantic caching

- Xutong Liu et al. *Semantic Caching for Low-Cost LLM Serving: From Offline Learning to Online Adaptation*. IEEE INFOCOM 2026 - IEEE Conference on Computer Communications, Tokyo, Japan, May 18-21, 2026, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1109/INFOCOM59046.2026.11571467)

##### Model-state caching

- Shaoang Li and Jian Li. *POLAR: Online Learning for LoRA Adapter Caching and Routing in Edge LLM Serving*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.16583)

#### Agent Orchestration

##### Agent and tool selection

- Nihir Chadderwala. *Optimizing Life Sciences Agents in Real-Time using Reinforcement Learning*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2512.03065)
- Zhaoyang Guan et al. *Symphony-Coord: Adaptive Routing for Multi-Agent LLM Systems*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.00966)
- Dian Jin et al. *Personalizing Large Language Model Agents with Small Policy Models*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2608.00215)
- Yuqi Tang et al. *SciToolAgent-Evo: An Ontology-Aware Self-Evolving Agent for Open-World Scientific Tool Acquisition*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2607.28692)
- Sheldon Yu et al. *OLIVIA: Online Learning via Inference-time Action Adaptation for Decision Making in LLM ReAct Agents*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.11169)

##### Workflow and topology control

- Baran Atalar. *Neural Bandit Based Optimal LLM Selection for Pipeline of Tasks*. ACM SIGMETRICS Performance Evaluation Review, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2508.09958)
- Huan Chen et al. *Toward an Organizational Science of Multi-Agent LLM Systems: Decoupling Who, How, and Which Algorithm*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2607.25446)
- Xiangxiang Dai et al. *Cost-Effective Online Multi-LLM Selection with Versatile Reward Models*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2405.16587)
- Mohanna Hoveyda et al. *AQA: Adaptive Question Answering in a Society of LLMs via Contextual Multi-Armed Bandit*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2409.13447)
- Vasanth Rao Jadav, Shalini Sudarsan, and Vikram Isanaka. *Cost-Aware LLM Orchestration via Contextual Bandit Learning*. 2026 International Conference on Artificial Intelligence, Systems, and Emerging Technologies (ICAISET), 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1109/ICAISET66439.2026.11542012)
- Geremy Loachamín Suntaxi et al. *Learning to Choose: An Empowerment-Guided Multi-Agent System with semantic communication for Adaptive Method Selection*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.30042)

##### Adaptive computation allocation

- Alexandre Belloni, Yan Chen, and Yehua Wei. *Online Pandora's Box for Contextual LLM Cascading*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.07392)
- Hao Tang et al. *Code Repair with LLMs gives an Exploration-Exploitation Tradeoff*. NeurIPS, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2405.17503)
- Sixue Xing et al. *Compute Allocation in Evolutionary Search: From Depth-Breadth to Multi-Armed Bandits*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.29268)

##### Trust, verification, and integrity control

- Geremy Loachamín Suntaxi et al. *Learning to Choose: An Empowerment-Guided Multi-Agent System with semantic communication for Adaptive Method Selection*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.30042)
- Fanzeng Xia et al. *Beyond Numeric Rewards: In-Context Dueling Bandits with LLM Agents*. Findings of ACL, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.18653/v1/2025.findings-acl.519)
- Halley Young and Nikolaj Björner. *Theory Under Construction: Orchestrating Language Models for Research Software Where the Specification Evolves*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.27209)

</details>

<details>
<summary><strong>Evaluation</strong> — 4 research streams · 11 papers</summary>

#### Adaptive Evaluation

##### Best-model identification

- Zifan Lyu et al. *Cutting LLM Evaluation Costs with SySRs: A Bandit Algorithm that Provably Exploits Model Similarity*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.07726)
- Elad Tolochinsky, Yaniv Tenzer, and Yaniv Romano. *Valid Best-Model Identification for LLM Evaluation via Low-Rank Factorization*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.10405)
- Jin Peng Zhou et al. *On Speeding Up Language Model Evaluation*. ICLR, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2407.06172)

##### Ranking and Pareto identification

- Bo Xue et al. *Cost-Aware Multi-Objective Bandits: Theory and Application to Budgeted LLM Configuration Evaluation*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2608.04333)
- Vilém Zouhar et al. *Dynamically Allocating Evaluation Effort for Model Ranking*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2608.03437)

##### Preference-based evaluation

- Sarvesh Gharat, Nikhil Karamchandani, and Jayakrishnan Nair. *Cost-Aware Best Arm Identification via Dueling Feedback with Applications to Large Language Models*. Proceedings of the 25th International Conference on Autonomous Agents and Multiagent Systems, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.65109/GEKA7634)
- Aadirupa Saha, A. Wagde, and B. Kveton. *LLM-as-Judge on a Budget*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.15481)

##### Adaptive diagnostic and search evaluation

- Xiangxiang Dai et al. *A Multi-Agent Conversational Bandit Approach to Online Evaluation and Selection of User-Aligned LLM Responses*. AAAI, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1609/aaai.v40i44.41064)
- Sweta Karlekar et al. *Duel-Evolve: Reward-Free Test-Time Scaling via LLM Self-Preferences*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.21585)
- Akshay Krishnamurthy et al. *Can large language models explore in-context?* NeurIPS, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2403.15371)
- Deng Pan et al. *Context Attribution with Multi-Armed Bandit Optimization*. Findings of ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2506.19977)

</details>

### LLM-Enhanced Bandits

<details>
<summary><strong>Representation</strong> — 7 research streams · 27 papers</summary>

#### Context Representation

##### Semantic context encoding

- Ali Baheri and Cecilia O. Alm. *LLMs-augmented Contextual Bandit*. arXiv, 2023. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2311.02268)
- Vikranth Dwaracherla et al. *Efficient Exploration for LLMs*. ICML, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2402.00396)
- Kaan Gönç et al. *User Feedback-based Online Learning for Intent Classification*. ICMI, 2023. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3577190.3614137)
- Xiaoqiang Lin et al. *Use Your INSTINCT: INSTruction optimization for LLMs usIng Neural bandits Coupled with Transformers*. ICML, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2310.02905)
- Xiaqiang Tang et al. *Adapting to Non-Stationary Environments: Multi-Armed Bandit Enhanced Retrieval-Augmented Generation on Knowledge Graphs*. AAAI, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2412.07618)

##### Task-specific feature construction

- Nicole Cho et al. *No One Size Fits All: QueryBandits for Hallucination Mitigation*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.20332)
- Xinyuan Wang et al. *MixLLM: Dynamic Routing in Mixed Large Language Models*. NAACL, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.18482)
- Yuqi Tang et al. *SciToolAgent-Evo: An Ontology-Aware Self-Evolving Agent for Open-World Scientific Tool Acquisition*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2607.28692)
- Zeyu Zhang et al. *Steering Frozen LLMs: Adaptive Social Alignment via Online Prompt Routing*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2603.15647)

##### Interaction-state representation

- Xiang Li et al. *ALSO: Adversarial Online Strategy Optimization for Social Agents*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.15768)
- Hanzhuo Tan et al. *Prompt-Based Code Completion via Multi-Retrieval Augmented Generation*. ACM TOSEM, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3725812)
- Xinle Wu and Yao Lu. *Reward Model Routing in Alignment*. ICLR, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2510.02850)
- Sheldon Yu et al. *OLIVIA: Online Learning via Inference-time Action Adaptation for Decision Making in LLM ReAct Agents*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.11169)

##### Joint context--configuration representation

- Kaiyu Huang et al. *UniScale: Adaptive Unified Inference Scaling via Online Joint Optimization of Model Routing and Test-Time Scaling*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.30898)
- Xianzhi Zhang et al. *Adapter-Augmented Bandits for Online Multi-Constrained Multi-Modal Inference Scheduling*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2603.06403)

#### Action Modeling

##### Semantic action representation

- Chao-Kai Chiang, Takashi Ishida, and Masashi Sugiyama. *LLM Routing with Dueling Feedback*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2510.00841)
- Kaiyu Huang et al. *UniScale: Adaptive Unified Inference Scaling via Online Joint Optimization of Model Routing and Test-Time Scaling*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.30898)
- Haruka Kiyohara et al. *Prompt Optimization with Logged Bandit Data*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2504.02646)
- Haruka Kiyohara et al. *An Off-Policy Learning Approach for Steering Sentence Generation towards Personalization*. RecSys, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3705328.3748088)
- Donghao Li et al. *Efficient Multi-objective Prompt Optimization via Pure-exploration Bandits*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.14553)
- Zhaoxuan Wu et al. *Prompt Optimization with EASE? Efficient Ordering-aware Automated Selection of Exemplars*. NeurIPS, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2405.16122)

##### Structured action-space modeling

- Van Dai Do et al. *SPaCe: Unlocking Sample-Efficient Large Language Models Training With Self-Pace Curriculum Learning*. Findings of ACL, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.18653/v1/2026.findings-acl.171)
- Zhi Hong et al. *MASPOB: Bandit-Based Prompt Optimization for Multi-Agent Systems with Graph Neural Networks*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2603.02630)
- Darrien M. McKenzie, Nicklas Hansen, and Xiaolong Wang. *Manifold Bandits: Bayesian Curriculum Learning over the Latent Geometry of Large Language Models*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.19750)

##### Dynamic action generation

- Zelin He et al. *ReSkill: Reconciling Skill Creation with Policy Optimization in Agentic RL*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.01619)
- Shion Ishikawa et al. *Progressive Content Refinement with Decaying Reward Joint LinUCB*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2608.06750)
- Sweta Karlekar et al. *Duel-Evolve: Reward-Free Test-Time Scaling via LLM Self-Preferences*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.21585)
- Junke Zhang et al. *Evolving Skill-Structured Attack Memory Enhances LLM Jailbreaking*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.29237)

</details>

<details>
<summary><strong>Learning</strong> — 8 research streams · 20 papers</summary>

#### Warm Start

##### Synthetic interaction pretraining

- Parand Alamdari, Yanshuai Cao, and Kevin Wilson. *Jump Starting Bandits with LLM-Generated Prior Knowledge*. EMNLP, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2406.19317)
- Adam Bayley et al. *Jump Start or False Start? A Theoretical and Empirical Evaluation of LLM-initialized Bandits*. TMLR, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.02527)

##### LLM-informed Bayesian priors

- Qing Feng et al. *LLM-Informed Bayesian Content Exploration in Ultra-Recency Recommendation*. SIGIR, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3805712.3808498)
- E. Lee et al. *LLM-Derived Priors for Thompson Sampling in Cold-Start Comment Recommendation*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2608.03382)
- Xinle Wu and Yao Lu. *Reward Model Routing in Alignment*. ICLR, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2510.02850)

##### Guided initialization and early interaction

- Dingyang Chen, Qi Zhang, and Yinglun Zhu. *Efficient Sequential Decision Making with Large Language Models*. EMNLP, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2406.12125)
- Shaohua Duan et al. *Chunks as Arms: Multi-Armed Bandit-Guided Sampling for Long-Context LLM Preference Optimization*. ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2508.13993)
- Sheldon Yu et al. *OLIVIA: Online Learning via Inference-time Action Adaptation for Decision Making in LLM ReAct Agents*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.11169)

#### Reward Estimation

##### LLM-based outcome prediction

- Uljad Berdica et al. *When Do We Need LLMs? A Diagnostic for Language-Driven Bandits*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.05859)
- Nicolò Felicioni et al. *On the Importance of Uncertainty in Decision-Making with Large Language Models*. TMLR, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2404.02649)
- Jiahang Sun et al. *Large Language Model-Enhanced Multi-Armed Bandits*. ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.01118)

##### Proxy augmentation and correction

- Parand Alamdari, Yanshuai Cao, and Kevin Wilson. *Jump Starting Bandits with LLM-Generated Prior Knowledge*. EMNLP, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2406.19317)
- Ruicheng Ao et al. *Best Arm Identification with LLM Judges and Limited Human*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2601.21471)
- Tianyi Ma et al. *Best-Arm Identification with Generative Proxy*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2607.06879)
- M.N. Pershin et al. *Calibration-Gated LLM Pseudo-Observations for Online Contextual Bandits*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.14961)

##### Language-to-reward construction

- Nikhil Behari et al. *A Decision-Language Model (DLM) for Dynamic Restless Multi-Armed Bandit Tasks in Public Health*. NeurIPS, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2402.14807)
- Shresth Verma et al. *Balancing Act: Prioritization Strategies for LLM-Designed Restless Bandit Rewards*. GameSec, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2408.12112)

##### Semantic surrogate evaluation

- Nicole Cho et al. *No One Size Fits All: QueryBandits for Hallucination Mitigation*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.20332)
- Linfeng Du et al. *Optimizing User Profiles via Contextual Bandits for Retrieval-Augmented LLM Personalization*. ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2601.12078)
- Sweta Karlekar et al. *Duel-Evolve: Reward-Free Test-Time Scaling via LLM Self-Preferences*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.21585)

#### Environment Modeling

##### Textual posterior and hypothesis modeling

- Dilip Arumugam and Thomas L. Griffiths. *Toward Efficient Exploration by Large Language Model Agents*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2504.20997)

</details>

<details>
<summary><strong>Decision</strong> — 8 research streams · 13 papers</summary>

#### Exploration

##### LLM-informed uncertainty exploration

- Uljad Berdica et al. *When Do We Need LLMs? A Diagnostic for Language-Driven Bandits*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.05859)
- Nicolò Felicioni et al. *On the Importance of Uncertainty in Decision-Making with Large Language Models*. TMLR, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2404.02649)
- Jiahang Sun et al. *Large Language Model-Enhanced Multi-Armed Bandits*. ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.01118)

##### Semantic exploration-space restriction

- Keegan Harris and Aleksandrs Slivkins. *Should You Use Your Large Language Model to Explore or Exploit?* arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.00225)

##### Direct exploration control

- Sanxing Chen et al. *When Greedy Wins: Emergent Exploitation Bias in Meta-Bandit LLM Training*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2509.24923)
- J. de Curtò et al. *LLM-Informed Multi-Armed Bandit Strategies for Non-Stationary Environments*. Electronics, 2023. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.3390/electronics12132814)

##### Model-based information exploration

- Dilip Arumugam and Thomas L. Griffiths. *Toward Efficient Exploration by Large Language Model Agents*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2504.20997)

#### Action Selection

##### Direct LLM action selection

- Keegan Harris and Aleksandrs Slivkins. *Should You Use Your Large Language Model to Explore or Exploit?* arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.00225)
- Jawad Hazime and Junaid Farooq. *Evaluation of LLM Powered Agentic AI for Solving Multi-Arm Bandit Problems*. IEEE COINS, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1109/COINS65080.2025.11125743)
- Fanzeng Xia et al. *Beyond Numeric Rewards: In-Context Dueling Bandits with LLM Agents*. Findings of ACL, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.18653/v1/2025.findings-acl.519)

##### Gated and validated LLM recommendations

- Junyu Cao et al. *LIBRA: Language Model Informed Bandit Recourse Algorithm for Personalized Treatment Planning*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2601.11905)
- Fanzeng Xia et al. *Beyond Numeric Rewards: In-Context Dueling Bandits with LLM Agents*. Findings of ACL, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.18653/v1/2025.findings-acl.519)

##### LLM-guided candidate generation

- Keegan Harris and Aleksandrs Slivkins. *Should You Use Your Large Language Model to Explore or Exploit?* arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.00225)
- Zichen Liu et al. *Sample-Efficient Alignment for LLMs*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2411.01493)

##### Proxy- and diagnosis-guided allocation

- Tianyi Ma et al. *Best-Arm Identification with Generative Proxy*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2607.06879)
- Geremy Loachamín Suntaxi et al. *Learning to Choose: An Empowerment-Guided Multi-Agent System with semantic communication for Adaptive Method Selection*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.30042)

</details>

<details>
<summary><strong>Feedback</strong> — 4 research streams · 7 papers</summary>

#### Feedback Interpretation

##### Scalar and binary feedback judging

- Kexin Chu, Dawei Xiang, and Wei Zhang. *Latency-Quality Routing for Functionally Equivalent Tools in LLM Agents*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.14241)
- Aditya Ramesh et al. *Efficient Jailbreak Attack sequences on Large Language Models via Multi-Armed Bandit-based Context switching*. ICLR, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://www.semanticscholar.org/paper/ead828879a0379b248f224321bf4076e7c4b0434)

##### Pairwise preference interpretation

- Yuanchen Wu et al. *LLM Prompt Duel Optimizer: Efficient Label-Free Prompt Optimization*. Findings of ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2510.13907)

##### Semantic feedback shaping and propagation

- Son Nguyen, Xinyuan Liu, and Ransalu Senanayake. *CUPID in the Model Zoo: Online Matchmaking for Selecting Your Dream LLM*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.00846)
- Shengbo Wang, Hong Sun, and Ke Li. *Preference Is More than Comparisons: Rethinking Dueling Bandits with Augmented Human Feedback*. AAAI, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1609/aaai.v40i31.39852)

##### Structured diagnosis and attribution

- Nikhil Behari et al. *A Decision-Language Model (DLM) for Dynamic Restless Multi-Armed Bandit Tasks in Public Health*. NeurIPS, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2402.14807)
- Geremy Loachamín Suntaxi et al. *Learning to Choose: An Empowerment-Guided Multi-Agent System with semantic communication for Adaptive Method Selection*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.30042)

</details>
<!-- END AUTO-GENERATED LITERATURE NAVIGATION -->

## 📄 Bibliography

Download [`references.bib`](references.bib) for the bibliographic records used by the survey. The file includes the 153-study corpus together with supporting background and methodological references; corpus membership is determined by [`taxonomy.yaml`](taxonomy.yaml).

## 🗂️ Repository Structure

```text
.
├── README.md                # Methodology and literature navigation
├── references.bib           # Survey and supporting references
├── taxonomy.yaml            # Machine-readable corpus classification
└── LICENSE
```

## 🤝 Updates / Contributing

The **Survey Corpus Snapshot** is fixed at 153 studies through August 15, 2026. Later work may be added under **Post-Survey Updates**, clearly separated from the frozen snapshot statistics.

Suggestions for missing or newly published work are welcome through issues or pull requests. Please include an authoritative citation, a short explanation of the substantive Bandit–LLM interaction, and a proposed taxonomy location. A background mention of bandits or LLMs alone is not sufficient for inclusion.

## 📝 Citation

If this collection supports your work, please cite the accompanying survey. Complete publication metadata will be added here when the paper is publicly available.
