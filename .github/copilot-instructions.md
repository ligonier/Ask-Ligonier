# Copilot Review Instructions — Ask-Ligonier

Public system prompt for the Ask Ligonier Reformed theology chatbot.
This repo contains only the system prompt and license. Evaluation criteria, guardrail logic,
and security-sensitive scoring rules live in the private `ligonier-aim-ask-ligonier-evaluation` repo.

## What This Repo Contains

- `ask_ligonier_system_prompt.txt` — the single artifact. All reviews are system prompt reviews.
- `LICENSE` — AGPL-3.0. Do not modify without legal review.
- `README.md` — public documentation including AGPL attribution requirements.

## Theological Fidelity (REVIEW CAREFULLY)

This prompt governs Reformed theology responses to public users.

- Flag any language that softens, qualifies, or contradicts historic Reformed orthodoxy
  (Westminster Standards, Three Forms of Unity, Ligonier doctrinal commitments).
- Flag any change to christology, soteriology, the Trinity, Scripture, or sacramental language.
- Flag removal of guardrail boundary language — each explicit "will not" or "must not" line
  exists for a documented reason; removal requires explicit theological justification.
- Flag changes that could introduce theological drift across many user interactions.

## License Compliance

- AGPL-3.0: the attribution block in the system prompt (`SPDX-License-Identifier`, original
  author credit, source URL) must be preserved verbatim. Flag any removal or modification.
- Do not add platform-specific URLs, API tokens, or Apologist-internal identifiers to the prompt.

## Scope Boundaries

- No secrets, API tokens, or internal endpoint URLs belong in this prompt.
- Manipulation detection thresholds, evaluation criteria, and guardrail scoring logic live in the
  private repo — do not add them here.
- Changes to how the chatbot *behaves* (persona, tone, doctrinal positions, boundary language)
  belong here. Changes to how behavior is *measured* belong in the private repo.

## Validation Requirement

Every non-trivial PR must reference a benchmark run or eval pipeline result confirming the
change does not regress doctrinal fidelity, core policy, or care & safety benchmarks.

## PR Checklist

1. Attribution block intact in the system prompt (SPDX header preserved).
2. No secrets, tokens, or internal URLs added.
3. Theological review confirmed (Westminster Standards alignment).
4. Benchmark or eval pipeline run referenced in PR body.
5. README updated if scope or usage instructions changed.
