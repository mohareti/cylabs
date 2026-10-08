---
description: "The NIST AI Risk Management Framework (AI RMF 1.0), released in January 2023, is a voluntary framework for managing risks across the AI lifecycle."
---

# NIST AI Risk Management Framework

The [NIST AI Risk Management Framework (AI RMF 1.0)](https://www.nist.gov/itl/ai-risk-management-framework), released in January 2023, is a voluntary framework for managing risks across the AI lifecycle. In July 2024 NIST added a **Generative AI Profile (NIST AI 600-1)** that applies the framework to GenAI risks.

## Characteristics of trustworthy AI

The framework describes AI that is valid and reliable; safe; secure and resilient; accountable and transparent; explainable and interpretable; privacy-enhanced; and fair, with harmful bias managed.

## The four functions

| Function | Purpose | Example activities |
|---|---|---|
| **GOVERN** | Build a culture and structure for AI risk management (applies across all functions) | Policies, roles, AI inventory, risk tolerance, training |
| **MAP** | Understand the context and identify risks for each AI system | Intended use, users, data sources, potential harms, dependencies |
| **MEASURE** | Analyze and track identified risks | Testing, red teaming, bias and robustness metrics, monitoring |
| **MANAGE** | Prioritize and act on risks | Mitigations, go/no-go decisions, incident response, decommissioning |

## Applying it in practice

1. **Govern:** publish an [AI policy](../ai-cyber-security-risk-management/ai-policies.md) and keep an inventory of AI systems with owners.
2. **Map:** for each system, document purpose, data, users and what happens if it is wrong.
3. **Measure:** test against the [OWASP Top 10 for LLMs](owasp-top-10-llms.md) and [MITRE ATLAS](mitre-atlas.md) techniques; track results over time.
4. **Manage:** fix or accept risks with sign-off, monitor in production, and feed incidents back into Govern.

## Related standards

* **ISO/IEC 42001:** a certifiable AI management system standard
* **EU AI Act:** risk-based regulation for AI systems placed on the EU market
