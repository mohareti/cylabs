---
description: "Model manipulation covers attacks that change how a model behaves by tampering with its training data, its weights, or its inputs at inference time."
---

# Model Manipulation

Model manipulation covers attacks that change how a model behaves by tampering with its training data, its weights, or its inputs at inference time.

## Main attack types

| Attack | Stage | What happens |
|---|---|---|
| **Data poisoning** | Training / fine-tuning | Malicious samples are slipped into training data so the model learns wrong or attacker-chosen behavior |
| **Backdoors (trojans)** | Training / supply chain | The model behaves normally until a secret trigger phrase or pattern appears |
| **Evasion (adversarial examples)** | Inference | Small, crafted changes to the input cause misclassification, e.g. malware tweaked to evade an ML detector |
| **Model extraction** | Inference | Repeated queries are used to rebuild a copy of a proprietary model |
| **Membership / model inversion** | Inference | Queries reveal whether a record was in the training set or reconstruct sensitive training data |
| **RAG / embedding poisoning** | Retrieval | Planted documents steer answers for specific queries |

## Where this hits security teams

* ML-based detection (malware, phishing, fraud, UEBA) can be evaded or poisoned.
* Models and datasets pulled from public hubs can carry backdoors or malicious serialized code (for example unsafe pickle files).
* Fine-tuning on user feedback lets attackers shape future behavior.

## Defenses

* Track the provenance of datasets and models; prefer signed artifacts and safe formats such as safetensors.
* Scan model files before loading them, and load them in isolated environments.
* Validate and de-duplicate training data; look for outliers and label flips.
* Evaluate models against adversarial test sets before deployment and after each retrain.
* Rate-limit and monitor query patterns to spot extraction attempts.
* Keep an inventory of models, versions and data sources (an AI bill of materials).

References: [MITRE ATLAS](../security-frameworks/mitre-atlas.md) · [OWASP Top 10 for LLMs](../security-frameworks/owasp-top-10-llms.md)
