---
description: "MITRE ATLAS (Adversarial Threat Landscape for Artificial-Intelligence Systems) is a knowledge base of adversary tactics and techniques against AI and machine-learning systems."
---

# MITRE ATLAS

[MITRE ATLAS](https://atlas.mitre.org/) (Adversarial Threat Landscape for Artificial-Intelligence Systems) is a knowledge base of adversary tactics and techniques against AI and machine-learning systems. It is modeled on MITRE ATT&CK, so it will feel familiar to anyone who uses ATT&CK.

## How it is organized

* **Tactics:** the attacker's goal at each stage, such as reconnaissance, initial access, ML model access, persistence, exfiltration and impact.
* **Techniques:** how the goal is achieved, e.g. LLM prompt injection, poisoning training data, evading an ML model, or extracting a model through its API.
* **Mitigations:** controls mapped to the techniques they reduce.
* **Case studies:** documented real-world attacks and red-team exercises against AI systems.

Several ATLAS tactics are shared with ATT&CK, and ATLAS adds AI-specific ones such as ML model access and ML attack staging.

## How to use it

| Use case | How |
|---|---|
| **Threat modeling** | Walk each tactic for your AI system and note which techniques apply |
| **Red teaming** | Build test plans from techniques and case studies |
| **Detection engineering** | Map logs (prompts, tool calls, model API usage) to techniques you can detect |
| **Reporting** | Tag findings with ATLAS technique IDs alongside ATT&CK IDs |

## Tips

* Pair ATLAS with ATT&CK: most AI attacks still involve ordinary steps like credential theft or cloud misconfiguration.
* Browse the case studies first; they show which techniques show up in practice.
* The ATLAS site has a navigator for building your own technique matrix.

See also: [OWASP Top 10 for LLMs](owasp-top-10-llms.md) · [Model Manipulation](../ai-attacks/model-manipulation.md)
