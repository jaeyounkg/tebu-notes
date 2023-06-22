---
aliases: 🔬LiX(AAAI20)
cite: "Li, Xinjian, Siddharth Dalmia, David Mortensen, Juncheng Li, Alan Black, and Florian Metze. “Towards Zero-Shot Learning for Automatic Phonemic Transcription.” _Proceedings of the AAAI Conference on Artificial Intelligence_ 34, no. 05 (April 3, 2020): 8261–68. [https://doi.org/10.1609/aaai.v34i05.6341](https://doi.org/10.1609/aaai.v34i05.6341)."
---
#ASR  #Low-resource 

[[LiX_2020_Towards Zero-Shot Learning for Automatic Phonemic Transcription.pdf|PDF Link]]

Improving zero-shot ASR (target: phones) performance when no target speech/text corpus is available

# Methodology
- Consider [[Articulatory Features|articulatory attribute]] assignment of all IPA "phonemes"
- Use X-SAMPA representations instead of raw IPA

## Articulatory Attribute Modeling
- $A_{phone} :=$ Union of the consonants & vowels & diacritics attributes (plus $\{blank\}$)
	- Consonant attributes: manner & place of articulation
	- Vowel attributes: *front*, *back*, *rounded*, *unrounded*, etc
		- Allowing for binary encoding instead of ternary
- $P_{base} :=$ All base symbols of IPA
- $P_{xsampa} :=$ All "phonemes" of IPA(X-SAMPA), subset of which is used as target phoneme inventory

### Attribute Assignment of IPA "phonemes"
- First construct assignment $f\vert _{P_{base}} : P_{base} \rightarrow 2^{A_{phone}}$ by hand
- Then $f : P_{xsampa} \rightarrow 2^{A_{phone}}$ can be assigned algorithmically by putting different symbols together
	- e.g. */ts_>/* is recognized as */ts/* and *ejective*

## Signature Matrix
$$
S \in \{0,1\}^{z\times a}
$$
where $z$ is # phonemes, $a$ is # attributes
- The $(i, j)$ cell is 1 if the $i$-th phoneme has been assigned to the $j$-th attribute.
- This matrix is fixed and does not get trained

## Model Overview
![[Screenshot 2023-06-22 at 1.38.40.png]]

## Zero-shot Inference
For a new target language with $z'$ phonemes, create and use a new signature matrix $S' \in \{0,1\}^{z'\times a}$

# Experiments
- Training set comes from 17 corpora in **13** languages
	- English, Mandarin, **Italian**, Dutch, Turkish, Cebuano, ...
- Test set comes from corpora in **7** other languages
	- German, Russian, **Spanish**...

# Results
![[Screenshot 2023-06-22 at 2.19.58.png]]

![[Screenshot 2023-06-22 at 2.21.23.png]]

- Substitution error rate improved; however not addition and deletion errors
- Average PER(%) improved, as # training languages increased

# Related to
[[🔬XuQ22 Simple and Effective Zero-shot Cross-lingual Phoneme Recognition (Meta, IS22')|🔬XuQ(IS22)]]