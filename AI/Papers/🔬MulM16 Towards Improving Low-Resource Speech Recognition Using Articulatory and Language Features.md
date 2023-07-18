---
aliases: 🔬MulM16
cite: "Müller, Markus, Sebastian Stüker, and Alex Waibel. “Towards Improving Low-Resource Speech Recognition Using Articulatory and Language Features.” In _Proceedings of the 13th International Conference on Spoken Language Translation_. Seattle, Washington D.C: International Workshop on Spoken Language Translation, 2016. [https://aclanthology.org/2016.iwslt-1.9](https://aclanthology.org/2016.iwslt-1.9)."
---
#ASR #Low-resource #Phonetic #Articulatory

[[MüllerM_2016_Towards Improving Low-Resource Speech Recognition Using Articulatory and.pdf|PDF Link]]

# Methodology
- Use more linguistic features along with acoustic input features
	- Language Feature Vectors (LFVs): appended to the acoustic feature vectors
	- Articulatory Features (AFs): classifiers are trained
 - 7 AF classifiers for 7 different AF types
	 - Trained in the same way as phoneme classifier
	  - Shared hidden layers + AF specific output layers
		  - To prevent networks from learning dependencies between different AF configurations, cus they're lang specific
	  - Additional class to each AF type representing "does not apply"
 - Only _middle_ sub-phoneme frames are used for training
	 - 3 sub-phone states representing parts of the phoneme as it is uttered: _begin_, _middle_, _end_
	 - This increases performance cus they're in a more stable position [[(MetF02) A Flexible Stream Architecture for ASR Using Articulatory Features|🔬MetzeF02]]
  - Train DNN-HMM hybrid system

# Articulatory Features
- Consonants (place, manner, voice)
- Vowel (type, front, height, roundedness)
- Type
	- Vowel, consonant, silence, noise

# Experiments and Results
- Using 10h of English as target, French, German, Turkish as complementary
- WER went from 18.1% to 17.3%

# Insights
- AFs benefit from LFVs
- Multilingual setups benefit from both LFVs and AFs
- Using AFs ***in combination with*** acoustic features improved performance
