---
title: "A Multi-Agent Iterative Framework for Reliable Code Debugging"
date: 2026-05-06

links:
  - name: Repo
    url: "https://github.com/kgupta9191/Framework-for-Code-Translation-and-Debugging"
    icon: brands/github

tags:
  - Agentic - AI
  - Langgraph
---

## Introduction

Automated code translation across programming languages is a persistent challenge in scientific computing, where legacy codebases in Fortran and C must increasingly coexist with modern Python, Julia, and CUDA ecosystems. While instruction-tuned Large Language Models (LLMs) have shown strong capabilities in code generation, conventional single-pass inference is unreliable for production-grade migration tasks — failing through missing headers, off-by-one errors, incorrect type declarations, and outputs that compile but produce wrong results. This project presents a structured multi-agent iterative framework that decomposes the translation problem into five sequential, mutually coupled stages: semantic understanding, target-language translation, compilation and execution, error-driven debugging, and logical correctness review. The framework is implemented as a directed state graph using LangGraph, where conditional edges create feedback loops that mirror iterative residual correction in classical numerical methods.

## Background

LLM-based code generation was significantly advanced by Codex and subsequent models such as GPT-4 and Code Llama, which demonstrated high rates of syntactically valid code generation from natural language prompts. However, even state-of-the-art models achieve pass rates well below 100% on established benchmarks like HumanEval and MBPP without iterative correction. Code translation is a strictly harder problem than generation — it requires not only syntactic correctness in the target language but also semantic preservation of runtime behavior with respect to the source.

Prior work on iterative refinement includes self-debugging approaches that use chain-of-thought reasoning, dual-execution filtering (CodeT), and large-scale sampling with filtering (AlphaCode). The key distinction of this framework is the use of actual compilation and execution as the feedback signal — rather than self-criticism or test-case matching — embedded within a formally structured multi-agent state graph. LangGraph provides the stateful graph infrastructure that makes control flow, branching, and loop termination explicit and auditable, making it well-suited to this iterative correction paradigm.

Single-pass LLM translation fails across three systematic failure modes: syntactic failures (missing headers, incorrect type declarations), semantic failures (loss of algorithmic intent, misaligned input-output contracts), and logical failures (code that compiles and runs but produces numerically incorrect results). None of these are reliably detected without execution-based validation, creating the fundamental gap this framework addresses.

## Objective

- Develop a structured multi-agent pipeline that wraps LLM inference within a formal compilation-execution feedback loop
- Implement a directed state graph with conditional routing for retry, debugging, and fallback termination using LangGraph
- Evaluate the framework against single-pass GPT inference across six representative Python-to-C translation test cases
- Draw a formal analogy between the iterative correction mechanism and classical iterative solvers from computational science
- Provide a reproducible, configurable pipeline applicable to automated code migration in scientific computing workflows

## Computational Environment

- OpenAI
- Framework: LangGraph
- Streamlit

## Results

The agentic framework achieved a compilation success rate of 100% and a logical correctness rate of 97.5% across all six test cases, compared to 58.3% and 49.2% respectively for single-pass GPT inference using the same underlying model (gpt-4.1-mini). The mean iteration count to convergence was 1.38, confirming that the feedback loop resolves most errors within 1–2 debugging cycles rather than exhausting the iteration budget.
