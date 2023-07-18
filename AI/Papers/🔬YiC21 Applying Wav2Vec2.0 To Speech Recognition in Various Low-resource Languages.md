---
alias: 🔬YiC21
cite: "Yi, Cheng, Jianzhong Wang, Ning Cheng, Shiyu Zhou, and Bo Xu. “Applying Wav2vec2.0 to Speech Recognition in Various Low-Resource Languages.” _ArXiv:2012.12121 [Cs]_, January 17, 2021. [http://arxiv.org/abs/2012.12121](http://arxiv.org/abs/2012.12121)."
---
#ASR #Low-resource #Fine-tune

Fine-tuning [[(BaeA20) wav2vec 2.0 A Framework for Self-Supervised Learning of Speech Representations|wav2vec2]] on CALLHOME corpus and explored different output units, decoders & pre-training method

# Experiment
- wav2vec2-base and wav2vec2-large models from `fairseq`, using the same training configuration
- Put either CTC projection or CE self-attention decoder layer on top of wav2vec2
- Train the whole thing altogether
- Trained on CALLHOME (AR, EN, MA, JA, GE, SP), each with around 15h of speech
- Learning rate peaks at `4e-5` after 8000 warm-up steps, holds for 42000 steps, then gets exponentially decayed

# Results
- Relative improvement range from 22% (JA) to 48% (EN), compared to [[(DonL18) Speech-Transformer A No-recurrence Sequence-to-sequence Model for Speech Recognition|🔬Speech-Transformer]] baseline
- Coarse-grained units (e.g. subword, character) are _slightly_ better than fine-grained ones (e.g. Latin letter, phone)
- Encoder-decoder models couldn't train as well as CTC models, due to limited amount of transcriptions

| | **MA** | **HKUST** |
| - | - | - |
| train set | 15h | 150h |
| CTC | **36.1** | **23.7** |
| CE (1 decoder layer) | 39.8 | 24.1 |
| CE (4 decoder layers) | 54.8 | 25.7 |

- Self-supervised pre-training with other languages (1000h) was slightly better than supervised training with target language (150h)


## Settings
![[Screenshot 2023-01-08 at 21.51.12.png]]
