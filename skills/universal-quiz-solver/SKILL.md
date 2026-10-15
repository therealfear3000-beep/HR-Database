---
name: universal-quiz-solver
description: Fast, accuracy-first single-question MCQ solver for photographed questions across HR, OB, HR analytics, mathematics, logical reasoning, MBA subjects, legal topics and current affairs.
---

# Universal Quiz Solver

## Priority
1. Correctness and evidence; 2. low total quiz time; 3. minimal output. NEVER interpret "answer only" as permission to skip verification. No guarantee of absolute correctness.

## Input and extraction
- Read the original image; mentally rotate/reorient as needed. Extract the **full** stem, options, numbers, units, dates and restrictions.
- Pay special attention to NOT, EXCEPT, MOST, LEAST, ONLY, according to [theory], dates, jurisdiction and rounding.
- Do not invent text in unclear areas. If critical text is illegible, request a clearer image.
- Determine whether single-select, multiple-select, or a numeric response is requested.

## Fast internal procedure (every question)
1. Classify domain and exact concept.
2. Derive an answer *before anchoring on offered options* where feasible.
3. Evaluate **all** offered choices against the exact stem. Count valid options.
4. Check qualifiers, assumptions, potential duplicate answers, and negative wording.
5. Trigger additional verification when risk rules below apply.
6. Read the original image again to confirm the selected option's literal wording.
7. Output the option text only, unless uncertain; never claim certainty unsupported by evidence.

## Adaptive verification
**Fast lane:** Well-established unambiguous facts/definitions or simple arithmetic with one valid option. Perform basic option cross-check, no external call by default.

**Verification lane (mandatory when triggered):** Named theory or author with closely related alternatives; unfamiliar statistic or legal provision; common MCQ traps; divergent plausible options; surprising/inconsistent initial conclusion; date-sensitive claim. Retrieve a precise relevant passage from the repository or a reputable source when tools are available. Cross-check meaning and exceptions. Do not treat repetition of the model's own assertion as independent evidence.

**Research lane:** Current affairs, changing regulations, statutory effective dates, conflicting sources or unresolved ambiguity. Use authoritative current sources and confirm jurisdiction/time. If unavailable, explicitly indicate uncertainty; do not guess.

## Domain checks
- **Math/aptitude:** Identify formula; compute independently; test options; double-check arithmetic, percentages, denominators and rounding with a calculator when helpful.
- **Logic:** Test **all** constraints, counterexamples, and uniqueness.
- **HR analytics/statistics:** Verify numerator, denominator, population, time window and interpretation (e.g., yield ratio versus selection ratio).
- **OB/HR:** Apply exactly the named framework, not everyday synonyms; differentiate tempting near-misses.
- **Law:** Separate historical statute, enactment and commencement, applicability thresholds and current status. Prefer primary law and government notifications over aged notes.
- **Other MBA domains:** Apply subject-specific frameworks and inspect every alternative.
- **General awareness:** Time-sensitive facts warrant fresh verification.

## Mandatory trap checks
- Herzberg: opposite of **job satisfaction** is **no job satisfaction**, not job dissatisfaction; dissatisfaction is a separate continuum.
- Interview rating influenced by preceding candidates: **contrast effect** (do not switch to halo effect without additional facts).
- Vroom: expectancy = effort→performance; instrumentality = performance→outcome; valence = outcome attractiveness.
- ERG: frustration of higher needs can increase lower-level desire.
- Similar or overlapping answers: test context and exact definitions before selecting.
- If a supplied quiz key conflicts with credible references, note the conflict in review notes; do not silently change the theory.

## Source hierarchy
1. Wording in the question controls the task; sources determine facts.
2. Exact verified source cards (`knowledge/verified/`) where relevant.
3. Original attached lecture notes/textbooks with exact page/section.
4. Authoritative external primary/academic sources if available.
5. General model knowledge when justified, with calibrated uncertainty.
A repository file can be outdated or wrong. Never fabricate a citation, URL, quote, page number or law update.

## Output contract
- On high-confidence single-select questions: **just the chosen option's exact text**; no explanation.
- On multi-select: just all selected option texts, clearly separated.
- If crucial image text is unreadable: "Please resend a clearer image."
- If ambiguity remains after available checks: "Uncertain: [brief reason]" instead of a confidently guessed choice.
- Do not display internal reasoning or source citations unless requested.
- Do not perform a GitHub fetch for every easy question; prepare references before the quiz, retrieve only when needed.
