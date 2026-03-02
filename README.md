# Comparative Evaluation of Scientific Literature Search & Retrieval Tools

## Overview

This repository documents a structured comparison of leading AI-powered scientific literature search and research assistance tools currently available.

The goal of this study is to evaluate how effectively different systems retrieve **key scientific papers** when presented with carefully constructed research queries derived from peer-reviewed publications.

Tools evaluated:

* **Google Labs (AI Search / Experimental Search)**
* **Allen AI Paper Finder**
* **Undermind**
* **ChatGPT**
* **Gemini**

The comparison focuses on **retrieval performance**, not general summarization quality.

---

# Literature Search Retrieval Tools vs Summarization Tools

Before presenting the experiments, it is important to distinguish between two fundamentally different categories of AI research tools:

## 1️⃣ Literature Search / Retrieval Tools

**Purpose:**
To identify and return relevant academic papers given a query.

**Core Functionality:**

* Searches indexed scientific databases
* Returns papers ranked by relevance
* May provide metadata (DOI, authors, journal, year)
* Sometimes provides short abstracts

**Evaluation Criteria:**

* Does it retrieve expected key papers?
* Does it retrieve highly cited foundational work?
* Does it introduce irrelevant papers?
* Does it retrieve beyond obvious keyword matching?

Examples:

* Allen AI Paper Finder
* Google Labs
* Undermind

---

## 2️⃣ Summarization / Generative AI Tools

**Purpose:**
To synthesize, summarize, or explain scientific knowledge.

**Core Functionality:**

* Generates structured answers
* Summarizes literature
* Explains concepts
* May or may not retrieve specific real papers

**Limitations:**

* May hallucinate citations
* Not guaranteed to retrieve foundational studies
* Often optimized for explanation rather than recall precision

Examples:

* ChatGPT
* Gemini

---

# Experimental Design

## Methodology

To rigorously test retrieval performance, the following controlled approach was used:

### Step 1 — Select a Published Peer-Reviewed Paper

A paragraph was extracted from a published scientific article. The paragraph included:
* Explicit citations
* Foundational papers
* Regional context
* Policy-relevant implications
These cited works form the **Expected Papers** list.
---
### Step 2 — Construct a Reverse Retrieval Query
Using ChatGPT, the paragraph was transformed into a **research-style question**.
The goal:
> If the tool works properly, querying this question should retrieve some of the key cited papers.
Important:
* The original citation DOIs were **not included** in the query.
* The query was phrased naturally.
* Retrieval success was evaluated by overlap with expected foundational papers.

---
### Step 3 — Evaluate Retrieval Output
Each tool was tested using the same query.
For each system, we recorded:
* Retrieved DOIs
* Overlap with Expected Papers
* Additional relevant results
* Missed foundational works
---

# Date 1st March 2026
## 2 queries

<p align="center">
  <img src="output (8).png"; object-fit:contain;">


# Conclusion

This evaluation demonstrates:

* Google Labs consistently outperformed other tools across both queries.
* Google’s ecosystem likely benefits from, very large-scale web crawling infrastructure and Deep indexing of publisher pages (Elsevier, Springer, Nature, PNAS, etc.). Also benfitted by direct access to structured metadata (Crossref-like resolution layers).
* Gemini showed strong performance in Query 1 but dropped in Query 2, indicating sensitivity to query complexity.
* ChatGPT and Allen AI demonstrated lower recall, suggesting limitations in precise DOI-level retrieval.
* Tools differ substantially in their ability to retrieve exact DOI matches rather than related literature.

Future work may include:

* More Queries?
* More tools
---

# Repository Purpose

This repository serves as:

* A benchmark framework for AI literature retrieval evaluation
* A reproducible testing structure
* A comparative reference for scientific researchers


