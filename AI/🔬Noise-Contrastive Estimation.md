---
aliases: ["🔬NCE", "NCE", "Noise-Contrastive Estimation"]
cite: "Gutmann, Michael, and Aapo Hyvärinen. “Noise-Contrastive Estimation: A New Estimation Principle for Unnormalized Statistical Models.” In _Proceedings of the Thirteenth International Conference on Artificial Intelligence and Statistics_, 297–304. JMLR Workshop and Conference Proceedings, 2010. [https://proceedings.mlr.press/v9/gutmann10a.html](https://proceedings.mlr.press/v9/gutmann10a.html)."
---
#ML

[[GutmannM_2010_Noise-contrastive estimation.pdf|PDF Link]]

[Gentle Introduction to NCE](https://www.kdnuggets.com/2019/07/introduction-noise-contrastive-estimation.html)

# Problem with SSL Approaches like Word2Vec
- In word2vec, you minimize the [[Cross Entropy|Cross-Entropy Loss]] where _label = 1_ for the target word and _label = 0_ for all other words
- The loss function depends on **every output** in the network, as the loss is a sum over the entire vocabulary
- This makes **every network parameter** have a non-zero gradient, needing to be updated for every training example

# Negative Sampling
- Just pick a few _negative samples_, instead of summing over the entire vocabulary 
- Turns out to be a good enough approximation

# Noice Contrastive Estimation
A more theoretically founded version of Negative Sampling
- $P$: true distribution (e.g. of words)
- $Q$: _noise_ distribution, set to whatever distribution of our convenience
- Labels are invented by indicating whether (e.g. a word) comes from $P$ or $Q$
