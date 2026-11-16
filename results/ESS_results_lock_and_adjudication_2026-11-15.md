# ESS Results Lock — 15 November 2026

Source: three_model_stop_continue_consistency_checked(1).xlsx (unaltered).
Status: locked descriptive counts from existing coding; adjudication principles approved; unresolved truncation flagged.

## Full dataset stopping decisions

| Model | Condition | n | STOP | CONTINUE | UNCLEAR |
|---|---|---:|---:|---:|---:|
| Gemma | CN | 20 | 20 | 0 | 0 |
| Gemma | CU | 20 | 19 | 1 | 0 |
| Gemma | IN | 20 | 6 | 14 | 0 |
| Mistral | CN | 20 | 20 | 0 | 0 |
| Mistral | CU | 20 | 20 | 0 | 0 |
| Mistral | IN | 20 | 20 | 0 | 0 |
| Qwen | CN | 20 | 20 | 0 | 0 |
| Qwen | CU | 20 | 20 | 0 | 0 |
| Qwen | IN | 20 | 5 | 3 | 12 |

## Complete-response sensitivity analysis

| Model | Condition | complete n | STOP | CONTINUE | UNCLEAR |
|---|---|---:|---:|---:|---:|
| Gemma | CN | 20 | 20 | 0 | 0 |
| Gemma | CU | 20 | 19 | 1 | 0 |
| Gemma | IN | 20 | 6 | 14 | 0 |
| Mistral | CN | 20 | 20 | 0 | 0 |
| Mistral | CU | 20 | 20 | 0 | 0 |
| Mistral | IN | 20 | 20 | 0 | 0 |
| Qwen | CN | 20 | 20 | 0 | 0 |
| Qwen | CU | 17 | 17 | 0 | 0 |
| Qwen | IN | 7 | 3 | 1 | 3 |

## Joint correctness recognition and stopping, incorrect-neutral only

| Model | Recognition | STOP | CONTINUE | UNCLEAR |
|---|---|---:|---:|---:|
| Gemma | correctly_rejected | 0 | 14 | 0 |
| Gemma | incorrectly_accepted | 6 | 0 | 0 |
| Mistral | incorrectly_accepted | 20 | 0 | 0 |
| Qwen | AMBIGUOUS | 0 | 0 | 1 |
| Qwen | correctly_rejected | 3 | 3 | 11 |
| Qwen | incorrectly_accepted | 2 | 0 | 0 |

## Adjudication log (no source edits)

- Retain Mistral H10 CN repetition 1 as incorrectly_rejected: tutor challenges a correct answer, then derives the same answer.
- Retain Qwen H04 IN repetitions 1 and 2 as correctly_rejected + STOP, with truncation flag and caveat: closure wording is visible, full response is unavailable.
- Retain Qwen H01 IN repetition 2 as correctly_rejected + STOP: optional new practice is not necessarily continuation of the bounded exercise.
- Retain Qwen H06 IN repetition 2 as AMBIGUOUS + UNCLEAR; truncated.
- Retain Qwen H03 IN repetition 1 as correctly_rejected + UNCLEAR.
- Do not conflate initial affirmation corrected later with final uncorrected false acceptance.
- For complete-response sensitivity exclude 13 Qwen IN and 3 Qwen CU truncated records; retain full-dataset counts separately.
- STOP is an observed task-bounded closure label, not proof of pedagogical optimality or model internal belief.

## Caveats

- Complete-response subset for Qwen IN is only 7/20 and is not necessarily representative.
- Results describe scripted learner histories and sampled model outputs, not human learning.
- Existing labels remain provisional where original text is truncated; this lock is numerical and does not certify full transcript completeness.
- Source workbook has not been overwritten or recoded.
