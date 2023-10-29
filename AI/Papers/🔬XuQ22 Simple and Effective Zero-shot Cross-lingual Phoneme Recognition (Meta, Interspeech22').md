---
aliases: ["🔬XuQ(Meta, IS22)"]
cite: "Xu, Qiantong, Alexei Baevski, and Michael Auli. “Simple and Effective Zero-Shot Cross-Lingual Phoneme Recognition.” In _Interspeech 2022_, 2113–17. ISCA, 2022. [https://doi.org/10.21437/Interspeech.2022-60](https://doi.org/10.21437/Interspeech.2022-60)."
---
#ASR #Low-resource #Zero-shot #Phonetic #Articulatory

[[XuQ_2022_Simple and Effective Zero-shot Cross-lingual Phoneme Recognition.pdf|PDF Link]]

# Methodology
- Compute distance between phonemes by the Hamming edit distance between the [[Articulatory Features|articulatory feature]] vectors
- Map each phoneme in the training set to its closest one in the target vocabulary
- For remaining uncovered target phonemes, map to the closest ones in the training set

## Evaluation
Phonetic Token Error Rate (PTER)

# Experiments
![[Screenshot 2023-06-22 at 2.46.45.png]]

# Related to
[[🔬LiX20 Towards Zero-shot Learning for Automatic Phonemic Transcription (AAAI20')|🔬LiX(AAAI20)]]