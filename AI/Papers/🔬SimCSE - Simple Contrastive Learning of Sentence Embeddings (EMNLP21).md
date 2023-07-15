---
alias: 🔬SimCSE
cite: "Gao, Tianyu, Xingcheng Yao, and Danqi Chen. “SimCSE: Simple Contrastive Learning of Sentence Embeddings.” arXiv, May 18, 2022. [https://doi.org/10.48550/arXiv.2104.08821](https://doi.org/10.48550/arXiv.2104.08821)."
---

[[Contrastive Learning]]

Simple contrastive learning for sentence embeddings

# _Unsupervised_ SimCSE
- _Only_ use dropout as noise to apply to positive samples
- Simply use other sentences in the same mini-batch as negative samples
- Turns out this method significantly outperforms predicting next words or discrete data augmentation

# _Supervised_ SimCSE
- Use entailment pairs for positive samples
- Use contradiction pairs as hard negatives