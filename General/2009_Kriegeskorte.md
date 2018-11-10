# Title: Circular analysis in systems neuroscience: the dangers of double dipping
# Authors: Kriegeskorte et al (2009)

### Main Takeaway: Results are often mistaken to "be" the data. Decoupling (independence) of selection/hypothesis generation criteria and actual analysis. Ensure independence or use different data sets/correction! Otherwise analysis is destined to overfit noise even in the light of multiple comparison correction on the analysis level.

# General Notes:

* Selection - assumption and hypothesis generation process (e.g. ROI selection) -> clearly influences the following analysis/inference (varying degrees) - 2 forms of biases:
    1. Selective reporting of accurate Results
    2. Distortion of estimates and invalidation of statistical tests

* If selection determined only based on true effect - no problem! But: Data is function of true effects and noise.

* Selective analysis is totally justified if the results are statistically independent of the selection criterion under the null hypothesis! (E.g. fixed preprocessing pipeline)

* Contrast-vector orthogonality does not suffice to ensure independence! But mapping the whole measurement volume avoids selection

* Relationship of overfitting and selection:
    * Lin reg: continuous weighting overfits noise in data
    * ROI selection using whole data set

* Regional activation analysis: Perform statistical mapping + selective activation analysis of ROIs
    * If mapping not performed correctly - problems afterwards not caused by non-indep selection but mapping
    * Ran simulation study which shows that noise is falsely taken as signal in more than chance cases


# Questions:
* How to evaluate most of previous neuroscience results (e.g. Quiroga et al (2005))? Most often there are not enough info given. Neuroscience is based on "trust" - would never work in industry.
* How can we incentivize open science practices more? Connect with grant approval and enforce pre-registration of hypothesis!
* What is contrast-orthogonality?
