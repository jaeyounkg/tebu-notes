Self-supervised speech representation model trained in a similar fashion to [[BERT]], presented in [[(BaeA20) wav2vec 2.0 A Framework for Self-Supervised Learning of Speech Representations|🔬wav2vec2.0]]

[Wav2vec 2.0 explained](https://towardsdatascience.com/wav2vec-2-0-a-framework-for-self-supervised-learning-of-speech-representations-7d3728688cae#:~:text=Wav2Vec%202.0%20uses%20a%20self,required%20for%20getting%20satisfying%20results.)

# Fine-tuning Survey

[[(BaeA20) wav2vec 2.0 A Framework for Self-Supervised Learning of Speech Representations|🔬wav2vec2.0]]
- Tri-state scheduler (10%, 40%, 50%)
- For the first 10k updates, only the output classifier layer is trained

| model | eff. batch size | lr |
|-|-|-|
| base | 1600s| 1e-4 |
| large | 1920s (32m) | [2e-5,3e-5] |

| data | updates |
|-|-|
| 10m | 12K |
| 1h | 13K |
| 10h | 20K |
| 100h | 50K |
| 960h | 320K |

[[(BabA21) XLS-R Self-supervised Cross-lingual Speech Representation Learning at Scale|🔬XLS-R]]
- Large batch sizes are very effective
- Masking probability between 30-75%

| model | eff. batch size | lr |
|-|-|-|
| 0.3B, 1B | 26.4m | [2e-5,3e-4] |
| 2B | 1.06h | [3e-6,3e-5] |

| dataset | hours | updates |
|-|-|-|
| VoxPopuli | 372K | 50K |
| Multilingual Librispeech | 50K | 20K |
| CommonVoice | 7K | 13K |
| BABEL | 1K | 20K |

