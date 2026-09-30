# Human annotation protocol

## Procedure reported in the manuscript

A 400-item subset was selected to represent corpus-derived polarity strata. Three native Kanuri speakers annotated each lexical item independently, assigning polarity and a confidence score on a five-point scale. Sheets displayed only item identifiers, Kanuri words, and empty polarity and confidence fields.

Annotators were blinded to automatic labels, sentiment scores, silver labels, sampling strata, and other annotators' judgments. Majority vote was used for non-unanimous items. Human labels were reserved for evaluation and were not used for candidate selection, scoring, calibration, or model selection.

The manuscript reports 391 unanimous items, Fleiss' kappa 0.9762, pairwise Cohen's kappa 0.9683–0.9881, and mean confidence 4.83/5.

## Recommended guidance for future annotation

These definitions are proposed guidance; they are not asserted to be the verbatim instructions used in the original study.

- **Positive:** a word with a favourable, approving, or desirable affective meaning.
- **Negative:** a word with an unfavourable, disapproving, or undesirable affective meaning.
- **Neutral:** a understood word without a clear positive or negative lexical orientation.

For an unknown word, record uncertainty separately rather than automatically assigning neutral. For polysemous or context-dependent items, record ambiguity and any relevant explanation. Use a documented confidence scale; for example, 1 = very low and 5 = very high confidence.

## Details to recover before release

Document the actual sampling algorithm, stratum definitions, counts, seed, sampling probabilities or inclusion criteria, original label definitions, confidence anchors, handling of unknown and ambiguous words, any all-different-label cases, annotator eligibility, and consent arrangements. Attach the original instructions if available. Do not retroactively present recommended guidance as the historical protocol.
