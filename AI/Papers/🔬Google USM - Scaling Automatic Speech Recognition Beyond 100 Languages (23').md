---
aliases: GoogleUSM
cite: "Zhang, Yu, Wei Han, James Qin, Yongqiang Wang, Ankur Bapna, Zhehuai Chen, Nanxin Chen, et al. “Google USM: Scaling Automatic Speech Recognition Beyond 100 Languages.” arXiv, March 2, 2023. [https://doi.org/10.48550/arXiv.2303.01037](https://doi.org/10.48550/arXiv.2303.01037)."
---
#ASR #MassivelyMultilingual

# Datasets
| name     | # hours | # langs | content                                                                 |
| -------- | ------- | ------- | -------------- |
| YT-NTL-U | 12M     | 300+    | unlabeled YouTube audio                                                 |
| YT-SUP+  | 90k     | 73      | labeled YouTube audio?                                                  |
|          | 100k    | 1       | pseudo-labeled en-US audio generated by [[🔬Noisy Student Training|NST]] |
| Pub-U    | 429k    | 51      | unlabeled audio from public datasets                                    |
| Pub-S    | 20k     | 102     | labeled public data                                                                        |
| Web-NTL  |         | 1140        | text-only corpus with 28B sentences |

# Training
2B-param [[Conformer]] models
1. Unsupervised Pre-training ([[🔬BEST-RQ|BEST-RQ]]) with YT-NTL-U
2.  [[🔬Listen, Attend and Spell|🔬Listen, Attend and Spell]]
