# Data dictionary

## Status

The actual dataset was not supplied with this documentation request. The following is a proposed release schema, not a verified description of existing columns. Update it against the real files before releasing data.

| Proposed field | Meaning | Verification needed |
|---|---|---|
| `word` | Kanuri lexical item | Exact spelling and normalization |
| `frequency` | Occurrences in the induction training corpus | Token versus context count |
| `corpus_score` | Corpus-derived sentiment association | Formula and range |
| `translation_score` | Translation-projected sentiment evidence | Formula, range, missing evidence |
| `contextual_score` | Contextual cross-lingual sentiment evidence | Formula, range, missing evidence |
| `final_score` | Score from the released calibrated configuration | Configuration, weights, scale |
| `polarity` | Positive, neutral, or negative assignment | Actual label encoding and thresholds |

Retain UTF-8 spelling. Record delimiters and missing-value conventions. Missing evidence must be distinguished from a measured zero score. Do not infer score bounds from field names.

## Human-reference schema

Suggested fields are `item_id`, `word`, and `gold_polarity`. Where sharing is permitted, add pseudonymous individual labels and confidence ratings. Record aggregation and tie handling. Verify these fields against the actual annotation sheets before describing them as released columns.

The manuscript reports 86 positive, 193 neutral, and 121 negative human-reference items.
