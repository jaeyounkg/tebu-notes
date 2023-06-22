---
aliases: ["AFs", "articulatory attribute", "articulatory feature"]
---

#ASR #Low-resource

- [[(MetF02) A Flexible Stream Architecture for ASR Using Articulatory Features|🔬MetzeF02]] proposed to use AFs in addition to the [[Conventional ASR|regular ASR pipeline]] in order to make systems more robust in terms of speaker or channel variability
- [[(StüS03) Multilingual Articulatory Features 1|🔬StükerS03]] showed that AFs can be recognized across different languages
- [[LeeC_2007_An overview on automatic speech attribute transcription (ASAT).pdf|ASAT Paper (07')]] describes ASAT architecture
- [[(BadL16) Integrating articulatory data in deep neural network-based acoustic modeling|🔬BadinoL16]] applies it to DNN-HMM system
- [[🔬MülM16 Towards Improving Low-Resource Speech Recognition Using Articulatory and Language Features|🔬MüllerM16]] uses AFs _and_ [[Language Feature Vectors|LFVs]] along with regular acoustic features, trained DNN-HMM model in multilingual settings
	- Only used En, Fr, De, Tr in multilingual training because only those fit their articulatory attribute framework
- [[(MitV18) Articulatory Information and Multiview Features for Large Vocabulary Continuous Speech Recognition (LVCSR)|🔬MitraV18]] uses articulatory information along with acoustic features, improving robustness to spontaneous and non-native speech
