# Title: Invariant Visual Representation by Single Neurons in the Human Brain
# Authors: Quiroga et al (2005)

### Main Takeaway: Subset of medial temporal lobe (MTL) neurons are selectively activated by pictures of individuals, landmarks and letter strings - Invariant, sparse and explicit code vs more distributed representations - easier trafo into long-term abstract memories.

# General Notes:
* 8 patient human study - 993 units were recorded in paradigm
    * Training/screening session in morning - display of many (ca 100) pictures with famous people and landmarks - Complemented by images selected after an interview (why?)
    * Afterwards offline analysis of data - selection of stimuli that elicited strongest responses
    * Then testing sessions - display of 3-8 variants of response eliciting stimuli (ca 80)
    * Tried to perform testing shortly after screening - max prob of recording from same units
    * Response significant = mean + 5std of baseline and at least two spikes in post-stimulus time interval (300-1000ms)
    * Response patterns of activation:
        * response disappeared with stimulus onset - 1sec after
        * rapid sequence of 6 spikes  between 300 and 600 ms after onset
        * or prolonged and continued up to 1s after stimulus offset

* Statistical methods:
    * Unclear how neuron spikes are aggregated across 8 subjects - seems like single patient - Bad!
    * ROC curve: predictiveness of specific concepts in images for firing of neuron
        * performance of binary classifier for different values of response threshold.
        * trade-off when decreasing threshold: increases prob of hits buts also false alarms
        * Robustness check: picked seven random pictures and again tested their predictive power on firing rate. Strongly below predictive power of concept "associated" with neuron.

1. Jennifer Aniston Neuron - No firing when Brad Pitt in image
    * alignment with concept encoded by neuron
    * Brad Pitt lead to conflict? - Interesting to know sex of participants

2. Hale Berry + Text string
    * Neuron also activated by letter string of concept

3. Same for landmark buildings
    * Used multi-unit in left anterior hippocampus = hippocampus, parahippocampal gyrus, anygdala, entorhinal cortex

* No movement artifact = selective responses started 300ms after image onset - key presses at 1s later

* Long-term memory formation and consolidation:
    1. connections between higher stages of visual hierarchy in ventral pathway and MTL
    2. reactivity of cortical stages feeding into MTL to sight of faces, etc
    3. any visual percept that will be consciusly remembered later has to be represented in hippocampal system

# Questions:
* Data mining - not really convincing stats. Large scale analysis as well as more robustness checks.
* Do findings really provide evidence against distributive nature of memory? - No stats are too bad.
