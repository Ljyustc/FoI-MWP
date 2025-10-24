# Foundation of Intelligence: Review of Math Word Problems from Human Cognition Perspective (FoI-MWP)

> A curated survey of mathematical reasoning research from the perspective of **human cognition**.

This repository provides a structured overview of mathematical reasoning models — not from the traditional "architectural" perspective, but through the lens of **human cognitive abilities**.  
We summarize, categorize, and compare existing work based on how well they align with the core cognitive processes used in human mathematical reasoning.

---

## 🔍 Motivation

Mathematical reasoning is a cognitive process involving problem comprehension, knowledge recall, logical reasoning, and self-reflection. However, most surveys classify models by architecture (e.g., Seq2Seq vs Seq2Tree), lacking a **human-centered cognitive viewpoint**.

This survey reframes mathematical reasoning research by mapping model designs and reasoning techniques to **five key cognitive abilities**, making the field more interpretable and pedagogically aligned with human learning.

---

## 🧠 Cognitive Framework of Mathematical Reasoning

We identify **five core cognitive abilities** essential for mathematical reasoning:

| Cognitive Ability | Description | Examples in Human Behavior |
|-------------------|-------------|-----------------------------|
| 🧭 **Problem Understanding** | Comprehend the problem, extract key information, formalize the goal | Reading, abstraction, problem reformulation |
| 🧩 **Logical Organization** | Structure reasoning steps coherently and logically | Step-by-step proofs, structured solution plans |
| 🔗 **Associative Memory** | Retrieve relevant experiences to solve problems | Recall formulas, known patterns, similar questions |
| 🧐 **Critical Thinking** | Self-reflection, self-correction, verification, counterfactual reasoning | Check mistakes, refine solutions, compare approaches |
| 📚 **Knowledge Learning** | Learn, store, and apply explicit domain knowledge (math rules, formulas) | Study, memorize, apply new theorems |

---

## 🏗️ Model Categorization

We categorize mathematical reasoning models into two major families:

---

### ✅ 1. **(Small) Neural Network Solvers**

These models solve math problems directly via neural architectures without large-scale language pretraining. They imitate specific cognitive abilities and generate mathematical expressions as solutions.

#### 📍 Representative Papers

| Cognitive Ability Focused | Representative Work |
|----------------------------|----------------------|
| Problem Understanding | [DNS](https://aclanthology.org/D17-1088/), [T-RNN](https://ojs.aaai.org/index.php/AAAI/article/view/4697), [Graph2Tree](https://aclanthology.org/2020.acl-main.362/), [Graph2Tree+](https://ieeexplore.ieee.org/document/9721720), [GROUPATT](https://aclanthology.org/P19-1619/), [NS-Solver](https://aclanthology.org/2021.acl-long.456.pdf), [HMS](https://ojs.aaai.org/index.php/AAAI/article/view/16547), [KA-S2T](https://aclanthology.org/2020.emnlp-main.579/), [LogicSolver](https://aclanthology.org/2022.findings-emnlp.1.pdf), [NumS2T](https://aclanthology.org/2021.acl-long.455/), [HGEN](https://ieeexplore.ieee.org/document/9693212), [Multi-E/D](https://aclanthology.org/2020.coling-main.262/), [EEH-G2T](https://aclanthology.org/2021.findings-emnlp.127/), [RPKHS](https://aclanthology.org/2021.emnlp-main.272/), [MWP-BERT](https://aclanthology.org/2022.findings-naacl.74/), [TCDP](https://ieeexplore.ieee.org/document/10113691) |
| Logical Organization | [GTS](https://www.ijcai.org/proceedings/2019/0736.pdf), [Seq2DAG](https://ojs.aaai.org/index.php/AAAI/article/view/16075), [CASS](https://aclanthology.org/C18-1018/), [FOMAS](https://dl.acm.org/doi/10.1145/3580305.3599375), [SUMC-Solver](https://aclanthology.org/2022.emnlp-main.556/), [TSN-MD](https://www.ijcai.org/proceedings/2020/0555.pdf), [DEDUCTREASONER](https://aclanthology.org/2022.acl-long.410/), [Multi-view](https://aclanthology.org/2022.findings-emnlp.79.pdf), [Multi-E/D](https://aclanthology.org/2020.coling-main.262/), [MathDQN](https://ojs.aaai.org/index.php/AAAI/article/view/11981) |
| Associative Memory | [REAL](https://aclanthology.org/2021.findings-emnlp.68/), [RHMS](https://ieeexplore.ieee.org/document/10136830) |
| Critical Thinking | [Generate&Rank](https://aclanthology.org/2021.findings-emnlp.195/), [WDA](https://dl.acm.org/doi/10.1609/aaai.v37i11.26548), [DQGF](https://aclanthology.org/2023.findings-acl.705/) |
| Knowledge Learning | [CogSolver](https://ieeexplore.ieee.org/document/10027795), [LeAp](https://dl.acm.org/doi/10.1609/aaai.v37i4.25571) |

---

### ✅ 2. **LLM-based Solvers**

LLM-based solvers utilize language models to perform and explain reasoning. They solve MWPs by generating a rational, within which they unify multiple human cognitive abilities.

#### 📍 Representative Papers

| Cognitive Ability Focused | Representative Work |
|-------------------|-------------------|
| Logical Organization | [Chain-of-Thought (CoT)](https://dl.acm.org/doi/10.5555/3600270.3602070), [Tree-of-Thought (ToT)](https://dl.acm.org/doi/abs/10.5555/3666122.3666639), [Graph-of-Thought (GoT)](https://dl.acm.org/doi/10.1609/aaai.v38i16.29720), [Least-to-Most](https://arxiv.org/abs/2205.10625), [DeAR](https://dl.acm.org/doi/10.5555/3737916.3737928), [Planning-LM](https://aclanthology.org/2023.acl-long.379.pdf) |
| Associative Memory | [TopK+ConE](https://aclanthology.org/2024.acl-long.492/), [TopK+MDL](https://virtual2023.aclweb.org/paper_P1627.html), [InfICL](https://arxiv.org/abs/2402.11750), [MI-ICL](https://aclanthology.org/2022.acl-long.60/?trk=public_post_comment-text), [SPELL](https://aclanthology.org/2023.findings-emnlp.679.pdf), [IDS](https://aclanthology.org/2024.findings-emnlp.438.pdf), [LMS3](https://icml.cc/virtual/2025/poster/43714) |
| Critical Thinking | [Self-Consistency](https://arxiv.org/abs/2203.11171), [Self-Verification](https://aclanthology.org/2023.findings-emnlp.167.pdf), [Self-Reflection](https://arxiv.org/pdf/2405.06682), [CRITIC](https://arxiv.org/abs/2305.11738), [CoRe](https://aclanthology.org/2023.acl-long.245.pdf), [CEMAL](https://aclanthology.org/2023.emnlp-main.889/), [WizardMath](https://arxiv.org/abs/2308.09583), [Xwin-Math](https://arxiv.org/abs/2405.20335), [MetaMath](https://arxiv.org/abs/2309.12284) |
| Tool Integration | [Program-of-Thought](https://arxiv.org/abs/2211.12588), [PAL](https://dl.acm.org/doi/10.5555/3618408.3618843), [CREATOR](https://aclanthology.org/2023.findings-emnlp.462.pdf), [CRAFT](https://arxiv.org/abs/2309.17428), [TROVE](https://dl.acm.org/doi/10.5555/3692070.3694168), [KTCE](https://ojs.aaai.org/index.php/AAAI/article/view/34664), [Tool-MVR](https://dl.acm.org/doi/10.1145/3711896.3736835) |

---

### 📊 Performances of NN-based Methods on MWP datasets

| Cognitive Ability | Method | Math23K | MAWPS | SVAMP | MathQA |
|------------------|--------|---------|-------|-------|--------|
| **Problem Understanding** | DNS | 58.1 | 59.2 | 20.0 | / |
|  | HMS | 76.1 | 80.3 | 17.9 | / |
|  | Graph2Tree | 77.4 | 83.7 | 31.9 | 69.5 |
|  | KA-S2T | 76.3 | / | / | / |
|  | MWP-BERT | 84.7 | 82.9 | / | 76.2 |
|  | BERT-Tree | 83.3 | 87.2 | 32.4 | 73.8 |
| **Logical Organization** | GTS | 74.3 | 82.6 | 27.7 | / |
|  | FOMAS | 84.8 | 88.6 | / | / |
|  | DEDUCTREASONER | 85.1 | 92.0 | 47.3 | 78.6 |
| **Associative Memory** | RHMS | 78.6 | 84.9 | / | / |
|  | REAL | 82.3 | / | / | / |
| **Critical Thinking** | Generate&Rank | 85.4 | 84.0 | / | / |
| **Knowledge Learning** | CogSolver | 77.3 | 82.9 | / | / |
|  | LeAp | 77.9 | 85.2 | 34.1 | / |


### 📊 Performances of LLM-based Methods on MWP datasets

| Cognitive Ability | Method | Backbone | Math23K | MAWPS | SVAMP | MathQA | GSM8K |
|------------------|--------|---------|---------|-------|-------|--------|-------|
| **Logical Organization** | CoT | GPT-3.5 | 85.8 | 91.9 | 88.4 | 79.8 | 87.2 |
|   |   | LLaMA3.1-8B | 83.4 | 92.7 | 88.9 | 80.2 | 87.4 |
|   | ToT | GPT-3.5 | 86.5 | 92.5 | 89.7 | 80.8 | 88.8 |
|   |   | LLaMA3.1-8B | 84.9 | 93.2 | 90.0 | 81.0 | 89.2 |
|   | GoT | GPT-3.5 | 86.0 | 93.0 | 90.1 | 80.6 | 87.9 |
|   |   | LLaMA3.1-8B | 84.4 | 93.9 | 90.8 | 81.0 | 88.5 |
| **Associative Memory** | ICL | GPT-3.5 | 85.9 | 92.8 | 89.9 | 81.1 | 90.8 |
|   |   | LLaMA3.1-8B | 83.7 | 93.3 | 91.0 | 81.5 | 91.3 |
| **Critical Thinking** | Self-Consistency | GPT-3.5 | 87.0 | 93.1 | 91.7 | 81.4 | 90.5 |
|   |   | LLaMA3.1-8B | 84.1 | 94.5 | 91.9 | 81.7 | 91.2 |
|   | Self-Verification | GPT-3.5 | 86.8 | 94.4 | 90.6 | 82.5 | 91.6 |
|   |   | LLaMA3.1-8B | 84.6 | 93.8 | 92.1 | 82.0 | 90.9 |
| **Tool Integration** | PoT | GPT-3.5 | 88.3 | 95.0 | 93.8 | 84.7 | 92.8 |
|   |   | LLaMA3.1-8B | 85.8 | 95.8 | 93.5 | 85.5 | 92.5 |
|   | PAL | GPT-3.5 | 87.7 | 95.3 | 92.5 | 83.1 | 93.0 |
|   |   | LLaMA3.1-8B | 86.1 | 96.0 | 93.7 | 82.4 | 93.4 |
| **Math LLMs** | WizardMath | LLaMA2-7B | 75.2 | 79.5 | 63.2 | 73.5 | 75.1 |
|   |   | LLaMA2-70B | 85.8 | 88.6 | 76.4 | 80.1 | 83.8 |
|   | MetaMath | LLaMA2-7B | 74.4 | 82.4 | 75.8 | 77.6 | 79.2 |
|   |   | LLaMA2-70B | 84.5 | 89.3 | 80.6 | 81.0 | 85.3 |