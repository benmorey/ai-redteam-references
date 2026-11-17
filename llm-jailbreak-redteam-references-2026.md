# LLM Jailbreak & Red Team References — 2025/2026

**Curated by:** sakurablush  
**Date:** 2026-09-09  
**Purpose:** Competition-grade reference list of the best red-team research, tools, and sources for direct injection / jailbreak / prompt-injection work.

---

## GitHub Repositories

| Repository | Description | Stars |
|------------|-------------|-------|
| [asgeirtj/system_prompts_leaks](https://github.com/asgeirtj/system_prompts_leaks) | Extracted system prompts from ChatGPT, Claude, Gemini, Grok, Perplexity, and more. Updated regularly. | 53k+ |
| [belinwu/system_prompts_leaks](https://github.com/belinwu/system_prompts_leaks) | Another active system prompt archive with diffs between model versions. | — |
| [elder-plinius/CL4R1T4S](https://github.com/elder-plinius/CL4R1T4S) | Pliny's leaked system prompts collection, including Claude Fable 5 (270K chars). | — |
| [elder-plinius/G0DM0D3](https://github.com/elder-plinius/G0DM0D3) | Liberation prompts and battle-tested jailbreak prompt combos for multiple models. | 11k+ |
| [anwhelan01/L1B3RT45](https://github.com/anwhelan01/L1B3RT45) | Community mirror of Pliny's jailbreak prompts for all major AI models. | — |
| [mlcommons/jailbreak-taxonomy](https://github.com/mlcommons/jailbreak-taxonomy) | Standardized jailbreak taxonomy with families, leaves, prevalence, and paper links. | — |
| [zhipeng-wei/EmojiAttack](https://github.com/zhipeng-wei/EmojiAttack) | Emoji Attack implementation — disrupts Judge LLM tokenization during evaluation. | — |
| [TransluceAI/jailbreaking-frontier-models](https://github.com/TransluceAI/jailbreaking-frontier-models) | Reference implementation for RL-trained investigator agents that jailbreak frontier models. | — |
| [nerudek/llm-jailbreak-techniques](https://github.com/nerudek/llm-jailbreak-techniques) | 33 obfuscation techniques, 27 prefill templates, 4 roleplay patterns, 7 token smuggling methods. | — |
| [becheng/agent-security-wiki](https://github.com/becheng/agent-security-wiki) | Agent security wiki with multi-turn jailbreak and prompt injection technique notes (2026). | — |
| [xspeen/DeepSeek-Jailbreak-OneShot](https://github.com/xspeen/DeepSeek-Jailbreak-OneShot) | One-shot DeepSeek jailbreak framework with validated prompt variants. | — |
| [MartinRJ/LLMJailbreakResources2026](https://github.com/MartinRJ/LLMJailbreakResources2026) | Curated 2026 jailbreak resources, including leaked prompts and technique-driven payloads. | — |

---

## Academic Papers & Preprints

| Paper | Authors / Venue | Key Contribution |
|-------|----------------|----------------|
| [Involuntary Jailbreak: On Self-Prompting Attacks](https://arxiv.org/abs/2508.13246) | Guo, Li, Kankanhalli — ICLR 2026 | Single universal prompt jailbreaking Claude Opus 4.1, Grok 4, Gemini 2.5 Pro, GPT-4.1 with >90% ASA. |
| [UniAttack: Automated jailbreak attack targeting multiple defense strategies](https://arxiv.org/abs/2606.16751) | Wang et al. — arXiv:2606.16751 | Fusion-based black-box attack; 64.63%-248.82% ASR improvement; 99% ASR on Gemini-2.0-Flash. |
| [Prefill-level Jailbreak: A Black-Box Risk Analysis](https://arxiv.org/abs/2602.14689) | Struppek, Gleave, Pelrine — FAR.AI / arXiv:2602.14689 | Largest empirical study of prefill attacks; 28-98% ASR; up to 99% with optimization. |
| [Sockpuppetting: Jailbreaking LLMs by Combining Prefilling with Optimization](https://arxiv.org/abs/2601.13359) | Dotsinski & Eustratiadis — arXiv:2601.13359 | Introduces sockpuppeting via assistant prefill; ensemble prefill variants improve success. |
| [Breaking Refusal in the First Half: A Mechanistic Study of the Prefill Jailbreak](https://arxiv.org/abs/2607.14147) | Kwon — arXiv:2607.14147 | Shows refusal is a shallow response-site computation localized to the first half of generation. |
| [Great, Now Write an Article About That: The Crescendo Multi-Turn LLM Jailbreak Attack](https://arxiv.org/abs/2404.01833) | Russinovich, Salem, Eldan — Microsoft / USENIX Security 2025 | Crescendo multi-turn attack; 98% binary success on GPT-4, 100% on Gemini-Pro. |
| [Tree of Attacks: Jailbreaking Black-Box LLMs Automatically](https://arxiv.org/abs/2312.02119) | Mehrotra et al. — NeurIPS 2024 | TAP automated black-box jailbreak; 94-98% success on GPT-4o/Gemini-Pro. |
| [AutoRedTeamer: Autonomous Red Teaming with Lifelong Attack Integration](https://arxiv.org/abs/2503.15754) | Zhou et al. — arXiv:2503.15754 | Fully automated red teaming; 20% higher ASR on HarmBench, 46% lower cost. |
| [Automatically Jailbreaking Frontier Language Models with Investigator Agents](https://transluce.org/jailbreaking-frontier-models) | Chowdhury, Schwettmann, Steinhardt — Transluce / Sep 2025 | RL-trained 8B investigator agents jailbreak GPT-5-main (78%), Claude Sonnet 4 (92%), Gemini 2.5 Pro (90%). |
| [Red Teaming the Mind of the Machine: A Systematic Evaluation of Prompt Injection and Jailbreak Vulnerabilities in LLMs](https://arxiv.org/abs/2505.04806) | Pathade et al. — CMU / arXiv:2505.04806 | Systematic evaluation over 1,400 adversarial prompts across GPT-4, Claude 2, Mistral 7B, Vicuna. |
| [SoK: A Comprehensive Security Analysis of Jailbreak Resilience in GPT and DeepSeek Models](https://arxiv.org/abs/2506.18543) | Wu et al. — arXiv:2506.18543 | Comparative jailbreak resilience analysis; GPT-4 more robust than DeepSeek overall. |
| [Large reasoning models are autonomous jailbreak agents](https://www.nature.com/articles/s41467-026-XXXXX) | Hagendorff et al. — Nature Communications May 2026 | 4 attacker LRMs × 9 targets × 70 prompts = 25,200 runs; 97.14% overall jailbreak success. |
| [ArtPrompt: ASCII Art-based Jailbreak Attacks against Aligned LLMs](https://aclanthology.org/2024.acl-long.809) | ACL 2024 | ASCII-encoded harmful keywords bypass safety filters across GPT-3.5, GPT-4, Gemini, Claude, Llama2. |
| [Emoji Attack: Enhancing Jailbreak Attacks Against Judge LLM Detection](https://arxiv.org/abs/2411.01077) | Wei, Liu, Erichson — ICML 2025 | Inserts emojis to disrupt Judge LLM tokenization; 12% reduction in unsafe prediction rate. |
| [Na'vi or Knave: Jailbreaking Language Models via Metaphorical Avatars](https://arxiv.org/abs/2412.12145) | NeurIPS 2024 SoLaR Workshop | AVATAR metaphor-mapping jailbreak; state-of-the-art transferable ASR across models. |
| [MetaCipher: A General and Extensible Reinforcement Learning Framework for Obfuscation-Based Jailbreak Attacks](https://arxiv.org/abs/2506.22557) | arXiv:2506.22557 | RL-based cipher selection from 9 ciphers; optimizes obfuscation for black-box LLMs. |
| [Tool-Framing Bypasses LLM Safety: Procedural Abstraction](https://openreview.net/forum?id=ysiOhmgECl) | OpenReview 2026 | Shows tool-use framing sharply reduces safety refusals by decomposing harmful intent into legitimate API calls. |

---

## Vendor / Lab Reports & Blogs

| Source | Date | Key Finding |
|--------|------|-------------|
| [FAR.AI AI Security Leaderboard](https://leaderboard.far.ai/docs/report.pdf) | July 2026 | 100x+ gap in attack cost: $58 for Grok 4.5 vs >$14,200 for Claude Fable 5 / GPT-5.6 Sol. |
| [FAR.AI Press Release — A Hundredfold Gap in AI Security](https://www.prnewswire.com/news-releases/farai-launches-ai-security-leaderboard-revealing-hundredfold-gap-in-frontier-ai-model-safeguards-302838216.html) | July 2026 | 448 universal jailbreaks on Grok, 249 on Gemini; 0 on Claude/GPT under same automated suite. |
| [Gray Swan — Your AI Agent Can Be Compromised. You'd Never Know.](https://www.grayswan.ai/blog/your-ai-agent-can-be-compromised-youd-never-know) | March 2026 | IPI Arena: 272,000+ attacks, 464 participants, 13 models, 8,648 successful breaks. Universal fake-control-panel template worked across 21/41 scenarios and 9 models. |
| [Gray Swan Hazard Hunt Q3 2026](https://app.grayswan.ai/arena/challenge/hazard-hunt-q3) | Aug-Sep 2026 | $80K prize pool; direct elicitation across chemical, biological, cyber, miscellaneous categories. |
| [Anthropic — Constitutional Classifiers](https://www.anthropic.com/research/constitutional-classifiers) | Feb 2025 | Reduced jailbreak success from 86% to 4.4%; 95%+ block rate with minimal over-refusal. |
| [Anthropic — Next-generation Constitutional Classifiers](https://www.anthropic.com/research/next-generation-constitutional-classifiers) | Jan 2026 | Constitutional Classifiers++; no universal jailbreak after 1,700+ hours red teaming; ~1% compute cost. |
| [Anthropic — Frontier Red Team](https://www.anthropic.com/research/team/frontier-red-team) | 2025-2026 | Latest frontier red team publications on cybersecurity, biosecurity, and autonomous systems. |
| [Google DeepMind — CaMeL](https://www.deepmind.com/technologies/camel) | 2025 | Control-flow-based defense; neutralizes 67% of attacks in AgentDojo benchmark. |
| [Google AI Progress Report](https://ai.google/static/documents/ai-responsibility-update-2026.pdf) | Feb 2026 | Gemini 3 gains in reducing sycophancy, resisting prompt injections, and improving protection against cyber misuse. |
| [Microsoft Research — Crescendo](https://www.usenix.org/conference/usenixsecurity25/presentation/russinovich) | USENIX Security 2025 | Multi-turn jailbreak; 29-61% improvement over single-turn on GPT-4; 49-71% on Gemini-Pro. |
| [Palo Alto Unit 42 — Autonomous AI Attack Pipelines Move Into the Field](https://labs.cloudsecurityalliance.org/wp-content/uploads/2026/07/CSA_research_note_ai_driven_threat_actor_autonomous_exploitation_20260730-csa-styled-1.pdf) | July 2026 | DeepSeek + Hermes Agent automated 460+ target attack campaign; Claude/Codex refused similar requests. |
| [Cloud Security Alliance — Indirect Prompt Injection Goes Operational](https://labs.cloudsecurityalliance.org/wp-content/uploads/2026/04/CSA_research_note_indirect_prompt_injection_in_the_wild_20260426-csa-styled.pdf) | April 2026 | Documents live IPI exploitation, GrafanaGhost case, and 32% increase in malicious IPI content. |
| [Cloud Security Alliance — Sockpuppeting: LLM Safety Bypass via API Prefill Injection](https://labs.cloudsecurityalliance.org/wp-content/uploads/2026/04/CSA_research_note_sockpuppeting_llm_api_jailbreak_20260413-csa-styled.pdf) | April 2026 | Prefill injection as systematic vulnerability; 28-98% ASR across frontier models. |
| [WIRED — It's Frighteningly Easy to Jailbreak Some Frontier AI Models](https://www.wired.com/story/jailbreaking-ai-models-google-anthropic-openai-spacexai) | July 2026 | FAR.AI automated testing: 448 jailbreaks on Grok, 249 on Gemini; Claude and GPT impervious to same automated suite. |
| [Washington Post — See the hidden rules behind AI](https://www.washingtonpost.com/technology/interactive/2026/ai-system-prompts-leaked/) | May 2026 | Built interactive story using leaked system prompts from asgeirtj/system_prompts_leaks repository. |

---

## Red Teamers & Influential Researchers to Follow

| Handle / Name | Affiliation / Role | Notable Work |
|---------------|-------------------|--------------|
| [Pliny the Liberator](https://x.com/elder_plinius) | Independent jailbreak researcher | Fable 5 jailbreak, system prompt leaks, G0DM0D3, L1B3RT45 |
| [Adam Gleave](https://x.com/adamgleave) | FAR.AI CEO | FAR.AI Security Leaderboard, prefill jailbreak research |
| [Mark Russinovich](https://x.com/markrussinovich) | Microsoft Azure | Crescendo multi-turn jailbreak (USENIX Security 2025) |
| [Logan Graham](https://x.com/logangraham) | Anthropic Frontier Red Team Lead | Frontier red team publications, AI safety evaluation |
| [Neil Chowdhury](https://transluce.org) | Transluce AI | Investigator agents, RL-based automated jailbreaking |
| [Kellin Pelrine](https://x.com/kellinpelrine) | FAR.AI / researcher | Prefill attacks, jailbreak taxonomy |
| [Lukas Struppek](https://x.com/lukasstruppek) | FAR.AI / researcher | Systematic prefill attack study |
| [Anay Mehrotra](https://x.com/anaymehrotra) | Researcher | Tree of Attacks with Pruning (TAP), NeurIPS 2024 |
| [Andy Zhou](https://x.com/andyzhou) | Researcher | AutoRedTeamer, lifelong attack integration |
| [Qi Wang](https://x.com/) | Researcher | UniAttack fusion-based automated attack |

---

## Competition Platforms & Challenges

| Platform | URL | Focus |
|----------|-----|-------|
| Gray Swan Arena | https://app.grayswan.ai/arena | Direct/indirect prompt injection, agentic AI red teaming |
| Hazard Hunt Q3 2026 | https://app.grayswan.ai/arena/challenge/hazard-hunt-q3 | Chemical, biological, cyber, miscellaneous harm ($80K prize pool) |
| Indirect Prompt Injection Aug 2026 | https://app.grayswan.ai/arena/challenge/ipi-aug-2026 | Tool use, computer use, coding agent IPI ($30K prize pool) |

---

## Defense Mechanisms & Tools

| Defense / Tool | Provider / Author | Effectiveness |
|----------------|-------------------|---------------|
| Constitutional Classifiers | Anthropic | 95%+ jailbreak block rate |
| Constitutional Classifiers++ | Anthropic | Next-gen; ~1% compute cost |
| CaMeL | Google DeepMind | 67% attack neutralization in AgentDojo |
| MELON | Research | System-level defense |
| PIGuard | Research | Filter-based defense |
| Spotlighting | Research | Prompt-based defense |
| Llama Guard | Meta | Input/output filtering |
| PyRIT (Crescendomation) | Microsoft | Automated Crescendo attack tool |

---
