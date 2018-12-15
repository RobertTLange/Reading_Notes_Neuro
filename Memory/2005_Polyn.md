# Title: Category-Specific Cortical Activity Precedes Retrieval During Memory
# Authors: Polyn et al (2005)

### Main Takeaway: MVPA fMRI study analyzing memory search (3 categories) during free recall task - evidence for category-specific cueing of memory system for retrieval. Reappearance of activity patterns during recall correlates with verbal recalls from category ad precedes recall event.

# General Notes:

* Recall = reactivation of constellation of representations active during that event ("mental time travel") - hypothesis: contextual reinstatement - activation of knowledge of general properties of event

* Set of representations active at recall increasingly come to resemble set of event-active representations. - Here: measure cue-trace match

* Hypothesis 1: Progressive refinement of activation pattern during recall
* Hypothesis 2: Likelihood recal <-> similarity train-test activity

* Free recall paradigm - subjects have to recall in absence of specific cues - 3x30 study items in three lists - GOAL: tracking of reinstatement

* Methods:
    * No haemodynamic lag correction!
    * NN classifier: regress object stimuli during training phase on whole-brain activity
    * Applied classifier to succesive scans and acquired time-varying estimates of extent of reinstatement
    * Event-related average of classifier estimates = category-specific brain activity realiably appeared before verbalization of recalled item

* Study phase: activation fusiform face area, parahippocampal place area activate (category-specific!) - drive contextual reinstatement

# Questions:

* No clue what architecture they used - softmax on top level for 3 categories
* Bayesian DL/Classifier methods - uncertainty/entropy decrease could also be used as measure of reinstatement trace
