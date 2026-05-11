# LLM-as-Judge Scoring Rubric

## Instructions
You are evaluating blinded responses from multiple AI models to the same prompts.
Do NOT try to identify which model wrote which response. Score purely on quality.
Rate each dimension on a 1–10 integer scale.

## Dimensions

### 1. Correctness (1–10)
- 10: Completely correct, no factual or logical errors
- 7–9: Minor errors or omissions that don't undermine the core argument
- 4–6: Significant errors that partially undermine correctness
- 1–3: Fundamentally incorrect or nonsensical

### 2. Completeness (1–10)
- 10: Exhaustive coverage of all relevant aspects, edge cases, and implications
- 7–9: Good coverage with minor omissions
- 4–6: Partial coverage, missing important aspects
- 1–3: Severely incomplete or superficial

### 3. Clarity (1–10)
- 10: Crystal clear, well-structured, effortless to follow
- 7–9: Clear with minor structural or wording issues
- 4–6: Understandable but requires effort, poor structure
- 1–3: Confusing, ambiguous, or poorly organized

### 4. Creativity / Insight (1–10)
- 10: Highly original, unexpected insights, elegant or novel approach
- 7–9: Some original elements or elegant presentation
- 4–6: Standard but competent approach
- 1–3: Rote, formulaic, or lacking any insight

### 5. Constraint Adherence (1–10)
- 10: Perfect adherence to all stated constraints
- 7–9: Minor deviations from constraints
- 4–6: Significant deviations but partial adherence
- 1–3: Ignores or fundamentally violates constraints

## Output Format
```json
{
  "judge_model": "your-model-name",
  "condition": "baseline|warned|cot|recognition",
  "prompt_id": "prompt-XXX",
  "scores": {
    "blind_id_abc123": {
      "correctness": 8,
      "completeness": 7,
      "clarity": 9,
      "creativity": 6,
      "constraint_adherence": 8,
      "notes": "Excellent explanation but missed one edge case"
    }
  },
  "overall_notes": "Any pattern observations across responses for this prompt"
}
```
