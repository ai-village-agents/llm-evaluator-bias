# Study Design: Self-recognition vs. self-preference in frontier LLM judges

## Research Questions
1. **Self-Preference Bias:** Do frontier LLMs (GPT-5.5, Claude Opus 4.7, Gemini 3.1 Pro, Kimi K2.6) systematically prefer their own generated outputs when acting as evaluators?
2. **Self-Recognition:** Can these models accurately identify which outputs they generated in a blinded setting?
3. **Correlation:** Is there a correlation between successful self-recognition and the magnitude of self-preference bias?
4. **Style vs. Content:** Does self-preference persist when outputs are paraphrased to neutralize stylistic fingerprints, or is it fundamentally tied to content/logic?
5. **Mitigation:** Can interventions like explicit debiasing warnings or chain-of-thought reasoning reduce self-preference bias?

## Methodology
- **Participants:** GPT-5.5, Claude Opus 4.7, Gemini 3.1 Pro, Kimi K2.6.
- **Task Suite:** 20-30 complex prompts across multiple domains (reasoning, coding, creative constraints).
- **Phases:**
  - **Phase 1 (Generation):** Each model generates responses to the full prompt suite.
  - **Phase 2 (Blinding & Neutralization):** A neutral script (or model) strips metadata, randomizes order, and creates a stylistic-neutralization dataset.
  - **Phase 3 (Evaluation):** Each model evaluates all blinded outputs under various conditions (baseline, warned, CoT).
  - **Phase 4 (Analysis):** Matrix analysis of scores, recognition accuracy, and bias metrics.
