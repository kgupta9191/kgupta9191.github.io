---
title: "Agentic Rag"
date: 2026-05-06

links:
  - name: Repo
    url: "https://github.com/kgupta9191/Agentic-RAG"
    icon: brands/github

tags:
  - AI
  - FAISS
  - RAG
---

## Introduction

Question-answering systems built on large language models often suffer from hallucination — generating fluent but factually unsupported responses. Retrieval-Augmented Generation (RAG) addresses this by grounding model outputs in external documents, but most RAG implementations are single-pass pipelines that retrieve once and answer once, with no quality validation. This project implements an Agentic RAG system that introduces decision-making control points at each stage of the pipeline. Built on LangGraph, the system incorporates relevance gating, grounding verification, retry logic, and equation-solving support via SymPy — making it well-suited for technical and scientific question answering over document corpora.

## Background

Standard RAG pipelines follow a straightforward three-step process: retrieve relevant chunks, pass them to an LLM, and return the generated answer. While effective for simple queries, this approach fails silently when retrieved context is irrelevant or when the generated answer is not actually supported by the retrieved material. There is no mechanism to catch or recover from these failures.

Agentic systems address this gap by encoding explicit decision policies into the pipeline. Rather than a linear chain, an agentic approach uses a stateful graph where each node can inspect intermediate outputs and conditionally route to retry, fallback, or tool-augmented paths. LangGraph provides exactly this infrastructure — a stateful graph framework built on top of LangChain that supports branching, retries, and multi-step reasoning workflows.

The four key intelligent control points in this system are: a relevance grader that verifies whether retrieved chunks are actually pertinent to the user query; an answer generator that produces a response strictly from retrieved context; a grounding checker that validates the answer is supported by the source material; and a SymPy-based equation solver that handles formula-driven queries symbolically rather than relying solely on language model reasoning.

## Objective

- Build a stateful, decision-driven RAG pipeline using LangGraph with explicit relevance and grounding checkpoints
- Implement conditional routing with retry logic and a safe fallback response for low-confidence outputs
- Augment the pipeline with symbolic equation-solving for technical/scientific document Q&A
- Provide a reproducible, testable implementation with a Streamlit chat interface

## Computational Environment

- OpenAI
- Framework: LangGraph
- Streamlit

## Results

The system successfully demonstrates end-to-end agentic control over the RAG pipeline. The relevance grader correctly gates irrelevant retrievals before answer generation, preventing the model from hallucinating on out-of-scope queries and routing them instead to a safe fallback. The grounding checker catches weakly supported answers and triggers a single retry before falling back, improving output reliability over a naive single-pass baseline.
