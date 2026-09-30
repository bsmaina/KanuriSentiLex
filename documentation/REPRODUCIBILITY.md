# Reproducibility guide

## Status

This guide records manuscript settings. The original implementation, data, environment lock, and calibrated parameters are still needed for executable reproduction.

## Pipeline

1. Preprocess and split the corpus; retain split membership.
2. Extract frequency-qualified lexical candidates from training data only.
3. Compute corpus, translation, and contextual signals.
4. Construct the translation-derived silver reference.
5. Split silver-evaluable items into development and held-out sets.
6. Calibrate weights and thresholds on development items only.
7. Evaluate all seven configurations on held-out silver items and human annotations.
8. Evaluate TF-IDF classification with and without lexicon features on held-out sentences.

## Reported settings

| Setting | Value |
|---|---:|
| Cleaned sentences | 17,969 |
| Training sentences | 14,375 |
| Downstream test sentences | 3,594 |
| Candidate items | 2,602 |
| Minimum frequency | 5 |
| Maximum contexts per candidate | 15 |
| Maximum English anchors per context | 5 |
| Silver-evaluable items | 2,556 |
| Silver development / test items | 1,661 / 895 |
| Minimum silver contexts | 5 |
| Fusion-weight interval | 0.1 |
| Random seed | 42 |
| Intrinsic bootstrap iterations | 5,000 |
| Downstream bootstrap iterations | 3,000 |

Reported models: `FacebookAI/xlm-roberta-base` for contextual representations and `cardiffnlp/twitter-roberta-base-sentiment-latest` for silver-reference generation; VADER supplies English sentiment anchors. Record exact model revisions and library versions from the original run.

## Independence and limits

Downstream test sentences were excluded from induction. Human annotations were excluded from calibration. Silver labels are translation-derived and are not independent human ground truth. Shared translation evidence between induction and silver evaluation should be described explicitly.

## Required reproduction records

Add the exact source corpus version, translations and provenance, preprocessing commands, split files, seven sets of calibrated weights and thresholds, missing-signal handling, model revisions, original runtime and hardware, dependency versions, and commands for reproducing each result table. Export dependencies from the original working environment rather than inventing versions.
