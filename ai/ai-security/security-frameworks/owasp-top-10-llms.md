---
description: "The OWASP Top 10 for Large Language Model Applications lists the most critical security risks in apps built on LLMs."
---

# OWASP Top 10 LLMs

The OWASP Top 10 for Large Language Model Applications lists the most critical security risks in apps built on LLMs. It is maintained by the [OWASP GenAI Security Project](https://genai.owasp.org/).

{% hint style="info" %}
OWASP published a **2026 edition** on 3 August 2026. It keeps the same ten risk areas but reorders them, moving **Excessive Agency** up and renaming **System Prompt Leakage** to **Hidden Context Exposure**. The table below is the widely used 2025 edition; check the [official 2026 list](https://genai.owasp.org/resource/owasp-genai-llm-top-10-2026/) for the current ranking.
{% endhint %}

## The list (2025 edition)

| ID | Risk | In one line | Key mitigation |
|---|---|---|---|
| LLM01 | **Prompt Injection** | Input changes the model's behavior against the developer's intent | Least-privilege tools, human approval, isolate untrusted content |
| LLM02 | **Sensitive Information Disclosure** | Model reveals personal data, secrets or proprietary data | Data minimization, access control on retrieval, output filtering |
| LLM03 | **Supply Chain** | Compromised models, datasets, plugins or dependencies | Provenance, signed artifacts, AI bill of materials |
| LLM04 | **Data and Model Poisoning** | Tampered training, fine-tuning or embedding data | Data validation, provenance, adversarial testing |
| LLM05 | **Improper Output Handling** | Model output passed to other systems without validation (XSS, SQLi, RCE) | Treat output as untrusted; encode and validate |
| LLM06 | **Excessive Agency** | Agent has too many permissions, functions or autonomy | Minimal tools and scopes, approval for risky actions |
| LLM07 | **System Prompt Leakage** | Hidden instructions, and any secrets in them, are exposed | Keep secrets out of prompts; enforce rules outside the model |
| LLM08 | **Vector and Embedding Weaknesses** | RAG stores leak data across users or get poisoned | Per-tenant access control, validate ingested content |
| LLM09 | **Misinformation** | Confident but false output, including hallucinated packages | Grounding, citations, human review |
| LLM10 | **Unbounded Consumption** | Abuse that drives cost, denial of service or model extraction | Rate limits, quotas, token caps, monitoring |

## Using it in an assessment

1. Map the application: model, prompts, RAG sources, tools and output sinks.
2. For each layer, test the relevant entries (LLM01 and LLM06 for agents, LLM08 for RAG, LLM05 for anything rendering output).
3. Report findings against the OWASP IDs so developers can look up guidance.

See also: [Prompt Injection](../ai-attacks/prompt-injection.md) · [MITRE ATLAS](mitre-atlas.md)
