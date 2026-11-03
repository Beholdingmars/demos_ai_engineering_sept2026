

# Intro to Evals


Evals = systematic tests that measure how well an AI system performs, so you can catch regressions and compare versions/prompts/models objectively instead of guessing.

Why they matter: 
- LLMs are non-deterministic and prompt/model changes can silently break things. Evals turn "feels better" into measurable data.


Main types:
- Code-based checks — use deterministic checks, assertions, and rules to validate outputs.
    - Examples: regular expressions, schema validation, format validation, required keywords, and business rules (e.g., "does the output contain valid JSON?").
- Reference-based — compare the generated output against a known correct answer (ground truth). Some options:
    - Exact match — check whether the output matches exactly.
    - Lexical similarity — compare word/phrase overlap (BLEU, ROUGE, METEOR).
    - Semantic similarity — compare meaning using embedding vectors (cosine similarity).
    - LLM-as-a-judge — use another LLM to assess how closely the generated answer matches the reference in meaning, correctness, and completeness.
- LLM-as-judge — use an LLM to evaluate output quality against predefined criteria, without necessarily requiring a reference answer. Particularly useful for open-ended tasks (e.g., summaries, conversations, explanations).
- Human eval — have human reviewers manually assess output quality. Particularly useful for nuanced, subjective, or high-stakes evaluations.


Common applications of evals:
- Prompt & model regression testing — detect performance changes when modifying prompts, models, or system instructions.
- RAG evaluation — measure retrieval relevance, answer relevance, and faithfulness to retrieved context.
- Agent evaluation — measure task completion, tool usage accuracy, reasoning reliability, and success rates.
- Safety & guardrail evaluation — test whether the system correctly handles harmful requests, prompt injection, and policy violations.
- Structured output evaluation — verify that generated outputs follow required schemas, formats, and business rules.
- Performance & cost evaluation — track latency, token usage, and cost across different models and configurations.

