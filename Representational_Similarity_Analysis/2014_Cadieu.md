# Title: Deep NNs rival the representation of Primate IT Cortex for Core Visual Object Recognition
# Authors: Cadieu et al (2014)

### Main Takeaway: Use CNNs and neural recording from 2 macaques to construct features/representations and compare the resulting performance (complexity-controlling kernel ridge regression), representational similarity as well as predictive strength for individual IT multi-unit responses.

# General Notes:

* Core visual object recognition: Judgement within a single saccadic fixation. End of ventral stream - IT cortex creates representation that is selective for object identity and invariant. - V1 -> V2 -> V4 -> IT

* Hubel, Wiesel - Hypothesized that within primate visual cortex more complex functional responses (complex cells) were constructed from more simplistic responses (simple cells). - Origin of all hierarchical modeling

* (Claimed) Advantages of paper attempt for model comparison:
    * Correction of experimental limitations - noise, recording sites, # stim presentations by modifying representations with artificial noise
    * No fixed complexity classifiers - Use of kernel analysis: measure accuracy of representation as fct of complexity and performance
    * Measure variations in neural/model space relevant to class-level object classification. Directly measure amount of IT variance captured by dnn as IT encoding models.
    * Wider stimulus range - 1960 images - 7 categories - 7 3D objects (49 representations for RDM) - randomly chosen background (40 times)

* Definition of behavioral context: Experimental setup - natural duration fixation - presentation time of 100ms
    * Recordings: 168 multi-unit sites IT, 128 multi-unit sites V4 - 40 single-unit sites isolated

* Kernel Analysis for Performance evaluation: Measures how precision of category regression problem changes as we allow complexity of regression function to increase. More effective representations achieve higher presion at same level of complexity.

* Yamins 2014 - HMO (Hierarchical Modular Optimization) DNN, V1, V4 like models to compare performance of AlexNet with

* Extract features from penultimate network layer and averaging over 10 image crops.

* Noise matching: Added noise to model representations due to nature of recordings. Spike counts approx poisson -> model repsonse variability as being proportional to mean response - linear function - generally decreases performance.

* DNNs perform better than V4 as wells as other models. Undersampling and noise matching IT representation only matched by ALexNet.

* Difference between single-unit and multi-unit recording performance comparison: AlexNet closer to single unit. Zeiler & Fergus (2013) model closer to multi-unit

* Variance explained: CNN trained on many more classes than 49, brain even more - no model can account for full variance in IT multi-unit responses

* Representational similarity: Compute RDMs for both neural measurements/features and CNN ones - Sort the visualizations accordingly. - Computational measure of similarity: Spearman Rank Correlation
    * In order to determine variability due to IT neural sample - present similarity measure between one-half of IT multi-units and the other half?!

* Decoding - Performance Comparison || Encoding - RSA

# Questions:

* What does comparable performance even mean? Not necessarily comparable computation - also not really given by similar representations?!
* Different dims of penultimate layers. Any form of dim reduction or just sticking into regularized kernel regression?
* Better form of representational comparison than spearman? More info-theoretic?
* R-CNN more dynamics/reaction time modeling - Kriegeskorte
* Argue for neural plausibility of computations but conv/weight sharing is really unplausible.
