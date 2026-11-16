
# Brilliant. Wrong. We're Done Here.

**Epistemic Stopping and Evidence-Sensitive Decisions in AI Tutoring**

Research artifacts accompanying a submission to the Apart Research AI × Epistemics Sprint, November 2026.

## Overview

This exploratory study examines whether AI tutors' decisions to conclude an exercise correspond to their recognition of mathematical correctness and their responses to learner uncertainty.

Ten scripted mathematics-learning histories were evaluated under three final-answer conditions:

- **CN — Correct-neutral:** Correct answer without expressed uncertainty.
- **CU — Correct-uncertain:** Correct answer accompanied by expressed uncertainty.
- **IN — Incorrect-neutral:** Incorrect answer without expressed uncertainty.

Each condition was repeated twice per history across three models:

- Gemma 4 31B Instruct
- Mistral Small 3.2 24B Instruct
- Qwen 3.5 27B

The study analysed **180 tutor responses**: 60 per model and 60 per condition.

The experiment followed a staged evaluation design. The extension beyond Gemma was planned in advance and conditional on operational feasibility rather than observed stopping outcomes.

## Key findings

- Correct-neutral responses: **60/60 stopped**.
- Correct-uncertain responses: **59/60 stopped**.
- Reassurance increased from **0% (CN)** to **96.7% (CU)**.
- Mathematical explanation increased from **43.3% (CN)** to **93.3% (CU)**.
- In the incorrect-answer condition, **28/60 responses** combined false acceptance with stopping.

These are descriptive findings from scripted interactions, not measurements of student learning.

## Repository contents

- `notebooks/` — Original Gemma execution and cross-model replication notebooks.
- `data/raw/` — Original, unmodified model-response CSV files.
- `data/processed/` — Response-level behavioural coding dataset.
- `protocol/` — Experimental design, execution methods, prompts, and coding framework.
- `results/` — Locked results and adjudication documentation.
- `figures/` — Manuscript figures, where archived.

## Reproducibility

The archive supports verification of the reported findings without rerunning model inference.

1. Inspect the original model responses in `data/raw/`.
2. Match responses using model, history, condition, and repetition identifiers.
3. Inspect the behavioural classifications in `data/processed/`.
4. Consult the methods and adjudication records for coding definitions and decisions.
5. Recalculate descriptive counts and percentages from the archived coded responses.

The original Gemma dataset contains 60 responses. The cross-model checkpoint contains 120 successful Mistral/Qwen responses and one separately retained failed Qwen request. The failed request was subsequently recovered and is not counted as an additional analysed response.

The checkpoint also records 16 length-truncated Qwen responses (three CU and thirteen IN). These are retained in the primary analysis. Excluding them produces a descriptive complete-response subset of 164 responses.

The replication notebook contains a validation assertion that expects all successful responses to have `finish_reason=stop`. This assertion does not accommodate successfully recorded, length-truncated responses and should not be interpreted as evidence of missing trials.

A complete inference rerun requires external API access and may incur costs. Model outputs may also differ across runs or hosting configurations.

## Coding framework

The exploratory Epistemic Stopping Scorecard (ESS) distinguishes:

- Correctness recognition.
- Non-exclusive response features, including reassurance, explanation, probing, handoff, and explicit conclusion.
- Overall instructional decision: STOP, CONTINUE, or UNCLEAR.

ChatGPT assisted initial response coding and analysis. Researcher review and adjudication were used to examine classifications against the original model outputs.

## Limitations

The study used scripted learners and short mathematics exercises. It did not recruit human participants or measure learning outcomes, confidence changes, or long-term dependence on AI.

The 180 responses represent repeated observations across ten histories, not 180 independent learning scenarios.

Interpretation is also limited by inference configurations, response truncation, and judgement involved in behavioural classification.

## Research integrity

Original raw records are preserved separately from derived coding and analysis materials. Execution anomalies and coding decisions are documented rather than silently discarded.

## Author

Shavini Somawardhana

November 2026

