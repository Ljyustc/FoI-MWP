# Foundation of Intelligence: Review of Math Word Problems from Human Cognition Perspective (FoI-MWP)

> A curated survey of mathematical reasoning research from the perspective of **human cognition**.

This repository provides a structured overview of mathematical reasoning models — not from the traditional "architectural" perspective, but through the lens of **human cognitive abilities**.  
We summarize, categorize, and compare existing work based on how well they align with the core cognitive processes used in human mathematical reasoning.

---

## 🔍 Motivation

Mathematical reasoning is a cognitive process involving problem comprehension, knowledge recall, logical reasoning, and self-reflection. However, most surveys classify models by architecture (e.g., Seq2Seq vs LLMs), lacking a **human-centered cognitive viewpoint**.

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
| Problem Understanding | DNS, T-RNN, Graph2Tree, Graph2Tree+, GROUPATT, NS-Solver, HMS, KA-S2T, LogicSolver, NumS2T, HGEN, Multi-E/D, EEH-G2T, RPKH, MWP-BERT, TCDP |
| Logical Organization | GTS, Seq2DAG, CASS, FOMAS, SUMC-Solver, TSN-MD, DEDUCTREASONER, Multi-view, MathDQN |
| Associative Memory | REAL, RHMS |
| Critical Thinking | Generate&Rank, WDA, DQGF |
| Knowledge Learning | CogSolver, LeAp |

---

### ✅ 2. **LLM-based Solvers**

LLM-based solvers utilize language models to perform and explain reasoning. They solve MWPs by generating a rational, within which they unify multiple human cognitive abilities.

#### 📍 Representative Papers

| Cognitive Ability Focused | Representative Work |
|-------------------|-------------------|
| Logical Organization | Chain-of-Thought (CoT), Tree-of-Thought (ToT), Graph-of-Thought (GoT), Least-to-Most, DeAR, Planning-LM |
| Associative Memory | Similar-ICL, InfICL, IDS, SPELL, LMS3, RaFe, Retreival-augmented Generation |
| Critical Thinking | Self-Consistency, Self-Verification, Self-Reflection, CRITIC, CoRe, CEMAL, WizardMath, Xwin-Math, MetaMath |
| Tool Integration | Program-of-Thought, ToolLlama, PAL, CREATOR, CRAFT, TROVE, KTCE |

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

<table>
  <thead>
    <tr>
      <th>Cognitive Ability</th>
      <th>Method</th>
      <th>Backbone</th>
      <th>Math23K</th>
      <th>MAWPS</th>
      <th>SVAMP</th>
      <th>MathQA</th>
      <th>GSM8K</th>
    </tr>
  </thead>
  <tbody>
    <!-- Logical Organization -->
    <tr>
      <td rowspan="6"><strong>Logical Organization</strong></td>
      <td rowspan="2">CoT</td>
      <td>GPT-3.5</td><td>85.8</td><td>91.9</td><td>88.4</td><td>79.8</td><td>87.2</td>
    </tr>
    <tr>
      <td>LLaMA3.1-8B</td><td>83.4</td><td>92.7</td><td>88.9</td><td>80.2</td><td>87.4</td>
    </tr>
    <tr>
      <td rowspan="2">ToT</td>
      <td>GPT-3.5</td><td>86.5</td><td>92.5</td><td>89.7</td><td>80.8</td><td>88.8</td>
    </tr>
    <tr>
      <td>LLaMA3.1-8B</td><td>84.9</td><td>93.2</td><td>90.0</td><td>81.0</td><td>89.2</td>
    </tr>
    <tr>
      <td rowspan="2">GoT</td>
      <td>GPT-3.5</td><td>86.0</td><td>93.0</td><td>90.1</td><td>80.6</td><td>87.9</td>
    </tr>
    <tr>
      <td>LLaMA3.1-8B</td><td>84.4</td><td>93.9</td><td>90.8</td><td>81.0</td><td>88.5</td>
    </tr>

    <!-- Associative Memory -->
    <tr>
      <td rowspan="2"><strong>Associative Memory</strong></td>
      <td rowspan="2">ICL</td>
      <td>GPT-3.5</td><td>85.9</td><td>92.8</td><td>89.9</td><td>81.1</td><td>90.8</td>
    </tr>
    <tr>
      <td>LLaMA3.1-8B</td><td>83.7</td><td>93.3</td><td>91.0</td><td>81.5</td><td>91.3</td>
    </tr>

    <!-- Critical Thinking -->
    <tr>
      <td rowspan="4"><strong>Critical Thinking</strong></td>
      <td rowspan="2">Self-Consistency</td>
      <td>GPT-3.5</td><td>87.0</td><td>93.1</td><td>91.7</td><td>81.4</td><td>90.5</td>
    </tr>
    <tr>
      <td>LLaMA3.1-8B</td><td>84.1</td><td>94.5</td><td>91.9</td><td>81.7</td><td>91.2</td>
    </tr>
    <tr>
      <td rowspan="2">Self-Verification</td>
      <td>GPT-3.5</td><td>86.8</td><td>94.4</td><td>90.6</td><td>82.5</td><td>91.6</td>
    </tr>
    <tr>
      <td>LLaMA3.1-8B</td><td>84.6</td><td>93.8</td><td>92.1</td><td>82.0</td><td>90.9</td>
    </tr>

    <!-- Tool Integration -->
    <tr>
      <td rowspan="4"><strong>Tool Integration</strong></td>
      <td rowspan="2">PoT</td>
      <td>GPT-3.5</td><td>88.3</td><td>95.0</td><td>93.8</td><td>84.7</td><td>92.8</td>
    </tr>
    <tr>
      <td>LLaMA3.1-8B</td><td>85.8</td><td>95.8</td><td>93.5</td><td>85.5</td><td>92.5</td>
    </tr>
    <tr>
      <td rowspan="2">PAL</td>
      <td>GPT-3.5</td><td>87.7</td><td>95.3</td><td>92.5</td><td>83.1</td><td>93.0</td>
    </tr>
    <tr>
      <td>LLaMA3.1-8B</td><td>86.1</td><td>96.0</td><td>93.7</td><td>82.4</td><td>93.4</td>
    </tr>

    <!-- Math LLMs -->
    <tr>
      <td rowspan="4"><strong>Math LLMs</strong></td>
      <td rowspan="2">WizardMath</td>
      <td>LLaMA2-7B</td><td>75.2</td><td>79.5</td><td>63.2</td><td>73.5</td><td>75.1</td>
    </tr>
    <tr>
      <td>LLaMA2-70B</td><td>85.8</td><td>88.6</td><td>76.4</td><td>80.1</td><td>83.8</td>
    </tr>
    <tr>
      <td rowspan="2">MetaMath</td>
      <td>LLaMA2-7B</td><td>74.4</td><td>82.4</td><td>75.8</td><td>77.6</td><td>79.2</td>
    </tr>
    <tr>
      <td>LLaMA2-70B</td><td>84.5</td><td>89.3</td><td>80.6</td><td>81.0</td><td>85.3</td>
    </tr>
  </tbody>
</table>
