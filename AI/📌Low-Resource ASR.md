# 🔬 Using Articulatory Features
- [[🔬FenS23 Language-Universal Phonetic Representation in Multilingual Speech Pretraining for Low-Resource Speech Recognition (Interspeech23')|🔬FenS(IS23)]] Multilingual HuBERT pretraining with IPA labels
- [[🔬ZhuC21 Multilingual and Cross-lingual Speech Recognition Using Phonological Vector-based Phone Embeddings (ASRU21')|🔬ZhuC(ASRU21)]] Gave a fancy name to using $sim(p_i, h_t)$ to compute final logits
	- $p_i$: $i$th phoneme embedding
	- $h_t$: model output at time $t$
- [[🔬XuQ22 Simple and Effective Zero-shot Cross-lingual Phoneme Recognition (Meta, Interspeech22')|🔬XuQ(IS22)]] Zero-shot, use Hamming distance between [[Articulatory Features|AF]] vectors
- [[🔬LiX20 Towards Zero-shot Learning for Automatic Phonemic Transcription (AAAI20')|🔬LiX(AAAI20)]] Zero-shot, use frozen linear transformation from attributes to phonemes
- [[🔬MulM16 Towards Improving Low-Resource Speech Recognition Using Articulatory and Language Features|🔬MüllerM16]] Using [[Articulatory Features|AF]] & language feature vectors

## Resources
- [[🔬PanPhon - A Resource for Mapping IPA Segments to Articulatory Feature Vectors|🔬PanPhon]] IPA symbol -> [[Articulatory Features|AF]] mappings

# 🔬 Using Adversarial Learning
- [[🔬DinF23 Improved Self-Supervised Multilingual Speech Representation Learning Combined With Auxiliary Language Information (ICASSP23')|🔬DinF(ICSP23)]] Language-adversarial pre-training based on [[🔬XLS-R - Self-supervised Cross-lingual Speech Representation Learning at Scale|XLSR]]
- [[🔬YiJ19 Language-Adversarial Transfer Learning for Low-Resource Speech Recognition|🔬YiJ19]] Language-adversarial pre-training (BiLSTM)
- [[🔬AdaO19 Massively Multilingual Adversarial Speech Recognition (NAACL19')|🔬AdaO(NA19)]] Massively multilingual + language-adversarial + context-independent phoneme prediction pretraining

# 🔬 Using Adaptive Tuning
- [[🔬DinF23 Improved Self-Supervised Multilingual Speech Representation Learning Combined With Auxiliary Language Information (ICASSP23')|🔬DinF(ICSP23)]]

# 🔬 Using Meta-Learning
- [[🔬HsuJ20 Meta Learning for End-to-end Low-Resource Speech Recognition (ICASSP20')|🔬HsuJ(ICSP20)]]