# Experiment

## Settings
![[Screenshot 2023-01-08 at 21.51.12.png]]


## Results
Table 1. Performance on CALLHOME corpus with 6 languages
The criteria is WER(%) on each test set (CER(%) for MA and JA).

| Models | AR | EN | MA | JA | GE | SP |
|--------|----|----|----|----|----|----|
| mlstm-residual [2] | 56.47 | 43.93 | 45.85 | 50.13 | 51.75 | 53.38 |
| Speech-Transformer [3] | 48.35 | 33.77 | 37.62 | 36.99 | 44.98 | 51.54 |
| wav2vec2.0-base + ctc (letter/phone) + LM decode | 40.73 | 21.83 | 33.57 | 38.24 | 29.88 | 45.92 |
| wav2vec2.0-base + ctc (subword/char) + LM decode | 50.67 | 24.93 | 36.06 | 37.70 | 41.77 | 52.53 |
| wav2vec2.0-large + ctc (letter/char) + LM decode | 42.44 | 17.65 | 28.75 | 28.69 | 40.27 | 47.36 |
| relative improvement | 26.3% | 52.4% | 25.1% | 23.4% | 42.9% | 24.1% |

2.3. Adaptation to ASR Tasks
