(Lee and Glass, 2012) A Nonparametric Bayesian Approach to Acoustic Model Discovery

# Summary
- Traditionally, unsupervised [[Acoustic Model]] has been broken down to **3 sequential and independent sub-tasks**: segmentation, clustering segments, modeling each cluster's acoustic patterns
- This work models the 3 sub-problems *and* the unknown set of sub-word units as **latent variables in one nonparametric Bayesian model**.

	![[Screenshot_20220826_160846.png]]
- Each cluster is modeled by an HMM ($\theta_c$)
- Each HMM has 3 hidden states ($s_t^i$): beginning, middle, end of a sub-word unit
- Each HMM state's emission probability is modeled by a diagonal GMM with 8 mixtures