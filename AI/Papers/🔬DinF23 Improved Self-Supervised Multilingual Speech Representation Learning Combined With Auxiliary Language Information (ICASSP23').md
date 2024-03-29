---
aliases:
  - 🔬DinF(ICSP23)
---
#ASR #Low-resource #Adversarial #Adapter

Try 4 different language-info-augmented approaches for multilingual [[🔬XLS-R - Self-supervised Cross-lingual Speech Representation Learning at Scale|XLSR]] pretraining (**XLSR is pretrained from scratch**)
- Language-[[Adversarial Learning|adversarial]] (LA): use [[Gradient Reversal Layer]]
- Language embeddings (LE): $\tilde{h}_i^l = h_i^l + embedding(l)$, embeddings are trainable params
- Language specific adapters (LSA)
- [[🔬PhaN21 Efficient Weight Factorization for Multilingual Speech Recognition (Interspeech21')|Language specific adaptive weight]] (LSAW)

Transformer encoder in XLSR is replaced by Conformer & filterbank features are used

# Conclusion
- Language-adversarial training _might_ be helpful for ASR performance (when pretraining data is not so large)
- Adapters are significantly more effective

# Experiments & Results
Used internal datasets. Pre-training ran on 32 A100 GPUs for 400k steps.

![[Pasted image 20230715220602.png]]

# Findings
- Language-[[Adversarial Learning|adversarial]] training works best when inserted into lower-level layer (best at 24.66% at 4th layer, worst at 25.98% at 16th)
- Language embeddings work best when inserted into the lowest (0th) layer (+ a bit of orthogonal constraint), though the difference is marginal