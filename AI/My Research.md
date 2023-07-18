# Using Phonetic Knowledge for Multilingual ASR
"Towards Building Universal Phonetic Representation for Low-Resource ASR"
- Language-adversarial pre-training (inserted to a low-level layer of XLSR) [[🔬DinF23 Improved Self-Supervised Multilingual Speech Representation Learning Combined With Auxiliary Language Information (ICASSP23')|🔬DinF(ICSP23)]]
- Pre-training using IPA labels [[🔬FenS23 Language-Universal Phonetic Representation in Multilingual Speech Pretraining for Low-Resource Speech Recognition (IS23')|🔬FenS(IS23)]]

## Limitations of Existing Work
- IPA labels are only human interpretation of actual speech; they are inherently inaccurate
	- Different IPA labels in different langs may have different meanings
- IPA labels may be unavailable/difficult to obtain for low-resource langs
- Human knowledge about phonetics/phonology is incomplete and often inaccurate

## Ideas
- IPA symbols as weak labels?
- Use (some sort of) IPA symbols in a way that only contrasting features in target language are considered
- Contrastive Learning for contrastive articulatory features?
- Somehow embed phonetic rules (allophonic & free variations) into model

