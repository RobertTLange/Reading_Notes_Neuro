# Title: Comparison of DNNs to spatio-temporal cortical dynamics of human visual object recognition reveals hierarchical correspondence
# Authors: Cichy et al (2016)

### Main Takeaway: Combine fMRI for spatial as well as MEG for temporal comparison for representation comparison with fixed 8 layer AlexNet. While CNN has no notion of tissue of time, the layer activations correlate with both of these notions! Highlight hierarchical correspondence and test for relevance of architecture, training by supervision as well as the task on which CNN is trained on.

# General Notes:

* Before DL nonlinear tuning of features done manually - now fully end to end via GD and backprop
    * Show 1: Ordered relationship between stages of processing in DNN and time course with which representations emerge in Brain
    * Show 2: Spatially unbiased surface-based searchlight approach reveals hierarchical relationship between CNN and processing cascade in ventral and dorsal stream

* RSA: Image-set of 118 natural objects on real-world backgrounds - unseen test for network
    * Recording with participants solving orthogonal task - why?
    * MEG: Sensor activation patterns (-100, +1000ms) -> percent decoding accuracy in pair-wise classification
    * fMRI: Spatially specific voxel patterns -> 1-Spearman's R
    * DNN: Layer-specific model neuron activations -> 1-Spearman's R
    * Make comparable by abstracting into similarity space - RDMs with 118x118

* Comparison MEG-CNN RDMs - time courses highlighting how CNN representations correlated with emerging visual representations.
* Comparison fMRI-CNN RDMs - spatial maps indicative of how representations in CNN correlated with brain activity

* Different fMRI techniques: surface-based searchlight, volumetric searchlight, partial correlation - results robust to all approaches

* Tests for where similarity comes from:
    1. Architecture: Comparison with random weights
        * Architecture alone, indep of task constraints/training procedure, leads to representational similarity, but additional factors do lead to better performance
    2. Task: Trained on different scene task
        * Scene DNN also correlated with emerging representations
    3. Supervision: Trained on random label assignment and noisy images
        * Also relevant but not necessary
    - Only all together lead to hierarchical relationship

# Questions:
* When looking at different layer mappings - left hemisphere significantly different from right one.
* Convolution is not plausible! Weight sharing does not happen across receptive fields!
