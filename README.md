#  AI-Powered Clinical Trial Matching System

This project presents an intelligent pipeline for **matching patients with suitable clinical trials** using state-of-the-art **Large Language Models (LLMs)**, semantic embeddings with **BioClinicalBERT**, and **retrieval-augmented generation (RAG)** techniques. 
It aims to automate the labor-intensive process of identifying relevant trials for patients, thereby accelerating clinical decision-making and patient recruitment.

---

## Overview

The system:
- Parses and preprocesses **patient records** and **clinical trial data** (titles, summaries, inclusion/exclusion criteria).
- Generates **dense embeddings** using `BioClinicalBERT`.
- Stores embeddings in a **FAISS index** for efficient retrieval.
- Employs a **RAG pipeline** powered by `FLAN-T5-base` to generate context-aware matches.
- Provides **model interpretability** using `LIME` and `SHAP`.

---
## How It Works
1. Data Ingestion & Preprocessing
Parses structured clinical trial data (e.g., from ClinicalTrials.gov).

Normalizes and tokenizes patient and trial information.

2. Embedding Generation
Uses BioClinicalBERT to create vector representations for each trial's text.

3. Indexing
Stores embeddings in a FAISS index for rapid semantic similarity search.

4. Retrieval-Augmented Generation
Accepts a patient profile query.

Retrieves top-k similar trials from the FAISS index.

Feeds trials + query to FLAN-T5-base for natural language generation of a match report.

5. Explainability
Uses LIME and SHAP to visualize which tokens/features influenced the decision.

## Use Cases
Clinical Decision Support: Aid doctors in quickly identifying fitting trials.

Patient Portals: Enable patients to search for trials using natural language.

Healthcare Research: Analyze criteria-matching patterns across diverse populations.

## Conclusion

This project demonstrates a robust AI-driven approach to clinical trial matching using state-of-the-art NLP models and explainability tools. From semantic embedding with BioClinicalBERT to retrieval and generation with FLAN-T5 and interpretability with LIME and SHAP, the system bridges patients with trials in a transparent and intelligent way.

Whether you're a researcher, clinician, or student, this project offers a valuable foundation for building scalable healthcare NLP applications.

---
## Thank you for exploring this project!

