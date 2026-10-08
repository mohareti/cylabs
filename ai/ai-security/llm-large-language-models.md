---
description: "A large language model (LLM) is a neural network, usually a transformer, trained on very large text corpora to predict the next token."
---

# LLM (Large Language Models)

A large language model (LLM) is a neural network, usually a transformer, trained on very large text corpora to predict the next token. That one skill, scaled up, gives it the ability to summarize, translate, write code, answer questions and follow instructions.

## How an LLM application is put together

Most real-world LLM systems are more than the model. The security boundary is the whole application:

| Layer | What it is | Why security cares |
|---|---|---|
| **Model** | The trained weights, hosted by a vendor or self-hosted | Poisoned or backdoored weights, model theft |
| **System prompt** | Hidden instructions that set the model's role and rules | Leakage, override by user input |
| **Context / RAG** | Documents retrieved from a vector store and added to the prompt | Indirect prompt injection, data leakage across tenants |
| **Tools & agents** | Functions the model can call: APIs, databases, shell, browser | Excessive agency: the model can *act*, not just talk |
| **Output handling** | Where the response goes next: UI, code, another system | XSS, SQL or command injection via model output |
| **Memory** | Conversation history or long-term memory stores | Persistence of injected instructions, privacy |

## Key properties that create risk

* **Instructions and data share one channel.** The model cannot reliably tell the developer's instructions from text it reads in an email or web page.
* **Output is probabilistic.** The same input can produce different output, so controls must not depend on the model "behaving".
* **Models are confident when wrong.** Hallucinated facts, packages or citations look as plausible as real ones.

## Security checklist for an LLM application

* Treat every model output as untrusted input to the next system.
* Give tools the least privilege possible and require human approval for high-impact actions.
* Keep secrets out of system prompts; assume they will leak.
* Enforce access control in the retrieval layer, not in the prompt.
* Log prompts, retrieved context, tool calls and outputs for detection and forensics.
* Rate-limit and cap tokens per user to prevent cost and resource abuse.

See also: [OWASP Top 10 for LLM Applications](security-frameworks/owasp-top-10-llms.md) · [Prompt Injection](ai-attacks/prompt-injection.md)
