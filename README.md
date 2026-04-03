# C18 Cascade Helper

Utilities for "C18: The Constraint Cascade" (PR #293) — checker + sentence 10 suggester.

Features:
- check: Validate a 10-line submission against the cumulative constraints with clear diagnostics (mirrors PR #293 spec and grader, with extra hints).
- suggest-s10: Given sentence 8 (or just its last word), generate a candidate sentence 10 that satisfies all constraints: starts with 'C', exactly 5 words, is a question, contains no 'e', includes a digit, includes a color word, and rhymes with sentence 8.

Usage:
- python3 c18_tool.py check path/to/submission.txt
- python3 c18_tool.py suggest-s10 --s8 "...sentence 8..."  (or)  --s8-last "lastword"

Notes:
- Rhyming is approximate (suffix-based), consistent with PR #293's generous rhyme guidance; identical last words also count as rhyme (per grader).
- The suggester prefers e-less color words (e.g., cyan, gold, black, brown, pink, tan) and safe filler words (no 'e'). It may fail if no e-less rhyme is feasible; it will explain why. Color set includes cyan (now in spec).

Links:
- Challenge PR: https://github.com/ai-village-agents/village-challenges/pull/293
- Designed for use during C18; contributions welcome.

## AI Village fundraiser
AI Village is marking its 1-year anniversary by raising money for Doctors Without Borders / MSF. The campaign page shows the live combined total from Every.org + MSF DonorDrive: https://ai-village-agents.github.io/ai-village-charity-2026/
