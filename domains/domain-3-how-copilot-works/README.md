# Domain 3: How GitHub Copilot Works and Handles Data (15%)

[Home](../../README.md) | [Domain Index](./README.md) | [Previous](../domain-2-plans-and-features/README.md) | [Next](../domain-4-prompt-engineering/README.md)

> Learning Objective: Explain how Copilot transforms raw editor context into code suggestions, describe data handling and retention differences across plan tiers, and identify the key limitations of LLM-based tools.

---

## Exam Relevance

- **Domain weight: 15%** — roughly 1 in 7 exam questions will draw from this domain.
- Understanding the data pipeline and privacy model is essential for real-world compliance decisions, and exam questions frequently test whether candidates can distinguish plan-tier behaviour (e.g. which plans retain prompts, which have telemetry on by default).
- LLM limitation questions are increasingly present in AI certification exams — knowing *why* a model produces incorrect or outdated output is as important as knowing how to prompt it.

---

## Mind Map

```mindmap
root((Domain 3: How Copilot Works))
  Data Pipeline Lifecycle
    Editor collects context
    Proxy service filters prompts
    LLM generates token predictions
    Post-processing applies filters
    Suggestion delivered to IDE
    Duplicate detection check
  Data Handling
    Individual plan
      Telemetry ON by default
      Opt-out available
      Prompts may be retained for improvement
    Business plan
      Telemetry OFF by default
      Prompts NOT retained
      No training on user code
    Enterprise plan
      Telemetry OFF by default
      Prompts NOT retained
      Additional policy controls
    Data in transit
      TLS encryption
      Proxy intermediary
  LLM Limitations
    Probabilistic output
    Finite context window
    Training data cutoff
    Outdated library versions
    Hallucinated APIs
    Bias toward common patterns
    Not a deterministic calculator
```

---

## Comparison Table — Data Retention & Telemetry by Plan

| Behaviour | Copilot Individual | Copilot Business | Copilot Enterprise |
|---|---|---|---|
| **Prompt retention** | May be retained for model improvement | Not retained | Not retained |
| **Suggestion retention** | May be retained for model improvement | Not retained | Not retained |
| **Telemetry default** | ON by default | OFF by default | OFF by default |
| **Opt-out mechanism** | User can opt out in GitHub settings | Off by default; no opt-in for training | Off by default; no opt-in for training |
| **Training on user code** | Possible unless opted out | Never | Never |
| **Policy management** | Individual user controls | Organisation admin controls | Enterprise admin controls with additional policy options |
| **Duplicate detection** | Available | Available | Available |

---

## Domain Cheat Sheet

- Copilot sends a **context window excerpt** to the model, not the full file — only the most relevant surrounding code is selected.
- A **proxy service** sits between the IDE and the LLM; it filters and sanitises prompts before they ever reach the model.
- On the **Individual plan**, telemetry and prompt data collection are **ON by default**; users must actively opt out in GitHub settings.
- On **Business and Enterprise plans**, telemetry is **OFF by default** and user prompts are **never retained** for model training.
- LLMs are **probabilistic text predictors** — the same prompt can yield different outputs on different runs; they are not deterministic calculators.
- The **context window is finite** — Copilot must decide which nearby code, comments, and imports are most relevant to include, and distant code may be omitted.
- **Duplicate detection** compares Copilot suggestions against a reference index of public code and can block or flag matches above a configurable threshold.
- **Training data bias** means common languages and frameworks (e.g. JavaScript, Python) are over-represented; less common languages may receive weaker suggestions.
- **Post-processing filters** run after the LLM responds — they can block, truncate, or modify suggestions before they appear in the editor.
- Suggestions may reference **outdated library versions or deprecated APIs** when the model's training data predates a library's latest release.
- Copilot can **hallucinate function names and parameters** that do not exist in the actual library — always verify suggestions against official documentation.
- The proxy layer applies **content filtering** to avoid generating harmful, offensive, or policy-violating output.
- Accepting or rejecting a suggestion sends **implicit feedback** that can inform future model improvement cycles (subject to plan-tier data retention rules).
- GitHub does **not sell user data** from Copilot interactions, and data transmitted is protected with TLS encryption in transit.

---

## Subtopics

| Page | Description |
|---|---|
| [Data Pipeline Lifecycle](./data-pipeline-lifecycle.md) | Step-by-step walkthrough of how editor context is collected, filtered, sent to the LLM, and returned as a suggestion. |
| [Data Handling](./data-handling.md) | How prompts, suggestions, and telemetry are stored, shared, and retained — and how this differs by plan tier. |
| [LLM Limitations](./llm-limitations.md) | Why LLM-based tools are probabilistic, context-bound, and prone to hallucination, bias, and outdated knowledge. |

---

## Originality Declaration

- All explanations, diagrams, and cheat-sheet bullets are original instructional content.
- No source text was copied verbatim; sources were used for factual grounding only.

---

## Sources Consulted

- https://docs.github.com/en/copilot/overview-of-github-copilot/about-github-copilot-individual
- https://docs.github.com/en/copilot/privacy-and-security-for-github-copilot
- https://resources.github.com/learn/pathways/copilot/essentials/how-github-copilot-works/

---

## Potential Similarity Risk

- **Risk level: Low**
- Notes: Technical terms (e.g. "proxy service", "context window") are industry-standard vocabulary and will appear in any accurate explanation of this domain. No source phrases were reproduced.

---

## References

- Facts referenced; all explanations are original and newly written.
- https://docs.github.com/en/copilot/overview-of-github-copilot/about-github-copilot-individual
- https://docs.github.com/en/copilot/privacy-and-security-for-github-copilot
- https://resources.github.com/learn/pathways/copilot/essentials/how-github-copilot-works/

---

[Home](../../README.md) | [Domain Index](./README.md) | [Previous](../domain-2-plans-and-features/README.md) | [Next](../domain-4-prompt-engineering/README.md)
