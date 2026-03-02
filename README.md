# 🔬 Comparative Evaluation of AI Scientific Literature Retrieval Tools
### *Benchmarking DOI-Level Recall Across Modern Research Assistants*
**Date:** 1 March 2026

---
## 🌍 Overview
This repository presents a structured, controlled comparison of leading AI-powered scientific literature search and research assistance tools.

The central question:

> How effectively can modern AI systems retrieve *foundational (key) cited papers* when queried using natural research-style questions derived from peer-reviewed literature?

Unlike many evaluations that assess explanation quality or summarization fluency, this study focuses strictly on:

🎯 **Retrieval precision**
🎯 **Foundational paper recall**
🎯 **DOI-level matching accuracy**

---

## 🧠 Tools Evaluated
### 🔎 Literature Retrieval Platforms

* **Google Labs (AI Search / Experimental Search)**
* **Allen Institute for AI Paper Finder**
* **Undermind**

### 🤖 Generative AI Systems
* **OpenAI ChatGPT**
* **Google Deep Research Gemini**

The distinction between retrieval systems and generative systems is central to interpreting results.

---

# 🔍 Retrieval Tools vs 🤖 Generative Summarizers

## 1️⃣ Literature Search / Retrieval Tools

**Purpose:**
Return relevant academic papers from indexed databases.

**Core Capabilities:**
* Indexed search over scientific repositories
* Ranking by relevance
* DOI-level output
* Citation network awareness (varies by platform)

**Evaluation Criteria:**
* Are expected foundational DOIs retrieved?
* Are highly cited works prioritized?
* Is retrieval robust beyond keyword matching?
* Is irrelevant literature minimized?

These tools are designed for **recall and precision**, not explanation quality.

---
## 2️⃣ Summarization / Generative AI Tools
**Purpose:**
Synthesize, summarize, or explain scientific knowledge.

**Core Capabilities:**
* Structured narrative answers
* Concept explanation
* Literature synthesis
* Contextual reasoning

**Limitations:**
* Difficult to know quality. 
* May hallucinate citations
* May retrieve semantically related but incorrect papers
* Often optimized for fluency over DOI-level recall

This does not test the summarization element and only look at the easily verifiable retrieval 
---

# 🧪 Experimental Design
## 🔁 Reverse-Citation Retrieval Framework
To rigorously evaluate retrieval quality, a controlled reverse-testing methodology was used.

---
### 📌 Step 1 — Select a Published Peer-Reviewed Paper
A paragraph was extracted from a published article containing:
* Explicit in-text citations
* Foundational or key studies
* Regional and policy-relevant references
* Multiple high-impact journals
The cited works became the **Expected DOI Set**.
---

### 📌 Step 2 — Construct a Reverse Query
Using ChatGPT, the paragraph was converted into a natural research-style question.
**Important controls:**
* ❌ No DOIs included in the query
* ❌ No direct citation phrasing copied
* ✅ Query written as a realistic research question

Goal:
> If retrieval is functioning correctly, some of the cited foundational papers should reappear in results.

---
### 📌 Step 3 — Standardized Evaluation
Each tool was tested using the *same query*.
For each system we recorded:
* Retrieved DOIs
* Overlap with Expected Set
* Additional relevant literature
* Missed foundational works

---

# 📊 Evaluation Summary
## 📅 1 March 2026
## 🧾 Total Queries Tested: 2

<p align="center">
  <img src="output (8).png" width="800">
</p>

---

# 🔬 Observed Patterns

## 🥇 Google Labs
* Consistently highest DOI-level recall
* Strong overlap with expected foundational (key) papers
* Likely benefits from:

  * Large-scale crawling infrastructure
  * Deep indexing of publisher ecosystems (Nature, PNAS, Elsevier, Springer)
  * Structured metadata resolution layers (Crossref-style linking)


# 🔭 Future Directions

Planned expansions:

* 📊 Precision / Recall scoring metrics
* 🧮 Statistical comparison across >20 queries
* 🧪 Inclusion of additional retrieval systems


# Repository Purpose

This repository serves as:
* A benchmark framework for AI literature retrieval evaluation
* A reproducible testing structure
* A comparative reference for scientific researchers


