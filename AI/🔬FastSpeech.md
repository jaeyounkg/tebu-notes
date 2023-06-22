---
aliases: FastSpeech
cite: "Ren, Yi, Yangjun Ruan, Xu Tan, Tao Qin, Sheng Zhao, Zhou Zhao, and Tie-Yan Liu. “FastSpeech: Fast, Robust and Controllable Text to Speech.” arXiv, November 20, 2019. [https://doi.org/10.48550/arXiv.1905.09263](https://doi.org/10.48550/arXiv.1905.09263)."
---
#TTS

[[RenY_2019_FastSpeech.pdf|PDF Link]]

E2E non-autoregressive (phonemes to [[Mel Spectrogram]]s) TTS model introduced in 2019
- Inference is 38x faster than autoregressive TransformerTTS, SoTA model at the time
- Performance almost equivalent to TransformerTTS

# Architecture
![[Screenshot 2023-06-15 at 0.50.43.png]]
## Phoneme Duration Predictor
- Trained with [[Mean Squared Error|MSE]] loss
- Length is predicted in the logarithmic domain, making them more Gaussian and easier to train
- Only used in inference, as we can directly use the phoneme duration extracted from an autoregressive teacher model in training

### "Ground-truth" phoneme durations
Extracted from an autoregressive teacher TTS model
