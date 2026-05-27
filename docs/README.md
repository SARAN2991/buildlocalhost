# BRK230 Documentation

This folder contains session-specific walkthroughs, diagrams, and reference material for **BRK230: Build Smarter AI Systems in Foundry as Models and Costs Evolve**.

> 🧪 **All hands-on labs and demo code for this session live in a dedicated repo:**
>
> **[microsoft-foundry/model-releases](https://github.com/microsoft-foundry/model-releases)**
>
> *Hands-on samples for Microsoft Foundry model releases, assembled into partner workshops for active skilling.*

Use this `docs/` folder for the conceptual walkthrough that ties the demos together. Use the linked repo for the executable code, datasets, and step-by-step lab instructions.

## How the content is organized

| Where | What you'll find |
|:------|:-----------------|
| **This folder (`/docs`)** | Session walkthrough, architecture diagrams, slide commentary, the Carmen scenario, metric tables, and explanations of the four acts (Select, Evaluate, Optimize, Operate). |
| **[`/src`](../src/)** | Small inline snippets and helper scripts referenced from the slides. |
| **[microsoft-foundry/model-releases](https://github.com/microsoft-foundry/model-releases)** | Full hands-on labs: runnable notebooks, evaluation harnesses, model router configs, fine-tuning and distillation pipelines, and partner workshop content. |

## Lab map: session content to hands-on labs

Each act of the session has a matching lab in the [model-releases](https://github.com/microsoft-foundry/model-releases) repo. Open the repo and pick the folder that matches the act you want to practice.

| Act | Session topic | Lab in `microsoft-foundry/model-releases` |
|:----|:--------------|:-------------------------------------------|
| **01 Select** | Browse the Foundry Models catalog (Azure OpenAI, Claude, MAI, DeepSeek, Mistral, Grok, Llama, Cohere, Fireworks AI). Decompose Carmen's request into jobs and shortlist a candidate model per job. | Model selection and catalog browsing samples. |
| **02 Evaluate** | Build an eval dataset, define quality, latency, and cost criteria, and compare models side by side with built-in and custom evaluators. | Evaluation harness, dataset curation, and evaluator samples. |
| **03 Optimize** | Apply the cost optimization stack: model router, prompt and semantic caching, structured outputs, global batch, provisioned throughput (PTU), and distillation or fine-tuning. | Model Router configs, caching examples, PTU sizing, distillation pipelines. |
| **04 Operate** | Deploy with managed endpoints, versioning, rollback, monitoring, responsible AI guardrails, and governance. | Deployment templates, monitoring dashboards, and Agent 365 governance samples. |

## Suggested reading order

1. Read this folder's walkthrough to understand the four-act narrative and the Carmen scenario.
2. Open [microsoft-foundry/model-releases](https://github.com/microsoft-foundry/model-releases) and clone it locally.
3. Work through the labs in the order Select, Evaluate, Optimize, Operate.
4. Come back here for the metric tables and the cost optimization stack diagram when comparing your own results to the session baseline.

## Reference material

- **Carmen scenario**: travel agent decomposed into five jobs (route intent, read receipt, answer policy, plan trip, translate email).
- **Baseline metrics** (GPT-4.1 for every call): quality 0.41, cost $0.023, latency 12.5s.
- **After multi-model routing** (nano + mini + frontier): quality 0.45 (+10%), cost $0.006 (-74%), latency 11.0s (-12%).
- **After distillation** (GPT-4.1-mini fine-tuned from a GPT-4.1 teacher on the policy slice): quality 0.49 (+4%), cost $0.003 (-70%), latency 5.1s (-59%).

## Authoring tips

When you add new content to this folder:

- Use numbered prefixes for ordering: `01-select/`, `02-evaluate/`, `03-optimize/`, `04-operate/`.
- Each subfolder can have its own `README.md` or `index.md`.
- Keep images in an `assets/` subfolder.
- If a topic has a runnable counterpart, link out to the matching folder in [microsoft-foundry/model-releases](https://github.com/microsoft-foundry/model-releases) rather than duplicating code here.
