---
aliases: 🔬FenS(IS23)
cite: "Feng, Siyuan, Ming Tu, Rui Xia, Chuanzeng Huang, and Yuxuan Wang. “Language-Universal Phonetic Representation in Multilingual Speech Pretraining for Low-Resource Speech Recognition.” arXiv, May 19, 2023. [http://arxiv.org/abs/2305.11569](http://arxiv.org/abs/2305.11569)."
---
#ASR #Low-resource #Phonetic

[[FengS_2023_Language-Universal Phonetic Representation in Multilingual Speech Pretraining.pdf|PDF Link]]

# Overview
- First train a language-universal IPA predictor (speech -> IPA symbol sequence)
	- Leveraging grapheme2IPA tools
	- IPA predictor is not data-hungry: 100 hrs per language was enough
	- Can be extended to any other languages without grapheme2IPA tools available
- Use IPA model to create pseudo frame labels for unlabeled speech data
- Pretrain [[🔬HuBERT|HuBERT]] using pseudo & true labels
	- Use IPA labels instead of K-means clustering

# Experiments & Results
**\# hours of speech data used in experiments** (data from the MLS corpus)
![[Screenshot 2023-06-22 at 13.08.16.png]]

**PTER% of IPA predictor models** (averaged over 7 languages' test sets)
![[Screenshot 2023-06-22 at 13.29.39.png]]

**WER% of SOTA works vs proposed method** ("Hrs" denotes the pretraining data)
![[Screenshot 2023-06-22 at 13.28.12.png]]
- Proposed MLS-7 LARGE *tends to* perform better than XLSR-53 and B0, while utilizing less pretraining data

**WER% when finetuning(FT) data is limited to 100 or 500 hours** (first column indicates the training set for IPA model)
![[Screenshot 2023-06-22 at 13.51.57.png]]
- Proposed MLS-7 LARGE beats XLSR-53 on most languages but not in DU and GE

🙋‍♂️ Maybe they should've separated languages in training & test sets?
🙋‍♂️ Can the IPA predictor really be applied effectively to unseen languages?
🙋‍♂️ (Sensei) Still not ideal because IPA targets are only used in pretraining, not in target training stage