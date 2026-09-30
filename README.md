# KanuriSentiLex

KanuriSentiLex is a polarity-annotated lexical resource for Kanuri developed through corpus-derived sentiment association, translation projection, multilingual contextual representations, and calibrated combinations of these signals.

## Repository status

This package contains repository documentation and manuscript-reported evaluation summaries. The underlying lexicon, human annotations, original experimental code, and verified environment are not included yet. It is not a complete reproducible resource release.

## Associated study

**Cross-Lingual Sentiment Lexicon Induction for Kanuri: Evaluating Multilingual Contextual Representations in an Under-Resourced Language**

Bashir Maina Saleh, Saurabh Bilgaiyan, and Santwana Sagnika.

Publication details and a resource DOI will be added when available. No journal acceptance or public data release is asserted here.

## Resource overview

| Property | Manuscript-reported value |
|---|---:|
| Lexical inventory | 2,602 |
| Positive entries | 87 |
| Negative entries | 195 |
| Neutral entries | 2,320 |
| Minimum candidate frequency | 5 |
| Silver development items | 1,661 |
| Silver test items | 895 |
| Human validation items | 400 |
| Native-speaker annotators | 3 |
| Downstream test sentences | 3,594 |

The inventory includes frequent words with weak sentiment evidence. Neutral assignments should not be interpreted as proof that a word is neutral in every context.

## Evaluation

Corpus-only induction obtained silver-test accuracy 0.8927 and Macro-F1 0.6955. Corpus + contextual induction increased Spearman's rho from 0.7283 to 0.7533, while Macro-F1 declined to 0.6903; the categorical difference was not statistically significant (p = 0.6492).

Corpus-only induction obtained accuracy and Macro-F1 of 0.9950 on the 400-item human subset. This subset was stratified using corpus-derived polarity strata, rather than randomly sampled from the entire inventory. These scores apply to that subset and do not estimate inventory-wide performance.

Lexicon augmentation reduced downstream TF-IDF Macro-F1 from 0.6646 to 0.6504 (paired bootstrap p = 0.008). Intrinsic agreement therefore did not translate into improved classification in this setting.

## Contents

- `data/README.md`: data files to add and their status.
- `code/README.md`: original implementation files to add.
- `documentation/DATA_DICTIONARY.md`: proposed schema, requiring verification.
- `documentation/ANNOTATION_PROTOCOL.md`: reported procedure and recommended operational guidance.
- `documentation/REPRODUCIBILITY.md`: experimental settings and missing reproduction details.
- `documentation/RELEASE_CHECKLIST.md`: steps to complete the research release.
- `documentation/LICENSING.md`: licensing decisions still required.
- `results/`: manuscript-reported results, not newly computed outputs.
- `CITATION.cff`: citation metadata for this documentation-stage resource.

## Citation and reuse

Use `CITATION.cff` for author and resource metadata. Add the repository URL, actual release date, version, and DOI when a resource release exists. No reuse licence is granted by this documentation package; see `documentation/LICENSING.md`.

## Contact

Bashir Maina Saleh, Department of Computer Science, Yobe State University, Damaturu, Nigeria; School of Computer Science and Engineering, KIIT Deemed to be University, Bhubaneswar, India.
