---
alias: 🔬ZhuC(ASRU21)
---

# Summary
- Compute _phonetic embedding vectors_ $e_i$ (for phone $i$) from _phonological-vectors_ $p_i\in \mathbb{R}^{51}$ (# of phonological features to be considered)
	- Linear: $e_i = Ap_i \in \mathbb{R}^h$
	- Non-linear: $e_i = A_2 \sigma (A_1 p_i) \in \mathbb{R}^h$
- Compute the final logits as $z_{t,i} = e_i^T h_t$ (omitting the bias term)
- Can be regarded as **cosine similarity** between each phonetic embedding vector and hidden output vector

💬 honestly a superset of my Interspeech 2023 paper lol
