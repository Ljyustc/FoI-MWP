# 🧠 Foundation of Intelligence: Review of Math Word Problems from Human Cognition Perspective (FoI-MWP)

> A curated survey of mathematical reasoning research from the perspective of **human cognition**.

This repository provides a structured overview of mathematical reasoning models — not from the traditional "architectural" perspective, but through the lens of **human cognitive abilities**.  
We summarize, categorize, and compare existing work based on how well they align with the core cognitive processes used in human mathematical reasoning.

---

## 🔍 Motivation

Mathematical reasoning is a cognitive process involving problem comprehension, knowledge recall, logical reasoning, and self-reflection.  
However, most surveys classify models by architecture (e.g., Seq2Seq vs LLMs), lacking a **human-centered cognitive viewpoint**.

This survey reframes mathematical reasoning research by mapping model designs and reasoning techniques to **five key cognitive abilities**, making the field more interpretable and pedagogically aligned with human learning.

---

## 🧩 Cognitive Framework of Mathematical Reasoning

We identify **five core cognitive abilities** essential for mathematical reasoning:

| Cognitive Ability | Description | Examples in Human Behavior |
|-------------------|-------------|-----------------------------|
| 🧠 **Problem Understanding** | Comprehend the problem, extract key information, formalize the goal | Reading, abstraction, problem reformulation |
| 🧩 **Logical Organization** | Structure reasoning steps coherently and logically | Step-by-step proofs, structured solution plans |
| 🔗 **Associative Memory** | Retrieve relevant experiences to solve problems | Recall formulas, known patterns, similar questions |
| 🧐 **Critical Thinking** | Self-reflection, self-correction, verification, counterfactual reasoning | Check mistakes, refine solutions, compare approaches |
| 📚 **Knowledge Learning** | Learn, store, and apply explicit domain knowledge (math rules, formulas) | Study, memorize, apply new theorems |

---

## 🏗️ Model Categorization

We categorize mathematical reasoning models into two major families:

---

### ✅ 1. **(Small) Neural Network Solvers**

These models solve math problems directly via neural architectures without large-scale language pretraining.

We evaluate them along the five cognitive dimensions above.

#### 📍 Representative Papers

| Cognitive Ability Focused | Representative Work |
|----------------------------|----------------------|
| Problem Understanding | NSM (Neural Symbolic Machines), MathBERT, TaLM |
| Logical Organization | Graph2Tree, TreeRNN, NS-Solver |
| Associative Memory | Memory-Augmented Neural Networks (MANN), Neural Turing Machines |
| Critical Thinking | ReCheck, Self-Verify NN solvers |
| Knowledge Learning | DeepMath, Transformers+formal math knowledge, Math-Knowledge Pretraining |

> These works typically learn reasoning patterns implicitly through supervision or structured neural architectures.

---

### 🧠 2. **LLM-based Mathematical Reasoning**

LLM-based models utilize pretrained language models to perform and explain reasoning.

We divide them into **General** and **Specialized** directions:

---

#### 2.1 🌍 **General LLM-based Reasoning Methods**

This branch enhances **inference-time reasoning** of LLMs by stimulating cognitive abilities.

| Cognitive Ability | Method Category | Representative Paper / Method |
|-------------------|-------------------|--------------------------------|
| Logical Organization | Chain-of-Thought (CoT), Tree-of-Thought (ToT) | CoT, ToT, Graph-of-Thought |
| Associative Memory | Retrieval-based CoT, In-context Learning (ICL) | RICL, ReACT, RAG for Math |
| Critical Thinking | Self-Consistency, Self-Refinement, Debate Models | SC, Reflexion, Socratic CoT |
| Tool Integration | Program-of-Thought, Toolformer, Calculator/Code Integration | PoT, Toolformer, PAL, Math-Toolformer |

> These methods improve reasoning **without retraining LLMs**, simulating human thinking strategies.

---

#### 2.2 🎯 **Specialized LLM-based Reasoning Methods**

These models are explicitly designed for mathematical reasoning.

| Category | Description | Representative Work |
|----------|--------------|----------------------|
| Math-Finetuned LLMs | LLMs specifically trained/tuned for mathematics | Minerva, MathGLM, Qwen-Math |
| Knowledge-Enhanced Math LLMs | Inject explicit math knowledge (symbolic, formulaic, or theorem-based) | MathCoder, MathReason, Logic-LM |
| Cognitive-Guided Math LLMs | Architectures inspired by human cognition | MAmmoTH, MetaMath, Think-in-Think |
| Multi-Agent LLM Reasoning | Collaborative agents with teacher–student or debate roles | MathAgents, Debate LLMs, Socratic Agents |

---

## 📂 Repository Structure

