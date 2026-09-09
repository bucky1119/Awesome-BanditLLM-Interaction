# Awesome Bandit–LLM Interaction

We maintain a structured collection of research on the interaction between bandit learning and large language models.

[![Papers](https://img.shields.io/badge/papers-153-539AB9?style=flat-square)](#-literature-navigation)
[![Directions](https://img.shields.io/badge/directions-2-6C63A8?style=flat-square)](#-taxonomy)
[![Coverage](https://img.shields.io/badge/coverage-through_August_15%2C_2026-D97706?style=flat-square)](#-corpus-at-a-glance)
[![License: MIT](https://img.shields.io/badge/license-MIT-2EA44F?style=flat-square)](LICENSE)

[Corpus at a Glance](#corpus-at-a-glance) · [Search & Review Methodology](#search--review-methodology) · [Taxonomy](#-taxonomy) · [Literature Navigation](#-literature-navigation) · [Bibliography](#-bibliography)

## 👋 About

We maintain this companion repository for our *Bandit–LLM Interaction* survey. We organize the literature in two directions: bandit methods that improve large language model systems, and LLM capabilities that augment bandit learning. We provide the complete classification in [`taxonomy.yaml`](taxonomy.yaml) and the corresponding citation records in [`references.bib`](references.bib).

## 📊 Corpus at a Glance

> **153 unique studies · 2 directions · 8 stages · 18 components**

We froze the survey corpus at **August 15, 2026**, with **153 unique studies**. We may add newly released Bandit–LLM research after the survey cutoff as clearly marked post-survey updates.

We invite readers to use the [Literature Navigation](#-literature-navigation) to browse papers by research stream and follow each reference to a verified arXiv record or official publication page. We also provide [`references.bib`](references.bib) for citation management and [`taxonomy.yaml`](taxonomy.yaml) for reuse of our classification.

## 🔍 Search & Review Methodology

### 🧩 PCC Search Framework

To provide broad and structured coverage of the rapidly evolving literature on Bandit–LLM interaction, we organized the literature search using the Population–Concept–Context (PCC) framework.

Rather than restricting retrieval to the components of our final taxonomy, we used PCC to define a broad search space around modern LLMs, genuine bandit methods, and their substantive technical interaction.

| PCC Element | Scope in This Review |
|---|---|
| Population | We consider modern large language models (LLMs) and LLM-based systems. |
| Concept | We focus on multi-armed bandits and related genuine bandit formulations, algorithms, and sequential decision mechanisms. |
| Context | We require substantive technical interaction between LLMs and bandits, either through bandit-based control of the LLM lifecycle or LLM-based augmentation of the bandit decision pipeline. |

We used the Population and Concept dimensions to construct broad retrieval queries, and we primarily applied the Context criterion during title/abstract screening and full-text assessment. This separation helped us preserve recall during literature identification without prematurely restricting retrieval to the component taxonomy that we developed later in the review.

### 🔎 Search Strategy

We searched the literature published between **January 1, 2022 and August 15, 2026**. We use the latter date as the cutoff for our survey corpus and identify any later repository additions as **Post-Survey Updates**.

We searched **Scopus**, **Web of Science Core Collection**, **ACM Digital Library**, **IEEE Xplore**, and **arXiv** as our primary literature sources. We supplemented this search with **Google Scholar**, **Semantic Scholar**, backward citation tracing, and forward citation tracing. By combining these sources, we cover machine learning, natural language processing, information retrieval, recommender systems, data mining, operations research, and online learning.

We used the following canonical Population terms:

```text
"large language model" OR "large language models" OR LLM OR LLMs
OR "language model" OR "language models"
```

We used the following canonical Concept terms:

```text
bandit OR "multi-armed bandit" OR "multi armed bandit"
OR "contextual bandit" OR "combinatorial bandit" OR "linear bandit"
OR "bandit learning" OR "bandit algorithm" OR "Thompson sampling"
OR "upper confidence bound"
```

We combined the two groups using the following canonical search logic:

```text
(Population terms) AND (Concept terms)
```

We adapted the syntax to each database interface. We present these concepts as a canonical reproducible strategy rather than as character-for-character historical queries. We did not require taxonomy-specific terms—such as prompting, retrieval, routing, caching, agent orchestration, reward estimation, exploration, and feedback interpretation—in the initial broad query; we applied them during screening and synthesis.

### ✅ Eligibility Criteria

**Core principle:** We retained a study only when Bandit–LLM interaction formed a substantive part of its problem formulation, methodology, learning procedure, decision mechanism, or system design.

| We included | We excluded |
|---|---|
| We include studies in which modern LLMs or LLM-based systems form part of the method or studied environment. | We exclude studies in which LLMs or bandits appear only in background, introduction, related work, baselines, or incidental implementation components. |
| We include studies with a genuine bandit formulation, algorithm, exploration mechanism, or partial-feedback decision process. | We exclude studies that use “bandit” metaphorically. |
| We include studies in which bandits substantively control or adapt an LLM component, or LLMs substantively augment a bandit component. | We exclude studies that use generic reinforcement learning without a genuine bandit formulation or algorithm. |
| We include theoretical, methodological, empirical, systems, and negative-result studies. | We exclude older or generic language-model work included only because it is conceptually related. |
| We include simulated users, proxy tasks, synthetic data, and synthetic environments when the interaction is methodologically substantive. | We exclude reports with insufficient technical information to determine the substantive interaction. |
| We include peer-reviewed, accepted, forthcoming, and high-quality preprint studies, and we impose no venue restriction. | We do not count duplicate or superseded versions of the same substantive study independently. |

We preferred the final published version where available. We treated a later conference or journal publication and its earlier preprint as one substantive study unless they clearly constituted distinct technical contributions.

**Operational scope.** We define **Bandit-Enhanced Large Language Models** as work in which bandit methods adapt or control computational decisions across Pre-training → Post-training → Utilization → Evaluation. We define **LLM-Enhanced Bandits** as work in which LLMs augment Representation → Learning → Decision → Feedback. We assign a study to both directions when both interactions are methodologically substantive.

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

We first screened candidate studies by title and abstract using the PCC scope. We retained ambiguous studies for full-text assessment rather than excluding them prematurely. For eligible studies, we consolidated multiple versions of the same substantive work and preferred the final published version where available.

We extracted evidence on the problem formulation, Bandit–LLM intervention mechanism, bandit formulation, LLM integration, theoretical analysis, experimental setting, empirical findings, comparisons and ablations, and reported limitations. We used this evidence to develop our component-level synthesis and bidirectional taxonomy.

## 🧭 Taxonomy

We organize the literature according to where one technology intervenes in the computational process of the other. For **Bandit-Enhanced Large Language Models**, we follow the LLM lifecycle—Pre-training, Post-training, Utilization, and Evaluation. For **LLM-Enhanced Bandits**, we follow the bandit decision pipeline—Representation, Learning, Decision, and Feedback.

We allow multi-component and bidirectional studies to appear in multiple research streams. We provide our complete reusable classification in [`taxonomy.yaml`](taxonomy.yaml).

## 📚 Literature Navigation

We place a study in multiple research streams when it contains multiple substantive intervention mechanisms. We provide two complementary views: component-level tables for structural comparison and a detailed paper index for title-based browsing. Both views cover all 153 studies.

**Choose a view:** [Component-Level Overview](#component-level-overview) · [Detailed Paper Index](#detailed-paper-index)

<!-- BEGIN AUTO-GENERATED LITERATURE NAVIGATION -->
### Component-Level Overview

We present each stage using the same four-column structure as our survey: Component, Research Stream, intervention mechanism, and References. We link every reference label directly to a verified arXiv record or, when no arXiv identifier is available, the official publication page.

#### Bandit-Enhanced Large Language Models

<details>
<summary><strong>Pre-training</strong> — 2 research streams · 2 papers</summary>

<br>

<table>
<thead>
<tr>
<th>Component</th>
<th>Research Stream</th>
<th>Bandit Intervention</th>
<th>References</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="2"><strong>Pre-training</strong></td>
<td>Adaptive data mixing</td>
<td>Allocate updates across data domains or sources</td>
<td><a href="https://arxiv.org/abs/2312.02406" title="Efficient Online Data Mixing For Language Model Pre-Training">Albalak et al. (2023)</a></td>
</tr>
<tr>
<td>Pre-training configuration optimization</td>
<td>Adapt masking policies or training configurations</td>
<td><a href="https://arxiv.org/abs/2203.13151" title="Multi-armed bandits for resource efficient, online optimization of language model pre-training: the use case of dynamic masking">Urteaga et al. (2023)</a></td>
</tr>
</tbody>
</table>

</details>

<details>
<summary><strong>Post-training</strong> — 7 research streams · 28 papers</summary>

<br>

<table>
<thead>
<tr>
<th>Component</th>
<th>Research Stream</th>
<th>Bandit Intervention</th>
<th>References</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><strong>Fine-tuning</strong></td>
<td>Adaptive curriculum and training-data scheduling</td>
<td>Adapt datasets, examples, rollouts, or tasks to the evolving learning state</td>
<td><a href="https://doi.org/10.18653/v1/2026.findings-acl.171" title="SPaCe: Unlocking Sample-Efficient Large Language Models Training With Self-Pace Curriculum Learning">Do et al. (2026)</a>; <a href="https://arxiv.org/abs/2602.08499" title="Contextual Rollout Bandits for Reinforcement Learning with Verifiable Rewards">Lu et al. (2026)</a>; <a href="https://arxiv.org/abs/2606.19750" title="Manifold Bandits: Bayesian Curriculum Learning over the Latent Geometry of Large Language Models">McKenzie et al. (2026)</a>; <a href="https://doi.org/10.18653/v1/2026.findings-acl.1972" title="DynamixSFT: Dynamic Mixture Optimization of Instruction Tuning Collections">Shin et al. (2026)</a>; <a href="https://doi.org/10.1145/3770855.3817990" title="Distribution-Value Coevolution for Adaptive RLHF Data Scheduling">Yang et al. (2026)</a></td>
</tr>
<tr>
<td>Online experience and skill control</td>
<td>Regulate newly generated experience, auxiliary skills, or reward-driven updates</td>
<td><a href="https://doi.org/10.1145/3577190.3614137" title="User Feedback-based Online Learning for Intent Classification">Gönç et al. (2023)</a>; <a href="https://arxiv.org/abs/2606.01619" title="ReSkill: Reconciling Skill Creation with Policy Optimization in Agentic RL">He et al. (2026)</a>; <a href="https://arxiv.org/abs/2601.14599" title="Rethinking Reinforcement fine-tuning of LLMs: A Multi-armed Bandit Learning Perspective">Hu et al. (2026)</a></td>
</tr>
<tr>
<td>Bandit-guided policy learning and co-evolution</td>
<td>Train or control evolving decision policies under sequential reward feedback</td>
<td><a href="https://arxiv.org/abs/2509.24923" title="When Greedy Wins: Emergent Exploitation Bias in Meta-Bandit LLM Training">Chen et al. (2025)</a>; <a href="https://arxiv.org/abs/2410.06238" title="EVOLvE: Evaluating and Optimizing LLMs For In-Context Exploration">Nie et al. (2025)</a>; <a href="https://arxiv.org/abs/2504.16078" title="LLMs are Greedy Agents: Effects of RL Fine-tuning on Decision-Making Abilities">Schmied et al. (2026)</a>; <a href="https://doi.org/10.1145/3589334.3645420" title="Which LLM to Play? Convergence-Aware Online Model Selection with Time-Increasing Bandits">Xia et al. (2024)</a></td>
</tr>
<tr>
<td rowspan="4"><strong>Alignment</strong></td>
<td>Active preference acquisition</td>
<td>Allocate limited feedback to informative contexts, responses, or comparisons</td>
<td><a href="https://doi.org/10.1007/978-3-032-06096-9_6" title="Active Preference Optimization for Sample Efficient RLHF">Das et al. (2025)</a>; <a href="https://arxiv.org/abs/2402.00396" title="Efficient Exploration for LLMs">Dwaracherla et al. (2024)</a>; <a href="https://arxiv.org/abs/2402.09401" title="Reinforcement Learning from Human Feedback with Active Queries">Ji et al. (2025)</a>; <a href="https://arxiv.org/abs/2312.00267" title="Sample Efficient Preference Alignment in LLMs via Active Exploration">Mehta et al. (2023)</a>; <a href="https://arxiv.org/abs/2410.17055" title="Optimal Design for Reward Modeling in RLHF">Scheid et al. (2024)</a></td>
</tr>
<tr>
<td>Exploration-aware preference optimization</td>
<td>Expand response-space coverage through uncertainty-aware exploration</td>
<td><a href="https://arxiv.org/abs/2501.12735" title="Online Preference Alignment for Language Models via Count-based Exploration">Bai et al. (2025)</a>; <a href="https://arxiv.org/abs/2405.21046" title="Exploratory Preference Optimization: Harnessing Implicit Q*-Approximation for Sample-Efficient RLHF">Xie et al. (2025)</a>; <a href="https://arxiv.org/abs/2312.11456" title="Iterative Preference Learning from Human Feedback: Bridging Theory and Practice for RLHF under KL-constraint">Xiong et al. (2024)</a>; <a href="https://arxiv.org/abs/2405.19332" title="Self-Exploring Language Models: Active Preference Elicitation for Online Alignment">Zhang et al. (2025)</a></td>
</tr>
<tr>
<td>Policy-coupled online alignment</td>
<td>Adapt comparison collection and preference updates to the evolving policy</td>
<td><a href="https://doi.org/10.52202/085713-5567" title="Provably Efficient Online RLHF with One-Pass Reward Modeling">Li et al. (2025)</a>; <a href="https://arxiv.org/abs/2509.22633" title="Towards Efficient Online Exploration for Reinforcement Learning with Human Feedback">Li &amp; Yan (2025)</a></td>
</tr>
<tr>
<td>Adaptive supervision and feedback control</td>
<td>Select and adapt reward signals, evidence, logged feedback, or response candidates</td>
<td><a href="https://arxiv.org/abs/2508.13993" title="Chunks as Arms: Multi-Armed Bandit-Guided Sampling for Long-Context LLM Preference Optimization">Duan et al. (2026)</a>; <a href="https://arxiv.org/abs/2310.12036" title="A General Theoretical Paradigm to Understand Learning from Human Preferences">Azar et al. (2024)</a>; <a href="https://arxiv.org/abs/2605.18899" title="Don&#x27;t Let Bandit Feedback Pull Continual LLM-Recommender Updates Off Target">Kim et al. (2026)</a>; <a href="https://arxiv.org/abs/2410.14001" title="Personalized Adaptation via In-Context Preference Learning">Lau et al. (2024)</a>; <a href="https://arxiv.org/abs/2411.01493" title="Sample-Efficient Alignment for LLMs">Liu et al. (2024)</a>; <a href="https://arxiv.org/abs/2410.01735" title="LASeR: Learning to Adaptively Select Reward Models with Multi-Arm Bandits">Nguyen et al. (2025)</a></td>
</tr>
</tbody>
</table>

</details>

<details>
<summary><strong>Utilization</strong> — 23 research streams · 96 papers</summary>

<br>

<table>
<thead>
<tr>
<th>Component</th>
<th>Research Stream</th>
<th>Bandit Intervention</th>
<th>References</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="4"><strong>Prompting</strong></td>
<td>Fixed-pool prompt selection and structured sharing</td>
<td>Allocate evaluations across prompt candidates while sharing evidence through representations, features, preferences, or distributed statistics</td>
<td><a href="https://doi.org/10.52202/079017-3161" title="Efficient Prompt Optimization Through the Lens of Best Arm Identification">Shi et al. (2024)</a>; <a href="https://arxiv.org/abs/2310.02905" title="Use Your INSTINCT: INSTruction optimization for LLMs usIng Neural bandits Coupled with Transformers">Lin et al. (2024)</a>; <a href="https://arxiv.org/abs/2405.16122" title="Prompt Optimization with EASE? Efficient Ordering-aware Automated Selection of Exemplars">Wu et al. (2024)</a>; <a href="https://arxiv.org/abs/2501.03508" title="SOPL: A Sequential Optimal Learning Approach to Automated Prompt Engineering in Large Language Models">Wang et al. (2025)</a>; <a href="https://arxiv.org/abs/2509.24701" title="FedPOB: Sample-Efficient Federated Prompt Optimization via Bandits">Lu et al. (2025)</a>; <a href="https://arxiv.org/abs/2605.14553" title="Efficient Multi-objective Prompt Optimization via Pure-exploration Bandits">Li et al. (2026)</a>; <a href="https://arxiv.org/abs/2405.17346" title="Prompt Optimization with Human Feedback">Lin et al. (2024)</a>; <a href="https://arxiv.org/abs/2510.13907" title="LLM Prompt Duel Optimizer: Efficient Label-Free Prompt Optimization">Wu et al. (2026)</a></td>
</tr>
<tr>
<td>Prompt generation and refinement</td>
<td>Adapt prompt-generation or modification strategies as the candidate space evolves</td>
<td><a href="https://doi.org/10.18653/v1/2025.findings-acl.1070" title="Bandit-Based Prompt Design Strategy Selection Improves Prompt Optimizers">Ashizawa et al. (2025)</a>; <a href="https://doi.org/10.1145/3746252.3760824" title="TwinBandit Prompt Optimizer: Adaptive Prompt Optimization via Synergistic Dual MAB-Guided Feedback">Park et al. (2025)</a>; <a href="https://arxiv.org/abs/2502.00728" title="Meta-Prompt Optimization for LLM-Based Sequential Decision Making">Kong et al. (2025)</a>; <a href="https://arxiv.org/abs/2603.02630" title="MASPOB: Bandit-Based Prompt Optimization for Multi-Agent Systems with Graph Neural Networks">Hong et al. (2026)</a></td>
</tr>
<tr>
<td>Contextual and deployment-time prompting</td>
<td>Select or adapt prompts according to users, queries, dialogue state, or interaction history</td>
<td><a href="https://doi.org/10.1145/3677052.3698651" title="Online Personalizing White-box LLMs Generation with Neural Bandits">Chen et al. (2024)</a>; <a href="https://arxiv.org/abs/2602.20332" title="No One Size Fits All: QueryBandits for Hallucination Mitigation">Cho et al. (2026)</a>; <a href="https://arxiv.org/abs/2608.06750" title="Progressive Content Refinement with Decaying Reward Joint LinUCB">Ishikawa et al. (2026)</a>; <a href="https://arxiv.org/abs/2605.15768" title="ALSO: Adversarial Online Strategy Optimization for Social Agents">Li et al. (2026)</a>; <a href="https://arxiv.org/abs/2410.05362" title="LLMs Are In-Context Bandit Reinforcement Learners">Monea et al. (2024)</a>; <a href="https://arxiv.org/abs/2410.06238" title="EVOLvE: Evaluating and Optimizing LLMs For In-Context Exploration">Nie et al. (2025)</a>; <a href="https://www.semanticscholar.org/paper/ead828879a0379b248f224321bf4076e7c4b0434" title="Efficient Jailbreak Attack sequences on Large Language Models via Multi-Armed Bandit-based Context switching">Ramesh et al. (2025)</a></td>
</tr>
<tr>
<td>Joint prompt and system optimization</td>
<td>Optimize prompts jointly with retrieval, inference compute, logged feedback, or surrounding workflow decisions</td>
<td><a href="https://arxiv.org/abs/2406.19251" title="AutoRAG-HP: Automatic Online Hyper-Parameter Tuning for Retrieval-Augmented Generation">Fu et al. (2024)</a>; <a href="https://arxiv.org/abs/2501.05247" title="Online Prompt Selection for Program Synthesis">Li et al. (2025)</a>; <a href="https://arxiv.org/abs/2508.10030" title="Inference-Aware Prompt Optimization for Aligning Black-Box Large Language Models">Mahmud et al. (2026)</a>; <a href="https://arxiv.org/abs/2504.02646" title="Prompt Optimization with Logged Bandit Data">Kiyohara et al. (2025)</a>; <a href="https://doi.org/10.1145/3705328.3748088" title="An Off-Policy Learning Approach for Steering Sentence Generation towards Personalization">Kiyohara et al. (2025)</a>; <a href="https://arxiv.org/abs/2604.27209" title="Theory Under Construction: Orchestrating Language Models for Research Software Where the Specification Evolves">Young &amp; Björner (2026)</a></td>
</tr>
<tr>
<td rowspan="3"><strong>Retrieval</strong></td>
<td>Retrieval strategy and configuration adaptation</td>
<td>Adapt retrieval depth, strategy, or RAG configuration according to request-level utility and cost</td>
<td><a href="https://arxiv.org/abs/2412.01572" title="MBA-RAG: a Bandit Approach for Adaptive Retrieval-Augmented Generation through Question Complexity">Tang et al. (2025)</a>; <a href="https://doi.org/10.1109/ICPADS67057.2025.11322957" title="Relative Performance Bandits: An Adaptive RAG Framework with Reward-Aware Exploration">Dai et al. (2025)</a>; <a href="https://arxiv.org/abs/2406.19251" title="AutoRAG-HP: Automatic Online Hyper-Parameter Tuning for Retrieval-Augmented Generation">Fu et al. (2024)</a></td>
</tr>
<tr>
<td>Evidence allocation and selection</td>
<td>Allocate limited retrieval or context capacity across candidate evidence sources</td>
<td><a href="https://arxiv.org/abs/2510.18633" title="Query Decomposition for RAG: Balancing Exploration-Exploitation">Petcu et al. (2026)</a>; <a href="https://doi.org/10.1145/3725812" title="Prompt-Based Code Completion via Multi-Retrieval Augmented Generation">Tan et al. (2026)</a>; <a href="https://arxiv.org/abs/2601.12078" title="Optimizing User Profiles via Contextual Bandits for Retrieval-Augmented LLM Personalization">Du et al. (2026)</a></td>
</tr>
<tr>
<td>Retrieval computation and dynamic memory control</td>
<td>Allocate retrieval-side computation or select useful information from evolving memory repositories</td>
<td><a href="https://arxiv.org/abs/2602.02827" title="Col-Bandit: Zero-Shot Query-Time Pruning for Late-Interaction Retrieval">Pony et al. (2026)</a>; <a href="https://arxiv.org/abs/2605.29237" title="Evolving Skill-Structured Attack Memory Enhances LLM Jailbreaking">Zhang et al. (2026)</a></td>
</tr>
<tr>
<td rowspan="5"><strong>Routing</strong></td>
<td>Contextual model routing</td>
<td>Match requests to individual LLMs using contextual rewards, representations, priors, or auxiliary feedback</td>
<td><a href="https://arxiv.org/abs/2410.13287" title="PAK-UCB Contextual Bandit: An Online Learning Approach to Prompt-Aware Selection of Generative Models and LLMs">Hu et al. (2025)</a>; <a href="https://arxiv.org/abs/2407.10834" title="MetaLLM: A High-performant and Cost-efficient Dynamic Framework for Wrapping LLMs">Nguyen et al. (2024)</a>; <a href="https://arxiv.org/abs/2603.30035" title="Reward-Based Online LLM Routing via NeuralUCB">Tsai &amp; Tran (2026)</a>; <a href="https://arxiv.org/abs/2510.00841" title="LLM Routing with Dueling Feedback">Chiang et al. (2025)</a>; <a href="https://arxiv.org/abs/2508.21141" title="Adaptive LLM Routing under Budget Constraints">Panda et al. (2025)</a>; <a href="https://arxiv.org/abs/2605.30736" title="OrcaRouter: A Production-Oriented LLM Router with Hybrid Offline-Online Learning">Bao et al. (2026)</a>; <a href="https://arxiv.org/abs/2607.09015" title="Correlation-Aware Contextual Bandits with Surrogate Rewards for LLM Routing">Sridhar et al. (2026)</a>; <a href="https://arxiv.org/abs/2606.00846" title="CUPID in the Model Zoo: Online Matchmaking for Selecting Your Dream LLM">Nguyen et al. (2026)</a>; <a href="https://arxiv.org/abs/2512.03065" title="Optimizing Life Sciences Agents in Real-Time using Reinforcement Learning">Chadderwala (2025)</a>; <a href="https://arxiv.org/abs/2506.17670" title="Online Multi-LLM Selection via Contextual Bandits Under Unstructured Context Evolution">Poon et al. (2026)</a>; <a href="https://arxiv.org/abs/2605.14241" title="Latency-Quality Routing for Functionally Equivalent Tools in LLM Agents">Chu et al. (2026)</a></td>
</tr>
<tr>
<td>Resource-aware and constrained routing</td>
<td>Allocate models under quality–cost trade-offs, budgets, capacities, queues, or other operational constraints</td>
<td><a href="https://arxiv.org/abs/2407.10834" title="MetaLLM: A High-performant and Cost-efficient Dynamic Framework for Wrapping LLMs">Nguyen et al. (2024)</a>; <a href="https://arxiv.org/abs/2502.02743" title="LLM Bandit: Cost-Efficient LLM Generation via Preference-Conditioned Dynamic Routing">Li (2025)</a>; <a href="https://arxiv.org/abs/2510.07429" title="Learning to Route LLMs from Bandit Feedback: One Policy, Many Trade-offs">Wei et al. (2025)</a>; <a href="https://arxiv.org/abs/2601.17551" title="GreenServ: Energy-Efficient Context-Aware Dynamic Routing for Multi-Model LLM Inference">Ziller et al. (2026)</a>; <a href="https://arxiv.org/abs/2405.16587" title="Cost-Effective Online Multi-LLM Selection with Versatile Reward Models">Dai et al. (2024)</a>; <a href="https://arxiv.org/abs/2606.17489" title="Online LLM Selection via Constrained Bandits with Time-Varying Demand">Huang et al. (2026)</a>; <a href="https://arxiv.org/abs/2605.27999" title="Learning to Assign Prediction Tasks to Agents with Capacity Constraints">Wu et al. (2026)</a>; <a href="https://arxiv.org/abs/2602.02061" title="Learning to Route and Schedule LLMs from User Retrials via Contextual Queueing Bandits">Bae et al. (2026)</a>; <a href="https://arxiv.org/abs/2604.00136" title="ParetoBandit: Budget-Paced Adaptive Routing for Non-Stationary LLM Serving">Taberner-Miller (2026)</a>; <a href="https://doi.org/10.1145/3774904.3792725" title="BARouter: A Budget-adaptive Online Large Language Model Router Framework">Zu et al. (2026)</a>; <a href="https://arxiv.org/abs/2603.06403" title="Adapter-Augmented Bandits for Online Multi-Constrained Multi-Modal Inference Scheduling">Zhang et al. (2026)</a>; <a href="https://doi.org/10.65109/MBRQ7564" title="Truthful Reverse Auctions for Adaptive Selection via Contextual Multi-Armed Bandits">Patra et al. (2026)</a></td>
</tr>
<tr>
<td>Sequential and combinatorial routing</td>
<td>Select cascades, repeated attempts, subsets, or ensembles involving multiple serving options</td>
<td><a href="https://arxiv.org/abs/2508.09958" title="Neural Bandit Based Optimal LLM Selection for Pipeline of Tasks">Atalar (2026)</a>; <a href="https://arxiv.org/abs/2606.07392" title="Online Pandora&#x27;s Box for Contextual LLM Cascading">Belloni et al. (2026)</a>; <a href="https://arxiv.org/abs/2505.18901" title="PromptWise: Online Learning for Cost-Aware Prompt Assignment in Generative Models">Hu et al. (2025)</a>; <a href="https://doi.org/10.1109/TON.2026.3663325" title="Combinatorial Logistic Online Learning and Its Applications in Nonlinear Networked Systems">Liu et al. (2026)</a>; <a href="https://www.semanticscholar.org/paper/2a86869b09d5df9b42629881ce0861f20e4cab20" title="CoCoMaMa: Contextual Combinatorial Multi-Armed Bandit Router for Multi-Agent Systems with Volatile Arms">Rau et al. (2025)</a>; <a href="https://doi.org/10.1145/3770855.3817902" title="CES: Combinatorial Experts Selection via Contextual Linear Bandits">Xu et al. (2026)</a></td>
</tr>
<tr>
<td>Composite serving-configuration routing</td>
<td>Route over speculative decoding, model–prompt–tool combinations, retrieval paths, compute budgets, or cached model states</td>
<td><a href="https://arxiv.org/abs/2408.08470" title="Context-Aware Assistant Selection for Improved Inference Acceleration with Large Language Models">Huang et al. (2024)</a>; <a href="https://arxiv.org/abs/2505.15141" title="BanditSpec: Adaptive Speculative Decoding via Bandit Algorithms">Hou et al. (2025)</a>; <a href="https://arxiv.org/abs/2604.05417" title="Multi-Drafter Speculative Decoding with Alignment Feedback">Kim et al. (2026)</a>; <a href="https://arxiv.org/abs/2501.05247" title="Online Prompt Selection for Program Synthesis">Li et al. (2025)</a>; <a href="https://doi.org/10.1109/CSCWD68734.2026.11582347" title="CH-RAG: Complexity-Guided Hybrid Retrieval-Augmented for Adaptive LLM Generation">Ren et al. (2026)</a>; <a href="https://arxiv.org/abs/2412.07618" title="Adapting to Non-Stationary Environments: Multi-Armed Bandit Enhanced Retrieval-Augmented Generation on Knowledge Graphs">Tang et al. (2025)</a>; <a href="https://arxiv.org/abs/2605.30898" title="UniScale: Adaptive Unified Inference Scaling via Online Joint Optimization of Model Routing and Test-Time Scaling">Huang et al. (2026)</a>; <a href="https://arxiv.org/abs/2604.16583" title="POLAR: Online Learning for LoRA Adapter Caching and Routing in Edge LLM Serving">Li &amp; Li (2026)</a>; <a href="https://doi.org/10.1109/ICAISET66439.2026.11542012" title="Cost-Aware LLM Orchestration via Contextual Bandit Learning">Jadav et al. (2026)</a></td>
</tr>
<tr>
<td>Adaptive routing under system change</td>
<td>Adapt routing as reward mappings, model pools, retrievers, services, or model quality change over time</td>
<td><a href="https://arxiv.org/abs/2406.12125" title="Efficient Sequential Decision Making with Large Language Models">Chen et al. (2024)</a>; <a href="https://arxiv.org/abs/2506.17254" title="Near-Optimal Online Deployment and Routing for Streaming LLMs">Li &amp; Li (2026)</a>; <a href="https://arxiv.org/abs/2510.02850" title="Reward Model Routing in Alignment">Wu &amp; Lu (2026)</a>; <a href="https://doi.org/10.1145/3589334.3645420" title="Which LLM to Play? Convergence-Aware Online Model Selection with Time-Increasing Bandits">Xia et al. (2024)</a>; <a href="https://arxiv.org/abs/2604.00136" title="ParetoBandit: Budget-Paced Adaptive Routing for Non-Stationary LLM Serving">Taberner-Miller (2026)</a>; <a href="https://arxiv.org/abs/2502.18482" title="MixLLM: Dynamic Routing in Mixed Large Language Models">Wang et al. (2025)</a>; <a href="https://arxiv.org/abs/2412.07618" title="Adapting to Non-Stationary Environments: Multi-Armed Bandit Enhanced Retrieval-Augmented Generation on Knowledge Graphs">Tang et al. (2025)</a></td>
</tr>
<tr>
<td rowspan="4"><strong>Generation</strong></td>
<td>Adaptive decoding and inference policies</td>
<td>Select decoding, speculative-inference, or inference-scaling configurations according to context and compute</td>
<td><a href="https://arxiv.org/abs/2505.15141" title="BanditSpec: Adaptive Speculative Decoding via Bandit Algorithms">Hou et al. (2025)</a>; <a href="https://arxiv.org/abs/2511.02017" title="TapOut: A Bandit-Based Approach to Dynamic Speculative Decoding">Sridhar et al. (2025)</a>; <a href="https://arxiv.org/abs/2603.09065" title="Learning Adaptive LLM Decoding">Su et al. (2026)</a>; <a href="https://arxiv.org/abs/2605.30898" title="UniScale: Adaptive Unified Inference Scaling via Online Joint Optimization of Model Routing and Test-Time Scaling">Huang et al. (2026)</a>; <a href="https://arxiv.org/abs/2508.10030" title="Inference-Aware Prompt Optimization for Aligning Black-Box Large Language Models">Mahmud et al. (2026)</a></td>
</tr>
<tr>
<td>Response- and token-level adaptive generation</td>
<td>Adapt response production or token-level decisions from sequential preference or reward feedback</td>
<td><a href="https://arxiv.org/abs/2410.14001" title="Personalized Adaptation via In-Context Preference Learning">Lau et al. (2024)</a>; <a href="https://arxiv.org/abs/2509.24696" title="T-POP: Test-Time Personalization with Online Preference Feedback">Qu et al. (2025)</a>; <a href="https://arxiv.org/abs/2506.07276" title="Tokenized Bandit for LLM Decoding and Alignment">Shin et al. (2025)</a></td>
</tr>
<tr>
<td>Test-time compute and candidate allocation</td>
<td>Allocate additional generation across queries, evolving candidates, or evaluators</td>
<td><a href="https://arxiv.org/abs/2506.12721" title="Strategic Scaling of Test-Time Compute: A Bandit Learning Approach">Zuo &amp; Zhu (2025)</a>; <a href="https://arxiv.org/abs/2602.21585" title="Duel-Evolve: Reward-Free Test-Time Scaling via LLM Self-Preferences">Karlekar et al. (2026)</a>; <a href="https://arxiv.org/abs/2410.01735" title="LASeR: Learning to Adaptively Select Reward Models with Multi-Arm Bandits">Nguyen et al. (2025)</a></td>
</tr>
<tr>
<td>Structured intermediate generation control</td>
<td>Select compact intermediate actions or optimization strategies that guide open-ended LLM generation</td>
<td><a href="https://arxiv.org/abs/2506.07275" title="Tailored Behavior-Change Messaging for Physical Activity: Integrating Contextual Bandits and Large Language Models">Song et al. (2025)</a>; <a href="https://arxiv.org/abs/2511.18868" title="KernelBand: Boosting LLM-based Kernel Optimization with a Hierarchical and Hardware-aware Multi-armed Bandit">Ran et al. (2025)</a></td>
</tr>
<tr>
<td rowspan="3"><strong>Caching</strong></td>
<td>Exact response-cache management</td>
<td>Learn retention, replacement, and reuse of exact query–response pairs under limited cache capacity</td>
<td><a href="https://arxiv.org/abs/2509.15515" title="LLM Cache Bandit Revisited: Addressing Query Heterogeneity for Cost-Effective LLM Inference">Yang et al. (2025)</a></td>
</tr>
<tr>
<td>Semantic caching</td>
<td>Reuse responses across semantically related requests while balancing inference cost against reuse mismatch</td>
<td><a href="https://doi.org/10.1109/INFOCOM59046.2026.11571467" title="Semantic Caching for Low-Cost LLM Serving: From Offline Learning to Online Adaptation">Liu et al. (2026)</a>; <a href="https://arxiv.org/abs/2604.20021" title="Continuous Semantic Caching for Low-Cost LLM Serving">Atalar et al. (2026)</a></td>
</tr>
<tr>
<td>Model-state caching</td>
<td>Jointly learn request routing and residency of reusable model states</td>
<td><a href="https://arxiv.org/abs/2604.16583" title="POLAR: Online Learning for LoRA Adapter Caching and Routing in Edge LLM Serving">Li &amp; Li (2026)</a></td>
</tr>
<tr>
<td rowspan="4"><strong>Agent Orchestration</strong></td>
<td>Local agent and tool selection</td>
<td>Select reasoning modes, tools, specialists, executors, or local orchestration configurations during execution</td>
<td><a href="https://arxiv.org/abs/2512.03065" title="Optimizing Life Sciences Agents in Real-Time using Reinforcement Learning">Chadderwala (2025)</a>; <a href="https://arxiv.org/abs/2605.11169" title="OLIVIA: Online Learning via Inference-time Action Adaptation for Decision Making in LLM ReAct Agents">Yu et al. (2026)</a>; <a href="https://arxiv.org/abs/2607.28692" title="SciToolAgent-Evo: An Ontology-Aware Self-Evolving Agent for Open-World Scientific Tool Acquisition">Tang et al. (2026)</a>; <a href="https://arxiv.org/abs/2602.00966" title="Symphony-Coord: Adaptive Routing for Multi-Agent LLM Systems">Guan et al. (2026)</a>; <a href="https://arxiv.org/abs/2608.00215" title="Personalizing Large Language Model Agents with Small Policy Models">Jin et al. (2026)</a></td>
</tr>
<tr>
<td>Workflow and topology control</td>
<td>Adapt communication structures, collaboration protocols, pipelines, or joint multi-agent configurations</td>
<td><a href="https://arxiv.org/abs/2409.13447" title="AQA: Adaptive Question Answering in a Society of LLMs via Contextual Multi-Armed Bandit">Hoveyda et al. (2024)</a>; <a href="https://arxiv.org/abs/2607.25446" title="Toward an Organizational Science of Multi-Agent LLM Systems: Decoupling Who, How, and Which Algorithm">Chen et al. (2026)</a>; <a href="https://doi.org/10.1109/ICAISET66439.2026.11542012" title="Cost-Aware LLM Orchestration via Contextual Bandit Learning">Jadav et al. (2026)</a>; <a href="https://arxiv.org/abs/2605.30042" title="Learning to Choose: An Empowerment-Guided Multi-Agent System with semantic communication for Adaptive Method Selection">Suntaxi et al. (2026)</a>; <a href="https://arxiv.org/abs/2508.09958" title="Neural Bandit Based Optimal LLM Selection for Pipeline of Tasks">Atalar (2026)</a>; <a href="https://arxiv.org/abs/2405.16587" title="Cost-Effective Online Multi-LLM Selection with Versatile Reward Models">Dai et al. (2024)</a></td>
</tr>
<tr>
<td>Adaptive computation allocation</td>
<td>Allocate additional LLM calls, iterations, branches, or search effort within an ongoing workflow</td>
<td><a href="https://arxiv.org/abs/2606.07392" title="Online Pandora&#x27;s Box for Contextual LLM Cascading">Belloni et al. (2026)</a>; <a href="https://arxiv.org/abs/2405.17503" title="Code Repair with LLMs gives an Exploration-Exploitation Tradeoff">Tang et al. (2024)</a>; <a href="https://arxiv.org/abs/2605.29268" title="Compute Allocation in Evolutionary Search: From Depth-Breadth to Multi-Armed Bandits">Xing et al. (2026)</a></td>
</tr>
<tr>
<td>Trust, verification, and integrity control</td>
<td>Adapt trust, validation, fallback, grounding, or integrity mechanisms during agentic execution</td>
<td><a href="https://doi.org/10.18653/v1/2025.findings-acl.519" title="Beyond Numeric Rewards: In-Context Dueling Bandits with LLM Agents">Xia et al. (2025)</a>; <a href="https://arxiv.org/abs/2604.27209" title="Theory Under Construction: Orchestrating Language Models for Research Software Where the Specification Evolves">Young &amp; Björner (2026)</a></td>
</tr>
</tbody>
</table>

</details>

<details>
<summary><strong>Evaluation</strong> — 4 research streams · 11 papers</summary>

<br>

<table>
<thead>
<tr>
<th>Component</th>
<th>Research Stream</th>
<th>Bandit Intervention</th>
<th>References</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="4"><strong>Adaptive Evaluation</strong></td>
<td>Best-model identification</td>
<td>Allocate evaluation budget toward candidate models that remain plausible winners while exploiting shared evaluation structure</td>
<td><a href="https://arxiv.org/abs/2407.06172" title="On Speeding Up Language Model Evaluation">Zhou et al. (2025)</a>; <a href="https://arxiv.org/abs/2605.10405" title="Valid Best-Model Identification for LLM Evaluation via Low-Rank Factorization">Tolochinsky et al. (2026)</a>; <a href="https://arxiv.org/abs/2606.07726" title="Cutting LLM Evaluation Costs with SySRs: A Bandit Algorithm that Provably Exploits Model Similarity">Lyu et al. (2026)</a></td>
</tr>
<tr>
<td>Ranking and Pareto identification</td>
<td>Allocate evaluations to resolve uncertain rankings or identify nondominated configurations under multiple objectives</td>
<td><a href="https://arxiv.org/abs/2608.03437" title="Dynamically Allocating Evaluation Effort for Model Ranking">Zouhar et al. (2026)</a>; <a href="https://arxiv.org/abs/2608.04333" title="Cost-Aware Multi-Objective Bandits: Theory and Application to Budgeted LLM Configuration Evaluation">Xue et al. (2026)</a></td>
</tr>
<tr>
<td>Preference- and judge-based evaluation</td>
<td>Allocate pairwise comparisons or repeated judge calls according to information, cost, or evaluation uncertainty</td>
<td><a href="https://doi.org/10.65109/GEKA7634" title="Cost-Aware Best Arm Identification via Dueling Feedback with Applications to Large Language Models">Gharat et al. (2026)</a>; <a href="https://arxiv.org/abs/2602.15481" title="LLM-as-Judge on a Budget">Saha et al. (2026)</a></td>
</tr>
<tr>
<td>Adaptive diagnostic evaluation</td>
<td>Direct evaluation toward informative responses, context perturbations, behavioral probes, or evolving candidate solutions</td>
<td><a href="https://doi.org/10.1609/aaai.v40i44.41064" title="A Multi-Agent Conversational Bandit Approach to Online Evaluation and Selection of User-Aligned LLM Responses">Dai et al. (2026)</a>; <a href="https://arxiv.org/abs/2506.19977" title="Context Attribution with Multi-Armed Bandit Optimization">Pan et al. (2026)</a>; <a href="https://arxiv.org/abs/2403.15371" title="Can large language models explore in-context?">Krishnamurthy et al. (2024)</a>; <a href="https://arxiv.org/abs/2602.21585" title="Duel-Evolve: Reward-Free Test-Time Scaling via LLM Self-Preferences">Karlekar et al. (2026)</a></td>
</tr>
</tbody>
</table>

</details>


#### LLM-Enhanced Bandits

<details>
<summary><strong>Representation</strong> — 8 research streams · 27 papers</summary>

<br>

<table>
<thead>
<tr>
<th>Component</th>
<th>Research Stream</th>
<th>LLM Intervention</th>
<th>References</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="4"><strong>Context Representation</strong></td>
<td>Semantic context encoding</td>
<td>Encode textual or prompt–response contexts into dense semantic features for reward prediction and exploration</td>
<td><a href="https://arxiv.org/abs/2311.02268" title="LLMs-augmented Contextual Bandit">Baheri &amp; Alm (2023)</a>; <a href="https://arxiv.org/abs/2310.02905" title="Use Your INSTINCT: INSTruction optimization for LLMs usIng Neural bandits Coupled with Transformers">Lin et al. (2024)</a>; <a href="https://arxiv.org/abs/2402.00396" title="Efficient Exploration for LLMs">Dwaracherla et al. (2024)</a>; <a href="https://doi.org/10.1145/3577190.3614137" title="User Feedback-based Online Learning for Intent Classification">Gönç et al. (2023)</a></td>
</tr>
<tr>
<td>Task-adapted context representation</td>
<td>Construct decision-specific representations that expose semantics relevant to routing, retrieval, rewriting, or supervision selection</td>
<td><a href="https://arxiv.org/abs/2502.18482" title="MixLLM: Dynamic Routing in Mixed Large Language Models">Wang et al. (2025)</a>; <a href="https://arxiv.org/abs/2602.20332" title="No One Size Fits All: QueryBandits for Hallucination Mitigation">Cho et al. (2026)</a>; <a href="https://doi.org/10.1145/3725812" title="Prompt-Based Code Completion via Multi-Retrieval Augmented Generation">Tan et al. (2026)</a>; <a href="https://arxiv.org/abs/2412.07618" title="Adapting to Non-Stationary Environments: Multi-Armed Bandit Enhanced Retrieval-Augmented Generation on Knowledge Graphs">Tang et al. (2025)</a>; <a href="https://arxiv.org/abs/2510.02850" title="Reward Model Routing in Alignment">Wu &amp; Lu (2026)</a></td>
</tr>
<tr>
<td>Stateful and trajectory-aware representation</td>
<td>Encode evolving dialogue histories, reasoning traces, observations, or open-world agent states for sequential decision making</td>
<td><a href="https://arxiv.org/abs/2605.15768" title="ALSO: Adversarial Online Strategy Optimization for Social Agents">Li et al. (2026)</a>; <a href="https://arxiv.org/abs/2605.11169" title="OLIVIA: Online Learning via Inference-time Action Adaptation for Decision Making in LLM ReAct Agents">Yu et al. (2026)</a>; <a href="https://arxiv.org/abs/2607.28692" title="SciToolAgent-Evo: An Ontology-Aware Self-Evolving Agent for Open-World Scientific Tool Acquisition">Tang et al. (2026)</a></td>
</tr>
<tr>
<td>Objective- and modality-aware representation</td>
<td>Augment semantic context with decision-relevant structure such as safety, resource demand, inference configuration, or multimodal information</td>
<td><a href="https://arxiv.org/abs/2605.30898" title="UniScale: Adaptive Unified Inference Scaling via Online Joint Optimization of Model Routing and Test-Time Scaling">Huang et al. (2026)</a>; <a href="https://arxiv.org/abs/2603.15647" title="Steering Frozen LLMs: Adaptive Social Alignment via Online Prompt Routing">Zhang et al. (2026)</a>; <a href="https://arxiv.org/abs/2603.06403" title="Adapter-Augmented Bandits for Online Multi-Constrained Multi-Modal Inference Scheduling">Zhang et al. (2026)</a></td>
</tr>
<tr>
<td rowspan="4"><strong>Action Modeling</strong></td>
<td>Semantic action representation</td>
<td>Embed prompts, models, demonstrations, or inference configurations so feedback can generalize across related actions</td>
<td><a href="https://arxiv.org/abs/2405.16122" title="Prompt Optimization with EASE? Efficient Ordering-aware Automated Selection of Exemplars">Wu et al. (2024)</a>; <a href="https://arxiv.org/abs/2605.14553" title="Efficient Multi-objective Prompt Optimization via Pure-exploration Bandits">Li et al. (2026)</a>; <a href="https://arxiv.org/abs/2510.00841" title="LLM Routing with Dueling Feedback">Chiang et al. (2025)</a>; <a href="https://arxiv.org/abs/2605.30898" title="UniScale: Adaptive Unified Inference Scaling via Online Joint Optimization of Model Routing and Test-Time Scaling">Huang et al. (2026)</a></td>
</tr>
<tr>
<td>Consequence-based action similarity</td>
<td>Reuse logged feedback across actions through semantic similarity among their generated outcomes</td>
<td><a href="https://arxiv.org/abs/2504.02646" title="Prompt Optimization with Logged Bandit Data">Kiyohara et al. (2025)</a>; <a href="https://doi.org/10.1145/3705328.3748088" title="An Off-Policy Learning Approach for Steering Sentence Generation towards Personalization">Kiyohara et al. (2025)</a></td>
</tr>
<tr>
<td>Relational and structured action modeling</td>
<td>Organize actions through clusters, hierarchies, graphs, or compositional structure to support statistical sharing</td>
<td><a href="https://doi.org/10.18653/v1/2026.findings-acl.171" title="SPaCe: Unlocking Sample-Efficient Large Language Models Training With Self-Pace Curriculum Learning">Do et al. (2026)</a>; <a href="https://arxiv.org/abs/2606.19750" title="Manifold Bandits: Bayesian Curriculum Learning over the Latent Geometry of Large Language Models">McKenzie et al. (2026)</a>; <a href="https://arxiv.org/abs/2603.02630" title="MASPOB: Bandit-Based Prompt Optimization for Multi-Agent Systems with Graph Neural Networks">Hong et al. (2026)</a></td>
</tr>
<tr>
<td>Dynamic action-space construction</td>
<td>Use LLMs to generate, revise, mutate, or expand candidate actions during learning</td>
<td><a href="https://arxiv.org/abs/2608.06750" title="Progressive Content Refinement with Decaying Reward Joint LinUCB">Ishikawa et al. (2026)</a>; <a href="https://arxiv.org/abs/2606.01619" title="ReSkill: Reconciling Skill Creation with Policy Optimization in Agentic RL">He et al. (2026)</a>; <a href="https://arxiv.org/abs/2602.21585" title="Duel-Evolve: Reward-Free Test-Time Scaling via LLM Self-Preferences">Karlekar et al. (2026)</a>; <a href="https://arxiv.org/abs/2605.29237" title="Evolving Skill-Structured Attack Memory Enhances LLM Jailbreaking">Zhang et al. (2026)</a></td>
</tr>
</tbody>
</table>

</details>

<details>
<summary><strong>Learning</strong> — 8 research streams · 20 papers</summary>

<br>

<table>
<thead>
<tr>
<th>Component</th>
<th>Research Stream</th>
<th>LLM Intervention</th>
<th>References</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><strong>Warm Start</strong></td>
<td>Synthetic-interaction pretraining</td>
<td>Generate pseudo-interactions or synthetic preferences to initialize reward estimates and uncertainty before substantial online feedback is available</td>
<td><a href="https://arxiv.org/abs/2406.19317" title="Jump Starting Bandits with LLM-Generated Prior Knowledge">Alamdari et al. (2024)</a>; <a href="https://arxiv.org/abs/2604.02527" title="Jump Start or False Start? A Theoretical and Empirical Evaluation of LLM-initialized Bandits">Bayley et al. (2026)</a></td>
</tr>
<tr>
<td>Prior-based initialization</td>
<td>Encode LLM-derived semantic knowledge into statistical priors that are subsequently revised through online observations</td>
<td><a href="https://doi.org/10.1145/3805712.3808498" title="LLM-Informed Bayesian Content Exploration in Ultra-Recency Recommendation">Feng et al. (2026)</a>; <a href="https://arxiv.org/abs/2608.03382" title="LLM-Derived Priors for Thompson Sampling in Cold-Start Comment Recommendation">Lee et al. (2026)</a>; <a href="https://arxiv.org/abs/2510.02850" title="Reward Model Routing in Alignment">Wu &amp; Lu (2026)</a></td>
</tr>
<tr>
<td>Guided initialization and early interaction</td>
<td>Use LLM signals to initialize action values, model parameters, or early decisions while preserving subsequent bandit exploration</td>
<td><a href="https://arxiv.org/abs/2508.13993" title="Chunks as Arms: Multi-Armed Bandit-Guided Sampling for Long-Context LLM Preference Optimization">Duan et al. (2026)</a>; <a href="https://arxiv.org/abs/2406.12125" title="Efficient Sequential Decision Making with Large Language Models">Chen et al. (2024)</a>; <a href="https://arxiv.org/abs/2605.11169" title="OLIVIA: Online Learning via Inference-time Action Adaptation for Decision Making in LLM ReAct Agents">Yu et al. (2026)</a></td>
</tr>
<tr>
<td rowspan="4"><strong>Reward Estimation</strong></td>
<td>LLM-based outcome modeling</td>
<td>Use LLMs to predict action-level rewards or reward distributions while the bandit retains control over uncertainty-aware exploration</td>
<td><a href="https://arxiv.org/abs/2404.02649" title="On the Importance of Uncertainty in Decision-Making with Large Language Models">Felicioni et al. (2024)</a>; <a href="https://arxiv.org/abs/2502.01118" title="Large Language Model-Enhanced Multi-Armed Bandits">Sun et al. (2026)</a>; <a href="https://arxiv.org/abs/2604.05859" title="When Do We Need LLMs? A Diagnostic for Language-Driven Bandits">Berdica et al. (2026)</a></td>
</tr>
<tr>
<td>Proxy augmentation and correction</td>
<td>Use LLM predictions as auxiliary or surrogate observations and correct their bias using real rewards, residuals, or selective audits</td>
<td><a href="https://arxiv.org/abs/2406.19317" title="Jump Starting Bandits with LLM-Generated Prior Knowledge">Alamdari et al. (2024)</a>; <a href="https://arxiv.org/abs/2604.14961" title="Calibration-Gated LLM Pseudo-Observations for Online Contextual Bandits">Pershin et al. (2026)</a>; <a href="https://arxiv.org/abs/2607.06879" title="Best-Arm Identification with Generative Proxy">Ma et al. (2026)</a>; <a href="https://arxiv.org/abs/2601.21471" title="Best Arm Identification with LLM Judges and Limited Human">Ao et al. (2026)</a></td>
</tr>
<tr>
<td>Language-to-reward construction</td>
<td>Translate natural-language objectives or preferences into executable reward functions and aggregate competing criteria</td>
<td><a href="https://arxiv.org/abs/2402.14807" title="A Decision-Language Model (DLM) for Dynamic Restless Multi-Armed Bandit Tasks in Public Health">Behari et al. (2024)</a>; <a href="https://arxiv.org/abs/2408.12112" title="Balancing Act: Prioritization Strategies for LLM-Designed Restless Bandit Rewards">Verma et al. (2025)</a></td>
</tr>
<tr>
<td>Semantic reward surrogates</td>
<td>Construct operational reward signals from LLM judgments, likelihoods, or pairwise preferences when direct task utility is unavailable</td>
<td><a href="https://arxiv.org/abs/2602.20332" title="No One Size Fits All: QueryBandits for Hallucination Mitigation">Cho et al. (2026)</a>; <a href="https://arxiv.org/abs/2601.12078" title="Optimizing User Profiles via Contextual Bandits for Retrieval-Augmented LLM Personalization">Du et al. (2026)</a>; <a href="https://arxiv.org/abs/2602.21585" title="Duel-Evolve: Reward-Free Test-Time Scaling via LLM Self-Preferences">Karlekar et al. (2026)</a></td>
</tr>
<tr>
<td rowspan="1"><strong>Environment Modeling</strong></td>
<td>Language-mediated posterior modeling</td>
<td>Maintain and update language-based beliefs over latent environment hypotheses for posterior sampling and sequential exploration</td>
<td><a href="https://arxiv.org/abs/2504.20997" title="Toward Efficient Exploration by Large Language Model Agents">Arumugam &amp; Griffiths (2025)</a></td>
</tr>
</tbody>
</table>

</details>

<details>
<summary><strong>Decision</strong> — 8 research streams · 13 papers</summary>

<br>

<table>
<thead>
<tr>
<th>Component</th>
<th>Research Stream</th>
<th>LLM Intervention</th>
<th>References</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="4"><strong>Exploration</strong></td>
<td>Uncertainty-aware exploration</td>
<td>Use LLM reward predictions or predictive variability within explicit optimism, posterior-sampling, or randomized exploration mechanisms</td>
<td><a href="https://arxiv.org/abs/2404.02649" title="On the Importance of Uncertainty in Decision-Making with Large Language Models">Felicioni et al. (2024)</a>; <a href="https://arxiv.org/abs/2502.01118" title="Large Language Model-Enhanced Multi-Armed Bandits">Sun et al. (2026)</a>; <a href="https://arxiv.org/abs/2604.05859" title="When Do We Need LLMs? A Diagnostic for Language-Driven Bandits">Berdica et al. (2026)</a></td>
</tr>
<tr>
<td>Semantic action-space restriction</td>
<td>Use pretrained semantic knowledge to identify a tractable candidate region before conventional statistical exploration</td>
<td><a href="https://arxiv.org/abs/2502.00225" title="Should You Use Your Large Language Model to Explore or Exploit?">Harris &amp; Slivkins (2025)</a></td>
</tr>
<tr>
<td>Direct exploration control</td>
<td>Delegate exploration schedules or history-dependent exploration policies directly to an LLM</td>
<td><a href="https://doi.org/10.3390/electronics12132814" title="LLM-Informed Multi-Armed Bandit Strategies for Non-Stationary Environments">Curtò et al. (2023)</a>; <a href="https://arxiv.org/abs/2509.24923" title="When Greedy Wins: Emergent Exploitation Bias in Meta-Bandit LLM Training">Chen et al. (2025)</a></td>
</tr>
<tr>
<td>Language-mediated model-based exploration</td>
<td>Represent uncertainty over latent environments in language and use sampled hypotheses or information gain to guide exploration</td>
<td><a href="https://arxiv.org/abs/2504.20997" title="Toward Efficient Exploration by Large Language Model Agents">Arumugam &amp; Griffiths (2025)</a></td>
</tr>
<tr>
<td rowspan="4"><strong>Action Selection</strong></td>
<td>Direct LLM action selection</td>
<td>Use interaction history and semantic reasoning to let the LLM directly select the next action or preference candidate</td>
<td><a href="https://doi.org/10.1109/COINS65080.2025.11125743" title="Evaluation of LLM Powered Agentic AI for Solving Multi-Arm Bandit Problems">Hazime &amp; Farooq (2025)</a>; <a href="https://arxiv.org/abs/2502.00225" title="Should You Use Your Large Language Model to Explore or Exploit?">Harris &amp; Slivkins (2025)</a>; <a href="https://doi.org/10.18653/v1/2025.findings-acl.519" title="Beyond Numeric Rewards: In-Context Dueling Bandits with LLM Agents">Xia et al. (2025)</a></td>
</tr>
<tr>
<td>Confidence-gated and validated selection</td>
<td>Subject LLM recommendations to statistical confidence tests, validation, or fallback procedures before execution</td>
<td><a href="https://arxiv.org/abs/2601.11905" title="LIBRA: Language Model Informed Bandit Recourse Algorithm for Personalized Treatment Planning">Cao et al. (2026)</a>; <a href="https://doi.org/10.18653/v1/2025.findings-acl.519" title="Beyond Numeric Rewards: In-Context Dueling Bandits with LLM Agents">Xia et al. (2025)</a></td>
</tr>
<tr>
<td>Candidate generation and restricted selection</td>
<td>Use the LLM to construct or update a smaller candidate set while a downstream bandit determines the executed action</td>
<td><a href="https://arxiv.org/abs/2502.00225" title="Should You Use Your Large Language Model to Explore or Exploit?">Harris &amp; Slivkins (2025)</a>; <a href="https://arxiv.org/abs/2411.01493" title="Sample-Efficient Alignment for LLMs">Liu et al. (2024)</a></td>
</tr>
<tr>
<td>Proxy- and diagnosis-guided selection</td>
<td>Use LLM-generated proxies, diagnoses, or intermediate analysis as auxiliary evidence for statistically controlled action allocation</td>
<td><a href="https://arxiv.org/abs/2607.06879" title="Best-Arm Identification with Generative Proxy">Ma et al. (2026)</a>; <a href="https://arxiv.org/abs/2605.30042" title="Learning to Choose: An Empowerment-Guided Multi-Agent System with semantic communication for Adaptive Method Selection">Suntaxi et al. (2026)</a></td>
</tr>
</tbody>
</table>

</details>

<details>
<summary><strong>Feedback</strong> — 4 research streams · 7 papers</summary>

<br>

<table>
<thead>
<tr>
<th>Component</th>
<th>Research Stream</th>
<th>LLM Intervention</th>
<th>References</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="4"><strong>Feedback Interpretation</strong></td>
<td>Scalar and binary judging</td>
<td>Convert generated or unstructured outcomes into scalar or binary observations for conventional bandit updates</td>
<td><a href="https://arxiv.org/abs/2605.14241" title="Latency-Quality Routing for Functionally Equivalent Tools in LLM Agents">Chu et al. (2026)</a>; <a href="https://www.semanticscholar.org/paper/ead828879a0379b248f224321bf4076e7c4b0434" title="Efficient Jailbreak Attack sequences on Large Language Models via Multi-Armed Bandit-based Context switching">Ramesh et al. (2025)</a></td>
</tr>
<tr>
<td>Pairwise preference interpretation</td>
<td>Convert comparative outputs into pairwise preference observations for dueling-bandit learning</td>
<td><a href="https://arxiv.org/abs/2510.13907" title="LLM Prompt Duel Optimizer: Efficient Label-Free Prompt Optimization">Wu et al. (2026)</a></td>
</tr>
<tr>
<td>Semantic feedback shaping and propagation</td>
<td>Use semantic feedback to bias future decisions or propagate observed evidence across related actions and comparisons</td>
<td><a href="https://arxiv.org/abs/2606.00846" title="CUPID in the Model Zoo: Online Matchmaking for Selecting Your Dream LLM">Nguyen et al. (2026)</a>; <a href="https://doi.org/10.1609/aaai.v40i31.39852" title="Preference Is More than Comparisons: Rethinking Dueling Bandits with Augmented Human Feedback">Wang et al. (2026)</a></td>
</tr>
<tr>
<td>Structured diagnosis and attribution</td>
<td>Interpret complex simulation or execution outcomes while preserving diagnostic information and attribution to the action that produced them</td>
<td><a href="https://arxiv.org/abs/2402.14807" title="A Decision-Language Model (DLM) for Dynamic Restless Multi-Armed Bandit Tasks in Public Health">Behari et al. (2024)</a>; <a href="https://arxiv.org/abs/2605.30042" title="Learning to Choose: An Empowerment-Guided Multi-Agent System with semantic communication for Adaptive Method Selection">Suntaxi et al. (2026)</a></td>
</tr>
</tbody>
</table>

</details>

### Detailed Paper Index

We also list every paper as a full bibliographic entry for title-based browsing. We retain the same Direction → Stage → Component → Research Stream organization and link each entry to arXiv or its official publication page.

#### Bandit-Enhanced Large Language Models

<details>
<summary><strong>Pre-training</strong> — 2 research streams · 2 papers</summary>

##### Pre-training

###### Adaptive data mixing

- Alon Albalak et al. *Efficient Online Data Mixing For Language Model Pre-Training*. arXiv, 2023. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2312.02406)

###### Pre-training configuration optimization

- Iñigo Urteaga et al. *Multi-armed bandits for resource efficient, online optimization of language model pre-training: the use case of dynamic masking*. Findings of ACL, 2023. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2203.13151)

</details>

<details>
<summary><strong>Post-training</strong> — 7 research streams · 29 papers</summary>

##### Fine-tuning

###### Adaptive curriculum and training-data scheduling

- Van Dai Do et al. *SPaCe: Unlocking Sample-Efficient Large Language Models Training With Self-Pace Curriculum Learning*. Findings of ACL, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.18653/v1/2026.findings-acl.171)
- Xiaodong Lu et al. *Contextual Rollout Bandits for Reinforcement Learning with Verifiable Rewards*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.08499)
- Darrien M. McKenzie, Nicklas Hansen, and Xiaolong Wang. *Manifold Bandits: Bayesian Curriculum Learning over the Latent Geometry of Large Language Models*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.19750)
- Haebin Shin et al. *DynamixSFT: Dynamic Mixture Optimization of Instruction Tuning Collections*. Findings of ACL, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.18653/v1/2026.findings-acl.1972)
- Zairun Yang et al. *Distribution-Value Coevolution for Adaptive RLHF Data Scheduling*. KDD, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3770855.3817990)

###### Online experience and skill control

- Kaan Gönç et al. *User Feedback-based Online Learning for Intent Classification*. ICMI, 2023. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3577190.3614137)
- Zelin He et al. *ReSkill: Reconciling Skill Creation with Policy Optimization in Agentic RL*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.01619)
- Xiao Hu et al. *Rethinking Reinforcement fine-tuning of LLMs: A Multi-armed Bandit Learning Perspective*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2601.14599)

###### Bandit-guided policy learning and co-evolution

- Sanxing Chen et al. *When Greedy Wins: Emergent Exploitation Bias in Meta-Bandit LLM Training*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2509.24923)
- Allen Nie et al. *EVOLvE: Evaluating and Optimizing LLMs For In-Context Exploration*. ICML, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2410.06238)
- Thomas Schmied et al. *LLMs are Greedy Agents: Effects of RL Fine-tuning on Decision-Making Abilities*. ICLR, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2504.16078)
- Yu Xia et al. *Which LLM to Play? Convergence-Aware Online Model Selection with Time-Increasing Bandits*. The Web Conference, 2024. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3589334.3645420)

##### Alignment

###### Active preference acquisition

- Nirjhar Das et al. *Active Preference Optimization for Sample Efficient RLHF*. ECML PKDD, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1007/978-3-032-06096-9_6)
- Vikranth Dwaracherla et al. *Efficient Exploration for LLMs*. ICML, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2402.00396)
- Kaixuan Ji, Jiafan He, and Quanquan Gu. *Reinforcement Learning from Human Feedback with Active Queries*. TMLR, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2402.09401)
- Viraj Mehta et al. *Sample Efficient Preference Alignment in LLMs via Active Exploration*. arXiv, 2023. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2312.00267)
- Antoine Scheid et al. *Optimal Design for Reward Modeling in RLHF*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2410.17055)

###### Exploration-aware preference optimization

- Chenjia Bai et al. *Online Preference Alignment for Language Models via Count-based Exploration*. ICLR, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2501.12735)
- Tengyang Xie et al. *Exploratory Preference Optimization: Harnessing Implicit Q\*-Approximation for Sample-Efficient RLHF*. ICLR, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2405.21046)
- Wei Xiong et al. *Iterative Preference Learning from Human Feedback: Bridging Theory and Practice for RLHF under KL-constraint*. ICML, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2312.11456)
- Shenao Zhang et al. *Self-Exploring Language Models: Active Preference Elicitation for Online Alignment*. TMLR, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2405.19332)

###### Policy-coupled online alignment

- Long-Fei Li et al. *Provably Efficient Online RLHF with One-Pass Reward Modeling*. NeurIPS, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.52202/085713-5567)
- Gen Li and Yuling Yan. *Towards Efficient Online Exploration for Reinforcement Learning with Human Feedback*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2509.22633)

###### Adaptive supervision and feedback control

- Shaohua Duan et al. *Chunks as Arms: Multi-Armed Bandit-Guided Sampling for Long-Context LLM Preference Optimization*. ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2508.13993)
- Mohammad Gheshlaghi Azar et al. *A General Theoretical Paradigm to Understand Learning from Human Preferences*. AISTATS, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2310.12036)
- Taesan Kim et al. *Don't Let Bandit Feedback Pull Continual LLM-Recommender Updates Off Target*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.18899)
- Allison Lau et al. *Personalized Adaptation via In-Context Preference Learning*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2410.14001)
- Zichen Liu et al. *Sample-Efficient Alignment for LLMs*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2411.01493)
- Duy Nguyen et al. *LASeR: Learning to Adaptively Select Reward Models with Multi-Arm Bandits*. NeurIPS, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2410.01735)

</details>

<details>
<summary><strong>Utilization</strong> — 23 research streams · 96 papers</summary>

##### Prompting

###### Fixed-pool prompt selection and structured sharing

- Chengshuai Shi et al. *Efficient Prompt Optimization Through the Lens of Best Arm Identification*. NeurIPS, 2024. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.52202/079017-3161)
- Xiaoqiang Lin et al. *Use Your INSTINCT: INSTruction optimization for LLMs usIng Neural bandits Coupled with Transformers*. ICML, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2310.02905)
- Zhaoxuan Wu et al. *Prompt Optimization with EASE? Efficient Ordering-aware Automated Selection of Exemplars*. NeurIPS, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2405.16122)
- Shuyang Wang, Somayeh Moazeni, and Diego Klabjan. *SOPL: A Sequential Optimal Learning Approach to Automated Prompt Engineering in Large Language Models*. Findings of ACL, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2501.03508)
- Pingchen Lu et al. *FedPOB: Sample-Efficient Federated Prompt Optimization via Bandits*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2509.24701)
- Donghao Li et al. *Efficient Multi-objective Prompt Optimization via Pure-exploration Bandits*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.14553)
- Xiaoqiang Lin et al. *Prompt Optimization with Human Feedback*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2405.17346)
- Yuanchen Wu et al. *LLM Prompt Duel Optimizer: Efficient Label-Free Prompt Optimization*. Findings of ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2510.13907)

###### Prompt generation and refinement

- Rin Ashizawa et al. *Bandit-Based Prompt Design Strategy Selection Improves Prompt Optimizers*. Findings of ACL, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.18653/v1/2025.findings-acl.1070)
- Young-Joon Park et al. *TwinBandit Prompt Optimizer: Adaptive Prompt Optimization via Synergistic Dual MAB-Guided Feedback*. CIKM, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3746252.3760824)
- Mingze Kong et al. *Meta-Prompt Optimization for LLM-Based Sequential Decision Making*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.00728)
- Zhi Hong et al. *MASPOB: Bandit-Based Prompt Optimization for Multi-Agent Systems with Graph Neural Networks*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2603.02630)

###### Contextual and deployment-time prompting

- Zekai Chen, Po-Yu Chen, and Francois Buet-Golfouse. *Online Personalizing White-box LLMs Generation with Neural Bandits*. ICAIF, 2024. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3677052.3698651)
- Nicole Cho et al. *No One Size Fits All: QueryBandits for Hallucination Mitigation*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.20332)
- Shion Ishikawa et al. *Progressive Content Refinement with Decaying Reward Joint LinUCB*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2608.06750)
- Xiang Li et al. *ALSO: Adversarial Online Strategy Optimization for Social Agents*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.15768)
- Giovanni Monea et al. *LLMs Are In-Context Bandit Reinforcement Learners*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2410.05362)
- Allen Nie et al. *EVOLvE: Evaluating and Optimizing LLMs For In-Context Exploration*. ICML, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2410.06238)
- Aditya Ramesh et al. *Efficient Jailbreak Attack sequences on Large Language Models via Multi-Armed Bandit-based Context switching*. ICLR, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://www.semanticscholar.org/paper/ead828879a0379b248f224321bf4076e7c4b0434)

###### Joint prompt and system optimization

- Jia Fu et al. *AutoRAG-HP: Automatic Online Hyper-Parameter Tuning for Retrieval-Augmented Generation*. Findings of ACL, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2406.19251)
- Yixuan Li et al. *Online Prompt Selection for Program Synthesis*. AAAI, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2501.05247)
- Saaduddin Mahmud et al. *Inference-Aware Prompt Optimization for Aligning Black-Box Large Language Models*. AAAI, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2508.10030)
- Haruka Kiyohara et al. *Prompt Optimization with Logged Bandit Data*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2504.02646)
- Haruka Kiyohara et al. *An Off-Policy Learning Approach for Steering Sentence Generation towards Personalization*. RecSys, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3705328.3748088)
- Halley Young and Nikolaj Björner. *Theory Under Construction: Orchestrating Language Models for Research Software Where the Specification Evolves*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.27209)

##### Retrieval

###### Retrieval strategy and configuration adaptation

- Xiaqiang Tang et al. *MBA-RAG: a Bandit Approach for Adaptive Retrieval-Augmented Generation through Question Complexity*. Proceedings of the 31st International Conference on Computational Linguistics, COLING 2025, Abu Dhabi, UAE, January 19-24, 2025, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2412.01572)
- Yuhang Dai, Jing Li, and Bohan Li. *Relative Performance Bandits: An Adaptive RAG Framework with Reward-Aware Exploration*. 31th IEEE International Conference on Parallel and Distributed Systems, ICPADS 2025, Hefei, China, December 14-18, 2025, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1109/ICPADS67057.2025.11322957)
- Jia Fu et al. *AutoRAG-HP: Automatic Online Hyper-Parameter Tuning for Retrieval-Augmented Generation*. Findings of ACL, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2406.19251)

###### Evidence allocation and selection

- Roxana Petcu et al. *Query Decomposition for RAG: Balancing Exploration-Exploitation*. Proceedings of the 19th Conference of the European Chapter of the Association for Computational Linguistics, EACL 2026 - Volume 1: Long Papers, Rabat, Morocco, March 24-29, 2026, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2510.18633)
- Hanzhuo Tan et al. *Prompt-Based Code Completion via Multi-Retrieval Augmented Generation*. ACM TOSEM, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3725812)
- Linfeng Du et al. *Optimizing User Profiles via Contextual Bandits for Retrieval-Augmented LLM Personalization*. ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2601.12078)

###### Retrieval computation and dynamic memory control

- Roi Pony et al. *Col-Bandit: Zero-Shot Query-Time Pruning for Late-Interaction Retrieval*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.02827)
- Junke Zhang et al. *Evolving Skill-Structured Attack Memory Enhances LLM Jailbreaking*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.29237)

##### Routing

###### Contextual model routing

- Xiaoyan Hu, Ho-fung Leung, and Farzan Farnia. *PAK-UCB Contextual Bandit: An Online Learning Approach to Prompt-Aware Selection of Generative Models and LLMs*. ICML, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2410.13287)
- Quang H. Nguyen et al. *MetaLLM: A High-performant and Cost-efficient Dynamic Framework for Wrapping LLMs*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2407.10834)
- M. Tsai and Phat Tran. *Reward-Based Online LLM Routing via NeuralUCB*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2603.30035)
- Chao-Kai Chiang, Takashi Ishida, and Masashi Sugiyama. *LLM Routing with Dueling Feedback*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2510.00841)
- Pranoy Panda et al. *Adaptive LLM Routing under Budget Constraints*. Findings of ACL, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2508.21141)
- Zhenghua Bao et al. *OrcaRouter: A Production-Oriented LLM Router with Hybrid Offline-Online Learning*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.30736)
- Ajay Narayanan Sridhar et al. *Correlation-Aware Contextual Bandits with Surrogate Rewards for LLM Routing*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2607.09015)
- Son Nguyen, Xinyuan Liu, and Ransalu Senanayake. *CUPID in the Model Zoo: Online Matchmaking for Selecting Your Dream LLM*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.00846)
- Nihir Chadderwala. *Optimizing Life Sciences Agents in Real-Time using Reinforcement Learning*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2512.03065)
- Manhin Poon et al. *Online Multi-LLM Selection via Contextual Bandits Under Unstructured Context Evolution*. AAAI, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2506.17670)
- Kexin Chu, Dawei Xiang, and Wei Zhang. *Latency-Quality Routing for Functionally Equivalent Tools in LLM Agents*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.14241)

###### Resource-aware and constrained routing

- Quang H. Nguyen et al. *MetaLLM: A High-performant and Cost-efficient Dynamic Framework for Wrapping LLMs*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2407.10834)
- Yang Li. *LLM Bandit: Cost-Efficient LLM Generation via Preference-Conditioned Dynamic Routing*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.02743)
- Wang Wei et al. *Learning to Route LLMs from Bandit Feedback: One Policy, Many Trade-offs*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2510.07429)
- Thomas Ziller et al. *GreenServ: Energy-Efficient Context-Aware Dynamic Routing for Multi-Model LLM Inference*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2601.17551)
- Xiangxiang Dai et al. *Cost-Effective Online Multi-LLM Selection with Versatile Reward Models*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2405.16587)
- Yin Huang, Qingsong Liu, and Jie Xu. *Online LLM Selection via Constrained Bandits with Time-Varying Demand*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.17489)
- Shanglin Wu, Saatvik Kher, and Padhraic Smyth. *Learning to Assign Prediction Tasks to Agents with Capacity Constraints*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.27999)
- Seoungbin Bae, Junyoung Son, and Dabeen Lee. *Learning to Route and Schedule LLMs from User Retrials via Contextual Queueing Bandits*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.02061)
- Annette Taberner-Miller. *ParetoBandit: Budget-Paced Adaptive Routing for Non-Stationary LLM Serving*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.00136)
- Ling Zu, Xiyue Peng, and Xin Liu. *BARouter: A Budget-adaptive Online Large Language Model Router Framework*. The Web Conference, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3774904.3792725)
- Xianzhi Zhang et al. *Adapter-Augmented Bandits for Online Multi-Constrained Multi-Modal Inference Scheduling*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2603.06403)
- P. Patra et al. *Truthful Reverse Auctions for Adaptive Selection via Contextual Multi-Armed Bandits*. Proc. of the 25th International Conference on Autonomous Agents and Multiagent Systems, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.65109/MBRQ7564)

###### Sequential and combinatorial routing

- Baran Atalar. *Neural Bandit Based Optimal LLM Selection for Pipeline of Tasks*. ACM SIGMETRICS Performance Evaluation Review, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2508.09958)
- Alexandre Belloni, Yan Chen, and Yehua Wei. *Online Pandora's Box for Contextual LLM Cascading*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.07392)
- Xiaoyan Hu et al. *PromptWise: Online Learning for Cost-Aware Prompt Assignment in Generative Models*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2505.18901)
- Xutong Liu et al. *Combinatorial Logistic Online Learning and Its Applications in Nonlinear Networked Systems*. IEEE Trans. Netw., 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1109/TON.2026.3663325)
- Jonathan Rau et al. *CoCoMaMa: Contextual Combinatorial Multi-Armed Bandit Router for Multi-Agent Systems with Volatile Arms*. Proceedings of the Second International Workshop on Hypermedia Multi-Agent Systems (HyperAgents 2025) co-located with 28th European Conference on Artificial Intelligence (ECAI 2025), Bologna, Italy, October 26, 2025, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://www.semanticscholar.org/paper/2a86869b09d5df9b42629881ce0861f20e4cab20)
- Jinkun Xu et al. *CES: Combinatorial Experts Selection via Contextual Linear Bandits*. KDD, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3770855.3817902)

###### Composite serving-configuration routing

- Jerry Huang et al. *Context-Aware Assistant Selection for Improved Inference Acceleration with Large Language Models*. EMNLP, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2408.08470)
- Yunlong Hou et al. *BanditSpec: Adaptive Speculative Decoding via Bandit Algorithms*. ICML, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2505.15141)
- Taehyeon Kim, Hojung Jung, and Se-Young Yun. *Multi-Drafter Speculative Decoding with Alignment Feedback*. Findings of ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.05417)
- Yixuan Li et al. *Online Prompt Selection for Program Synthesis*. AAAI, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2501.05247)
- Junxiao Ren et al. *CH-RAG: Complexity-Guided Hybrid Retrieval-Augmented for Adaptive LLM Generation*. 2026 29th International Conference on Computer Supported Cooperative Work in Design (CSCWD), 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1109/CSCWD68734.2026.11582347)
- Xiaqiang Tang et al. *Adapting to Non-Stationary Environments: Multi-Armed Bandit Enhanced Retrieval-Augmented Generation on Knowledge Graphs*. AAAI, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2412.07618)
- Kaiyu Huang et al. *UniScale: Adaptive Unified Inference Scaling via Online Joint Optimization of Model Routing and Test-Time Scaling*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.30898)
- Shaoang Li and Jian Li. *POLAR: Online Learning for LoRA Adapter Caching and Routing in Edge LLM Serving*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.16583)
- Vasanth Rao Jadav, Shalini Sudarsan, and Vikram Isanaka. *Cost-Aware LLM Orchestration via Contextual Bandit Learning*. 2026 International Conference on Artificial Intelligence, Systems, and Emerging Technologies (ICAISET), 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1109/ICAISET66439.2026.11542012)

###### Adaptive routing under system change

- Dingyang Chen, Qi Zhang, and Yinglun Zhu. *Efficient Sequential Decision Making with Large Language Models*. EMNLP, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2406.12125)
- Shaoang Li and Jian Li. *Near-Optimal Online Deployment and Routing for Streaming LLMs*. ICLR, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2506.17254)
- Xinle Wu and Yao Lu. *Reward Model Routing in Alignment*. ICLR, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2510.02850)
- Yu Xia et al. *Which LLM to Play? Convergence-Aware Online Model Selection with Time-Increasing Bandits*. The Web Conference, 2024. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3589334.3645420)
- Annette Taberner-Miller. *ParetoBandit: Budget-Paced Adaptive Routing for Non-Stationary LLM Serving*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.00136)
- Xinyuan Wang et al. *MixLLM: Dynamic Routing in Mixed Large Language Models*. NAACL, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.18482)
- Xiaqiang Tang et al. *Adapting to Non-Stationary Environments: Multi-Armed Bandit Enhanced Retrieval-Augmented Generation on Knowledge Graphs*. AAAI, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2412.07618)

##### Generation

###### Adaptive decoding and inference policies

- Yunlong Hou et al. *BanditSpec: Adaptive Speculative Decoding via Bandit Algorithms*. ICML, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2505.15141)
- Aditya Sridhar et al. *TapOut: A Bandit-Based Approach to Dynamic Speculative Decoding*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2511.02017)
- Chloe Su et al. *Learning Adaptive LLM Decoding*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2603.09065)
- Kaiyu Huang et al. *UniScale: Adaptive Unified Inference Scaling via Online Joint Optimization of Model Routing and Test-Time Scaling*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.30898)
- Saaduddin Mahmud et al. *Inference-Aware Prompt Optimization for Aligning Black-Box Large Language Models*. AAAI, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2508.10030)

###### Response- and token-level adaptive generation

- Allison Lau et al. *Personalized Adaptation via In-Context Preference Learning*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2410.14001)
- Zikun Qu et al. *T-POP: Test-Time Personalization with Online Preference Feedback*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2509.24696)
- Suho Shin et al. *Tokenized Bandit for LLM Decoding and Alignment*. ICML, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2506.07276)

###### Test-time compute and candidate allocation

- Bowen Zuo and Yinglun Zhu. *Strategic Scaling of Test-Time Compute: A Bandit Learning Approach*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2506.12721)
- Sweta Karlekar et al. *Duel-Evolve: Reward-Free Test-Time Scaling via LLM Self-Preferences*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.21585)
- Duy Nguyen et al. *LASeR: Learning to Adaptively Select Reward Models with Multi-Arm Bandits*. NeurIPS, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2410.01735)

###### Structured intermediate generation control

- Haochen Song et al. *Tailored Behavior-Change Messaging for Physical Activity: Integrating Contextual Bandits and Large Language Models*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2506.07275)
- Dezhi Ran et al. *KernelBand: Boosting LLM-based Kernel Optimization with a Hierarchical and Hardware-aware Multi-armed Bandit*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2511.18868)

##### Caching

###### Exact response-cache management

- Hantao Yang et al. *LLM Cache Bandit Revisited: Addressing Query Heterogeneity for Cost-Effective LLM Inference*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2509.15515)

###### Semantic caching

- Xutong Liu et al. *Semantic Caching for Low-Cost LLM Serving: From Offline Learning to Online Adaptation*. IEEE INFOCOM 2026 - IEEE Conference on Computer Communications, Tokyo, Japan, May 18-21, 2026, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1109/INFOCOM59046.2026.11571467)
- Baran Atalar et al. *Continuous Semantic Caching for Low-Cost LLM Serving*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.20021)

###### Model-state caching

- Shaoang Li and Jian Li. *POLAR: Online Learning for LoRA Adapter Caching and Routing in Edge LLM Serving*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.16583)

##### Agent Orchestration

###### Local agent and tool selection

- Nihir Chadderwala. *Optimizing Life Sciences Agents in Real-Time using Reinforcement Learning*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2512.03065)
- Sheldon Yu et al. *OLIVIA: Online Learning via Inference-time Action Adaptation for Decision Making in LLM ReAct Agents*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.11169)
- Yuqi Tang et al. *SciToolAgent-Evo: An Ontology-Aware Self-Evolving Agent for Open-World Scientific Tool Acquisition*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2607.28692)
- Zhaoyang Guan et al. *Symphony-Coord: Adaptive Routing for Multi-Agent LLM Systems*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.00966)
- Dian Jin et al. *Personalizing Large Language Model Agents with Small Policy Models*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2608.00215)

###### Workflow and topology control

- Mohanna Hoveyda et al. *AQA: Adaptive Question Answering in a Society of LLMs via Contextual Multi-Armed Bandit*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2409.13447)
- Huan Chen et al. *Toward an Organizational Science of Multi-Agent LLM Systems: Decoupling Who, How, and Which Algorithm*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2607.25446)
- Vasanth Rao Jadav, Shalini Sudarsan, and Vikram Isanaka. *Cost-Aware LLM Orchestration via Contextual Bandit Learning*. 2026 International Conference on Artificial Intelligence, Systems, and Emerging Technologies (ICAISET), 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1109/ICAISET66439.2026.11542012)
- Geremy Loachamín Suntaxi et al. *Learning to Choose: An Empowerment-Guided Multi-Agent System with semantic communication for Adaptive Method Selection*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.30042)
- Baran Atalar. *Neural Bandit Based Optimal LLM Selection for Pipeline of Tasks*. ACM SIGMETRICS Performance Evaluation Review, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2508.09958)
- Xiangxiang Dai et al. *Cost-Effective Online Multi-LLM Selection with Versatile Reward Models*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2405.16587)

###### Adaptive computation allocation

- Alexandre Belloni, Yan Chen, and Yehua Wei. *Online Pandora's Box for Contextual LLM Cascading*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.07392)
- Hao Tang et al. *Code Repair with LLMs gives an Exploration-Exploitation Tradeoff*. NeurIPS, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2405.17503)
- Sixue Xing et al. *Compute Allocation in Evolutionary Search: From Depth-Breadth to Multi-Armed Bandits*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.29268)

###### Trust, verification, and integrity control

- Fanzeng Xia et al. *Beyond Numeric Rewards: In-Context Dueling Bandits with LLM Agents*. Findings of ACL, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.18653/v1/2025.findings-acl.519)
- Halley Young and Nikolaj Björner. *Theory Under Construction: Orchestrating Language Models for Research Software Where the Specification Evolves*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.27209)

</details>

<details>
<summary><strong>Evaluation</strong> — 4 research streams · 11 papers</summary>

##### Adaptive Evaluation

###### Best-model identification

- Jin Peng Zhou et al. *On Speeding Up Language Model Evaluation*. ICLR, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2407.06172)
- Elad Tolochinsky, Yaniv Tenzer, and Yaniv Romano. *Valid Best-Model Identification for LLM Evaluation via Low-Rank Factorization*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.10405)
- Zifan Lyu et al. *Cutting LLM Evaluation Costs with SySRs: A Bandit Algorithm that Provably Exploits Model Similarity*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.07726)

###### Ranking and Pareto identification

- Vilém Zouhar et al. *Dynamically Allocating Evaluation Effort for Model Ranking*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2608.03437)
- Bo Xue et al. *Cost-Aware Multi-Objective Bandits: Theory and Application to Budgeted LLM Configuration Evaluation*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2608.04333)

###### Preference- and judge-based evaluation

- Sarvesh Gharat, Nikhil Karamchandani, and Jayakrishnan Nair. *Cost-Aware Best Arm Identification via Dueling Feedback with Applications to Large Language Models*. Proceedings of the 25th International Conference on Autonomous Agents and Multiagent Systems, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.65109/GEKA7634)
- Aadirupa Saha, A. Wagde, and B. Kveton. *LLM-as-Judge on a Budget*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.15481)

###### Adaptive diagnostic evaluation

- Xiangxiang Dai et al. *A Multi-Agent Conversational Bandit Approach to Online Evaluation and Selection of User-Aligned LLM Responses*. AAAI, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1609/aaai.v40i44.41064)
- Deng Pan et al. *Context Attribution with Multi-Armed Bandit Optimization*. Findings of ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2506.19977)
- Akshay Krishnamurthy et al. *Can large language models explore in-context?* NeurIPS, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2403.15371)
- Sweta Karlekar et al. *Duel-Evolve: Reward-Free Test-Time Scaling via LLM Self-Preferences*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.21585)

</details>

#### LLM-Enhanced Bandits

<details>
<summary><strong>Representation</strong> — 8 research streams · 27 papers</summary>

##### Context Representation

###### Semantic context encoding

- Ali Baheri and Cecilia O. Alm. *LLMs-augmented Contextual Bandit*. arXiv, 2023. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2311.02268)
- Xiaoqiang Lin et al. *Use Your INSTINCT: INSTruction optimization for LLMs usIng Neural bandits Coupled with Transformers*. ICML, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2310.02905)
- Vikranth Dwaracherla et al. *Efficient Exploration for LLMs*. ICML, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2402.00396)
- Kaan Gönç et al. *User Feedback-based Online Learning for Intent Classification*. ICMI, 2023. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3577190.3614137)

###### Task-adapted context representation

- Xinyuan Wang et al. *MixLLM: Dynamic Routing in Mixed Large Language Models*. NAACL, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.18482)
- Nicole Cho et al. *No One Size Fits All: QueryBandits for Hallucination Mitigation*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.20332)
- Hanzhuo Tan et al. *Prompt-Based Code Completion via Multi-Retrieval Augmented Generation*. ACM TOSEM, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3725812)
- Xiaqiang Tang et al. *Adapting to Non-Stationary Environments: Multi-Armed Bandit Enhanced Retrieval-Augmented Generation on Knowledge Graphs*. AAAI, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2412.07618)
- Xinle Wu and Yao Lu. *Reward Model Routing in Alignment*. ICLR, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2510.02850)

###### Stateful and trajectory-aware representation

- Xiang Li et al. *ALSO: Adversarial Online Strategy Optimization for Social Agents*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.15768)
- Sheldon Yu et al. *OLIVIA: Online Learning via Inference-time Action Adaptation for Decision Making in LLM ReAct Agents*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.11169)
- Yuqi Tang et al. *SciToolAgent-Evo: An Ontology-Aware Self-Evolving Agent for Open-World Scientific Tool Acquisition*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2607.28692)

###### Objective- and modality-aware representation

- Kaiyu Huang et al. *UniScale: Adaptive Unified Inference Scaling via Online Joint Optimization of Model Routing and Test-Time Scaling*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.30898)
- Zeyu Zhang et al. *Steering Frozen LLMs: Adaptive Social Alignment via Online Prompt Routing*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2603.15647)
- Xianzhi Zhang et al. *Adapter-Augmented Bandits for Online Multi-Constrained Multi-Modal Inference Scheduling*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2603.06403)

##### Action Modeling

###### Semantic action representation

- Zhaoxuan Wu et al. *Prompt Optimization with EASE? Efficient Ordering-aware Automated Selection of Exemplars*. NeurIPS, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2405.16122)
- Donghao Li et al. *Efficient Multi-objective Prompt Optimization via Pure-exploration Bandits*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.14553)
- Chao-Kai Chiang, Takashi Ishida, and Masashi Sugiyama. *LLM Routing with Dueling Feedback*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2510.00841)
- Kaiyu Huang et al. *UniScale: Adaptive Unified Inference Scaling via Online Joint Optimization of Model Routing and Test-Time Scaling*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.30898)

###### Consequence-based action similarity

- Haruka Kiyohara et al. *Prompt Optimization with Logged Bandit Data*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2504.02646)
- Haruka Kiyohara et al. *An Off-Policy Learning Approach for Steering Sentence Generation towards Personalization*. RecSys, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3705328.3748088)

###### Relational and structured action modeling

- Van Dai Do et al. *SPaCe: Unlocking Sample-Efficient Large Language Models Training With Self-Pace Curriculum Learning*. Findings of ACL, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.18653/v1/2026.findings-acl.171)
- Darrien M. McKenzie, Nicklas Hansen, and Xiaolong Wang. *Manifold Bandits: Bayesian Curriculum Learning over the Latent Geometry of Large Language Models*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.19750)
- Zhi Hong et al. *MASPOB: Bandit-Based Prompt Optimization for Multi-Agent Systems with Graph Neural Networks*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2603.02630)

###### Dynamic action-space construction

- Shion Ishikawa et al. *Progressive Content Refinement with Decaying Reward Joint LinUCB*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2608.06750)
- Zelin He et al. *ReSkill: Reconciling Skill Creation with Policy Optimization in Agentic RL*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.01619)
- Sweta Karlekar et al. *Duel-Evolve: Reward-Free Test-Time Scaling via LLM Self-Preferences*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.21585)
- Junke Zhang et al. *Evolving Skill-Structured Attack Memory Enhances LLM Jailbreaking*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.29237)

</details>

<details>
<summary><strong>Learning</strong> — 8 research streams · 20 papers</summary>

##### Warm Start

###### Synthetic-interaction pretraining

- Parand Alamdari, Yanshuai Cao, and Kevin Wilson. *Jump Starting Bandits with LLM-Generated Prior Knowledge*. EMNLP, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2406.19317)
- Adam Bayley et al. *Jump Start or False Start? A Theoretical and Empirical Evaluation of LLM-initialized Bandits*. TMLR, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.02527)

###### Prior-based initialization

- Qing Feng et al. *LLM-Informed Bayesian Content Exploration in Ultra-Recency Recommendation*. SIGIR, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1145/3805712.3808498)
- E. Lee et al. *LLM-Derived Priors for Thompson Sampling in Cold-Start Comment Recommendation*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2608.03382)
- Xinle Wu and Yao Lu. *Reward Model Routing in Alignment*. ICLR, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2510.02850)

###### Guided initialization and early interaction

- Shaohua Duan et al. *Chunks as Arms: Multi-Armed Bandit-Guided Sampling for Long-Context LLM Preference Optimization*. ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2508.13993)
- Dingyang Chen, Qi Zhang, and Yinglun Zhu. *Efficient Sequential Decision Making with Large Language Models*. EMNLP, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2406.12125)
- Sheldon Yu et al. *OLIVIA: Online Learning via Inference-time Action Adaptation for Decision Making in LLM ReAct Agents*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.11169)

##### Reward Estimation

###### LLM-based outcome modeling

- Nicolò Felicioni et al. *On the Importance of Uncertainty in Decision-Making with Large Language Models*. TMLR, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2404.02649)
- Jiahang Sun et al. *Large Language Model-Enhanced Multi-Armed Bandits*. ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.01118)
- Uljad Berdica et al. *When Do We Need LLMs? A Diagnostic for Language-Driven Bandits*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.05859)

###### Proxy augmentation and correction

- Parand Alamdari, Yanshuai Cao, and Kevin Wilson. *Jump Starting Bandits with LLM-Generated Prior Knowledge*. EMNLP, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2406.19317)
- M.N. Pershin et al. *Calibration-Gated LLM Pseudo-Observations for Online Contextual Bandits*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.14961)
- Tianyi Ma et al. *Best-Arm Identification with Generative Proxy*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2607.06879)
- Ruicheng Ao et al. *Best Arm Identification with LLM Judges and Limited Human*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2601.21471)

###### Language-to-reward construction

- Nikhil Behari et al. *A Decision-Language Model (DLM) for Dynamic Restless Multi-Armed Bandit Tasks in Public Health*. NeurIPS, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2402.14807)
- Shresth Verma et al. *Balancing Act: Prioritization Strategies for LLM-Designed Restless Bandit Rewards*. GameSec, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2408.12112)

###### Semantic reward surrogates

- Nicole Cho et al. *No One Size Fits All: QueryBandits for Hallucination Mitigation*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.20332)
- Linfeng Du et al. *Optimizing User Profiles via Contextual Bandits for Retrieval-Augmented LLM Personalization*. ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2601.12078)
- Sweta Karlekar et al. *Duel-Evolve: Reward-Free Test-Time Scaling via LLM Self-Preferences*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2602.21585)

##### Environment Modeling

###### Language-mediated posterior modeling

- Dilip Arumugam and Thomas L. Griffiths. *Toward Efficient Exploration by Large Language Model Agents*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2504.20997)

</details>

<details>
<summary><strong>Decision</strong> — 8 research streams · 13 papers</summary>

##### Exploration

###### Uncertainty-aware exploration

- Nicolò Felicioni et al. *On the Importance of Uncertainty in Decision-Making with Large Language Models*. TMLR, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2404.02649)
- Jiahang Sun et al. *Large Language Model-Enhanced Multi-Armed Bandits*. ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.01118)
- Uljad Berdica et al. *When Do We Need LLMs? A Diagnostic for Language-Driven Bandits*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2604.05859)

###### Semantic action-space restriction

- Keegan Harris and Aleksandrs Slivkins. *Should You Use Your Large Language Model to Explore or Exploit?* arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.00225)

###### Direct exploration control

- J. de Curtò et al. *LLM-Informed Multi-Armed Bandit Strategies for Non-Stationary Environments*. Electronics, 2023. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.3390/electronics12132814)
- Sanxing Chen et al. *When Greedy Wins: Emergent Exploitation Bias in Meta-Bandit LLM Training*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2509.24923)

###### Language-mediated model-based exploration

- Dilip Arumugam and Thomas L. Griffiths. *Toward Efficient Exploration by Large Language Model Agents*. arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2504.20997)

##### Action Selection

###### Direct LLM action selection

- Jawad Hazime and Junaid Farooq. *Evaluation of LLM Powered Agentic AI for Solving Multi-Arm Bandit Problems*. IEEE COINS, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1109/COINS65080.2025.11125743)
- Keegan Harris and Aleksandrs Slivkins. *Should You Use Your Large Language Model to Explore or Exploit?* arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.00225)
- Fanzeng Xia et al. *Beyond Numeric Rewards: In-Context Dueling Bandits with LLM Agents*. Findings of ACL, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.18653/v1/2025.findings-acl.519)

###### Confidence-gated and validated selection

- Junyu Cao et al. *LIBRA: Language Model Informed Bandit Recourse Algorithm for Personalized Treatment Planning*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2601.11905)
- Fanzeng Xia et al. *Beyond Numeric Rewards: In-Context Dueling Bandits with LLM Agents*. Findings of ACL, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.18653/v1/2025.findings-acl.519)

###### Candidate generation and restricted selection

- Keegan Harris and Aleksandrs Slivkins. *Should You Use Your Large Language Model to Explore or Exploit?* arXiv, 2025. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2502.00225)
- Zichen Liu et al. *Sample-Efficient Alignment for LLMs*. arXiv, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2411.01493)

###### Proxy- and diagnosis-guided selection

- Tianyi Ma et al. *Best-Arm Identification with Generative Proxy*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2607.06879)
- Geremy Loachamín Suntaxi et al. *Learning to Choose: An Empowerment-Guided Multi-Agent System with semantic communication for Adaptive Method Selection*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.30042)

</details>

<details>
<summary><strong>Feedback</strong> — 4 research streams · 7 papers</summary>

##### Feedback Interpretation

###### Scalar and binary judging

- Kexin Chu, Dawei Xiang, and Wei Zhang. *Latency-Quality Routing for Functionally Equivalent Tools in LLM Agents*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.14241)
- Aditya Ramesh et al. *Efficient Jailbreak Attack sequences on Large Language Models via Multi-Armed Bandit-based Context switching*. ICLR, 2025. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://www.semanticscholar.org/paper/ead828879a0379b248f224321bf4076e7c4b0434)

###### Pairwise preference interpretation

- Yuanchen Wu et al. *LLM Prompt Duel Optimizer: Efficient Label-Free Prompt Optimization*. Findings of ACL, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2510.13907)

###### Semantic feedback shaping and propagation

- Son Nguyen, Xinyuan Liu, and Ransalu Senanayake. *CUPID in the Model Zoo: Online Matchmaking for Selecting Your Dream LLM*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2606.00846)
- Shengbo Wang, Hong Sun, and Ke Li. *Preference Is More than Comparisons: Rethinking Dueling Bandits with Augmented Human Feedback*. AAAI, 2026. [![Paper](https://img.shields.io/badge/Paper-View-539AB9?style=flat-square)](https://doi.org/10.1609/aaai.v40i31.39852)

###### Structured diagnosis and attribution

- Nikhil Behari et al. *A Decision-Language Model (DLM) for Dynamic Restless Multi-Armed Bandit Tasks in Public Health*. NeurIPS, 2024. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2402.14807)
- Geremy Loachamín Suntaxi et al. *Learning to Choose: An Empowerment-Guided Multi-Agent System with semantic communication for Adaptive Method Selection*. arXiv, 2026. [![arXiv](https://img.shields.io/badge/arXiv-View-B31B1B?style=flat-square)](https://arxiv.org/abs/2605.30042)

</details>
<!-- END AUTO-GENERATED LITERATURE NAVIGATION -->

## 📄 Bibliography

We provide [`references.bib`](references.bib) for the bibliographic records used in our survey. We include the 153-study corpus together with supporting background and methodological references, and we identify the included corpus in [`taxonomy.yaml`](taxonomy.yaml).

## 🗂️ Repository Structure

```text
.
├── README.md                # Methodology and literature navigation
├── references.bib           # Survey and supporting references
├── taxonomy.yaml            # Reusable corpus classification
└── LICENSE
```

## 🤝 Updates / Contributing

We freeze our **Survey Corpus Snapshot** at 153 studies through August 15, 2026. We may add later work under **Post-Survey Updates**, clearly separated from our frozen snapshot.

We welcome suggestions for missing or newly published work through issues or pull requests. We ask contributors to include an authoritative citation, a short explanation of the substantive Bandit–LLM interaction, and a proposed taxonomy location. We do not include work that mentions bandits or LLMs only as background.

## 📝 Citation

If you use this collection, please cite our accompanying survey. We will add the complete publication metadata here when our paper is publicly available.
