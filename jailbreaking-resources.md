# Jailbreaking & Agent Red-Teaming — Resource List

Curated reading for **authorized** AI red-teaming (red-teaming platforms, CTFs, sanctioned pentests, your own systems). This is defensive literature: it catalogs how tool-using agents and aligned models fail, so the failures can be hardened against.

*Links verified live as of November 2026. Several papers and standards are revised periodically — check each source for a newer edition.*

---

## Taxonomies & risk catalogs (start here)

- **OWASP Top 10 for LLM Applications** — the standard catalog of LLM/agent risks: prompt injection, excessive agency, system-prompt leakage, and more. Maintained by the OWASP GenAI Security Project.
  <https://genai.owasp.org/llm-top-10/>
- **MITRE ATLAS** — adversarial-threat knowledge base for AI systems, structured like ATT&CK (tactics, techniques, and real-world case studies).
  <https://atlas.mitre.org/>
- **NIST AI 100-2e2025** — *Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations.* Organizes attacks by ML method, lifecycle stage, and attacker goals/capabilities; covers evasion, poisoning, privacy, and generative-AI attacks including prompt injection.
  <https://csrc.nist.gov/pubs/ai/100/2/e2025/final>

## Agent-specific attacks & benchmarks

- **Greshake et al. (2023)** — *Not what you've signed up for: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection.* The foundational indirect-prompt-injection paper; shows attacker instructions planted in retrieved content can hijack an app with no direct model access.
  arXiv:2302.12173 — <https://arxiv.org/abs/2302.12173>
- **Debenedetti et al. (2024)** — *AgentDojo: A Dynamic Environment to Evaluate Attacks and Defenses for LLM Agents.* Benchmark of tasks + security test cases for tool-using agents under injection.
  arXiv:2406.13352 — <https://arxiv.org/abs/2406.13352> · code: <https://github.com/ethz-spylab/agentdojo>
- **Zhan et al. (2024)** — *InjecAgent: Benchmarking Indirect Prompt Injections in Tool-Integrated LLM Agents.* 1,054 test cases across 17 user tools and 62 attacker tools.
  arXiv:2403.02691 — <https://arxiv.org/abs/2403.02691> · code: <https://github.com/uiuc-kang-lab/InjecAgent>

## Jailbreaking & model internals (why guards hold or fail)

- **Wei, Haghtalab, Steinhardt (2023)** — *Jailbroken: How Does LLM Safety Training Fail?* Two mechanisms — **competing objectives** vs. **mismatched generalization** — explain why reframe and obfuscation attacks work.
  arXiv:2307.02483 — <https://arxiv.org/abs/2307.02483>
- **Zou et al. (2023)** — *Universal and Transferable Adversarial Attacks on Aligned Language Models* (the **GCG** attack). Automated adversarial suffixes that transfer across models.
  arXiv:2307.15043 — <https://arxiv.org/abs/2307.15043> · code: <https://github.com/llm-attacks/llm-attacks>
- **Arditi et al. (2024)** — *Refusal in Language Models Is Mediated by a Single Direction.* Why some guards are shallow/word-triggered and others robust; refusal lives in a one-dimensional subspace in many open models.
  arXiv:2406.11717 — <https://arxiv.org/abs/2406.11717> · code: <https://github.com/andyrdt/refusal_direction>
- **Anthropic (2024)** — *Many-shot jailbreaking.* A long-context attack that scales with the number of in-context examples; explains why "context dilution" works only on soft-state guards.
  <https://www.anthropic.com/research/many-shot-jailbreaking>

## Hands-on practice (sandboxed, authorized)

- **Gray Swan Arena** — authorized agent red-teaming challenges and competitions.
  <https://app.grayswan.ai/>
- **Lakera Gandalf / Agent Breaker** — a prompt-injection practice game.
  <https://gandalf.lakera.ai/>
- **Simon Willison's prompt-injection series** — ongoing practitioner write-ups tracking current developments.
  <https://simonwillison.net/tags/prompt-injection/>

---

*For authorized testing and defensive research only. These resources describe how tool-using agents and aligned models fail so they can be built not to — not a license to point techniques at systems you don't own.*
