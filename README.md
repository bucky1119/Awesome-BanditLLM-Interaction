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

A study may appear in multiple research streams when it contains multiple substantive intervention mechanisms. The machine-readable taxonomy contains 153 unique studies and 230 assignments. The manuscript synthesis tables below preserve the paper's more compact presentation: they retain all 153 studies across 63 research streams while consolidating five closely related utilization placements, resulting in 225 linked reference placements.

<!-- BEGIN AUTO-GENERATED LITERATURE NAVIGATION -->
Browse the component-level synthesis below. Each stage expands into the same four-column structure used in the survey: Component, Research Stream, intervention mechanism, and References. Reference labels link directly to a verified arXiv record or, when no arXiv identifier is available, the official publication page.

### Bandit-Enhanced Large Language Models

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
<summary><strong>Post-training</strong> — 6 research streams · 29 papers</summary>

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
<td>Data and curriculum scheduling</td>
<td>Schedule samples, datasets, tasks, curricula, or rollouts</td>
<td><a href="https://doi.org/10.18653/v1/2026.findings-acl.171" title="SPaCe: Unlocking Sample-Efficient Large Language Models Training With Self-Pace Curriculum Learning">Do et al. (2026)</a>; <a href="https://arxiv.org/abs/2602.08499" title="Contextual Rollout Bandits for Reinforcement Learning with Verifiable Rewards">Lu et al. (2026)</a>; <a href="https://arxiv.org/abs/2606.19750" title="Manifold Bandits: Bayesian Curriculum Learning over the Latent Geometry of Large Language Models">McKenzie et al. (2026)</a>; <a href="https://doi.org/10.18653/v1/2026.findings-acl.1972" title="DynamixSFT: Dynamic Mixture Optimization of Instruction Tuning Collections">Shin et al. (2026)</a>; <a href="https://doi.org/10.1145/3770855.3817990" title="Distribution-Value Coevolution for Adaptive RLHF Data Scheduling">Yang et al. (2026)</a></td>
</tr>
<tr>
<td>Bandit-informed policy training</td>
<td>Shape policy learning from partial-feedback signals</td>
<td><a href="https://arxiv.org/abs/2509.24923" title="When Greedy Wins: Emergent Exploitation Bias in Meta-Bandit LLM Training">Chen et al. (2025)</a>; <a href="https://arxiv.org/abs/2601.14599" title="Rethinking Reinforcement fine-tuning of LLMs: A Multi-armed Bandit Learning Perspective">Hu et al. (2026)</a>; <a href="https://arxiv.org/abs/2410.06238" title="EVOLvE: Evaluating and Optimizing LLMs For In-Context Exploration">Nie et al. (2025)</a>; <a href="https://arxiv.org/abs/2504.16078" title="LLMs are Greedy Agents: Effects of RL Fine-tuning on Decision-Making Abilities">Schmied et al. (2026)</a></td>
</tr>
<tr>
<td>Online adaptation and co-evolving targets</td>
<td>Adapt models or skills with evolving online utilities</td>
<td><a href="https://doi.org/10.1145/3577190.3614137" title="User Feedback-based Online Learning for Intent Classification">Gönç et al. (2023)</a>; <a href="https://arxiv.org/abs/2606.01619" title="ReSkill: Reconciling Skill Creation with Policy Optimization in Agentic RL">He et al. (2026)</a>; <a href="https://doi.org/10.1145/3589334.3645420" title="Which LLM to Play? Convergence-Aware Online Model Selection with Time-Increasing Bandits">Xia et al. (2024)</a></td>
</tr>
<tr>
<td rowspan="3"><strong>Alignment</strong></td>
<td>Active preference acquisition</td>
<td>Query informative comparisons or preference feedback</td>
<td><a href="https://doi.org/10.1007/978-3-032-06096-9_6" title="Active Preference Optimization for Sample Efficient RLHF">Das et al. (2025)</a>; <a href="https://arxiv.org/abs/2402.00396" title="Efficient Exploration for LLMs">Dwaracherla et al. (2024)</a>; <a href="https://arxiv.org/abs/2402.09401" title="Reinforcement Learning from Human Feedback with Active Queries">Ji et al. (2025)</a>; <a href="https://arxiv.org/abs/2411.01493" title="Sample-Efficient Alignment for LLMs">Liu et al. (2024)</a>; <a href="https://arxiv.org/abs/2312.00267" title="Sample Efficient Preference Alignment in LLMs via Active Exploration">Mehta et al. (2023)</a>; <a href="https://arxiv.org/abs/2410.17055" title="Optimal Design for Reward Modeling in RLHF">Scheid et al. (2024)</a></td>
</tr>
<tr>
<td>Exploration-aware preference optimization</td>
<td>Explore uncertain preferences during alignment</td>
<td><a href="https://arxiv.org/abs/2501.12735" title="Online Preference Alignment for Language Models via Count-based Exploration">Bai et al. (2025)</a>; <a href="https://doi.org/10.52202/085713-5567" title="Provably Efficient Online RLHF with One-Pass Reward Modeling">Li et al. (2025)</a>; <a href="https://arxiv.org/abs/2509.22633" title="Towards Efficient Online Exploration for Reinforcement Learning with Human Feedback">Li &amp; Yan (2025)</a>; <a href="https://arxiv.org/abs/2405.21046" title="Exploratory Preference Optimization: Harnessing Implicit Q*-Approximation for Sample-Efficient RLHF">Xie et al. (2025)</a>; <a href="https://arxiv.org/abs/2312.11456" title="Iterative Preference Learning from Human Feedback: Bridging Theory and Practice for RLHF under KL-constraint">Xiong et al. (2024)</a>; <a href="https://arxiv.org/abs/2405.19332" title="Self-Exploring Language Models: Active Preference Elicitation for Online Alignment">Zhang et al. (2025)</a></td>
</tr>
<tr>
<td>Preference and supervision control</td>
<td>Adapt preference objectives, rewards, or supervision</td>
<td><a href="https://arxiv.org/abs/2310.12036" title="A General Theoretical Paradigm to Understand Learning from Human Preferences">Azar et al. (2024)</a>; <a href="https://arxiv.org/abs/2508.13993" title="Chunks as Arms: Multi-Armed Bandit-Guided Sampling for Long-Context LLM Preference Optimization">Duan et al. (2026)</a>; <a href="https://arxiv.org/abs/2605.18899" title="Don&#x27;t Let Bandit Feedback Pull Continual LLM-Recommender Updates Off Target">Kim et al. (2026)</a>; <a href="https://arxiv.org/abs/2410.14001" title="Personalized Adaptation via In-Context Preference Learning">Lau et al. (2024)</a>; <a href="https://arxiv.org/abs/2410.01735" title="LASeR: Learning to Adaptively Select Reward Models with Multi-Arm Bandits">Nguyen et al. (2025)</a></td>
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


### LLM-Enhanced Bandits

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
