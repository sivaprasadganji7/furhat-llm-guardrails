# furhat-llm-guardrails
System-level evaluation of safety and controllability in LLM-based dialogue for social robots
# Evaluating Safety and Controllability of LLM-Based Feedback in a Social Robot

This repository contains the implementation and experimental framework for an MSc dissertation
investigating the safety and controllability of Large Language Model (LLM)-based dialogue
in a social robot context.

The project compares three dialogue strategies used for generating feedback:

1. **Scripted (Rule-Based) Dialogue**
2. **LLM Prompt-Only Dialogue**
3. **LLM Dialogue with Explicit Safety Guardrails**

The work adopts a **system-level Human–Robot Interaction (HRI)** perspective and does not
evaluate user experience or learning outcomes.

---

## Research Motivation

Recent HRI systems increasingly integrate LLMs to enable adaptive dialogue in social robots.
However, prompt-only LLM integration raises concerns regarding:

- hallucinated or unsafe feedback
- lack of controllability
- vulnerability to prompt manipulation
- suitability for public-facing robotic systems

This project provides a controlled empirical comparison of dialogue strategies to assess
how explicit guardrails affect safety, consistency, and controllability.

---

## Project Scope

- No human participants
- No evaluation of interview training effectiveness
- Interview-style interaction used **only as a controlled test scenario**
- Focus on **feedback generation behaviour**

---

## Dialogue Strategies

### 1. Scripted
- Deterministic rule-based feedback
- Maximum controllability
- Minimal adaptivity

### 2. LLM Prompt-Only
- Feedback generated directly by an LLM
- Prompt-based constraints only
- High flexibility, limited safety guarantees

### 3. LLM + Guardrails
- LLM-generated feedback
- Explicit rule-based safety checks
- Unsafe outputs replaced with safe fallback responses

---

## Implementation Overview

- Backend implemented in Python
- LLM accessed via API
- Safety guardrails implemented using rule-based checks
- All outputs logged for reproducible evaluation
- Furhat robot used as an interaction interface (optional / simulator-supported)

---

## Running the Experiments

### Requirements
- Python 3.9+
- OpenAI API key (set as environment variable)

```bash
pip install -r requirements.txt
export OPENAI_API_KEY="your_key_here"
