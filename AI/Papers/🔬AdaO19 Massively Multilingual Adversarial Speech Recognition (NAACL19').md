---
alias: 🔬AdaO(NA19)
---
#ASR #MassivelyMultilingual #Adversarial 

Try 2 auxiliary training tasks for language-independent representation for better adaptation
- (1) **Context-independent** phoneme sequence prediction
- (2) Language-[[Adversarial Learning|adversarial]] classification objective
Hierarchical combination of grapheme & phoneme objectives

# Conclusion
- Using the aux. tasks in pretraining facilitates model transfer to unseen langs, esp. when the pretraining langs are very dissimilar
- 

# Findings
- Using the (1) phoneme objective during adaptation was harmful
