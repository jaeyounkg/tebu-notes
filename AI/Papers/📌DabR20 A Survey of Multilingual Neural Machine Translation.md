# Intro
- MNMT systems are desirable because they can
	- help resource-poor langs acquire extra knowledge from other langs
	- generalize better thanks to diverse langs (translation knowledge transfer)
		 - multilingual training is known to be a source of regularization 
	- enhance knowledge transfer between low-resource langs
	- potentially be relatively compact & reduce deployment footprint
- Major scenarios where MNMT has been explored in the literature
	- Multiway translation: one-to-many, many-to-one, or many-to-many translation
	- Low-resource translation
	- Multi-source translation: source data that need to be translated is in multiple languages

# Neural Machine Translation
- Most common approach is _Embed - Encode - Attend - Decode_ paradigm
	- Embed: convert words into word embeddings
	- Encode: neural representation that captures contextual information
	- Decode: use attention mechanism to decode contextual information into target text
- Training NMT models
	- Pre-processing of data
		- Parallel corpus for training first goes through pre-processing to remove noisy data
		- Vocabulary of _N_ most frequent words is created and the remaining words are treated as _UNK_
		- Byte-pair encoding, word-piece model, or sentence-piece model is employed to deal with the problem of unknown words
	- Loss function: typically a cross-entropy loss
	- Gradient descent methods like SGD, AAM, ADAGRAD, etc., can be used
		- ADAM is mainly used in MT, but it tends to not converge enough
		- SGD converges better but requires longer training times
	- Hyperparameters like learning rate, hidden dimension size, number of layers, etc., need to be considered
- Decoding NMT models (inference)
	- Simplest algorithm is beam search decoding

# Multiway NMT
- Multiway NMT is important because transfer learning between languages can help improve the overall translation quality for many translation directions

## Parameter Sharing
- **Minimal parameter sharing**
	- Only shared attention mechanism, and separate encoder & decoder for every language
- **Complete parameter sharing**
	- All languages share the encoder & decoder & attention
	- A special token called _language tag_ is put in the beginning
	- NMT system is treated as a complete black box
	- Has maximum simplicity and minimal parameter size
		- Can achieve comparable/better results w.r.t. bilingual systems, with the same parameter size
	- **Massively multilingual NMT**: combine as many as 100 languages or more
		- Tend to benefit translation _into English_ a lot more than _from English_
		- **Representation bottleneck**: not all translation directions are benefited
- **Controlled parameter sharing**
	- Somewhere between minimal and complete parameter sharing
	- The burden of generation is on the decoder, so keeping the decoders separate is importan

## Addressing Language Divergence
- The nature of multilingual representations
	- 
- Encoder representation
- Decode representation
- Impact of language tag

## Training Protocols
- Single stage Parallel/Joint Training
- Knowledge distillation
- Incremental training
- 