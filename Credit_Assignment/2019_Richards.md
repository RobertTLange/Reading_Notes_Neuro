# Title: Dendritic Solutions to the Credit Assignment Problem
# Authors: Richards & Lillicrap (2019)

### Main Takeaway: Overcome problem of mono-info transmission with the help of distinct firing patterns and dendritic architecture. We need computational models of neuronal credit assignment in order to come up with experiments which allow for testing/insights.

# General Notes:

* If credit signals are integrated with other signals it becomes hard for plasticity rules to distinguish types of activity! Solution = spatial layout of dendrites

* Learning algo = set of rules for translating experiences into neural circuit changes. - Results in altering of behavioral phenotypes!

* Problems: DNNs reduce complexity - neuron calculates everything using single voltage value - credit signal must be integrated with sensory data signals - or separate timing (not realistic). How to disambiguate?

* Spatial segregation with the help of dendritic trees, also active channels driving spiking behavior different from standard spikes (e.g. bursting/complex).

* Experimental difficulties:
    * Unclear how a loss fct can be identified and how to track it. Also: At neural level loss fct can be reduced even without direct correlate
    * Tetrode recordings - extracellular fields

* 3-Factor models: two-factor hebbian (pre, post) and a form of credit signal
    * eligibility trace - which synapses are to be updated
    * sign - LTP or LTD?

* Neuron-by-neuron credit assignment in cerebellum:
    - granule cells -> parallel fibers -> Purkinje cells
    - input to plasticity from climbing fibers from inferior olivary nucleus. c fibers map in 1-to-1 correspondece
    - climbing fibers control calcium currents - lead to complex spikes
    - specific timing controls plasticity in manner which matches temporal delay between cerebellar activity and error signal receipt
    - Problematic difference: Purkinje cells represent output of cerebellum - no depth!

* Apical compartment: recipient of higher-order cortico-cortical and thalamo-cortical feedback signals
    - in CA1 they receive long-range info back from enthorinal cortex
    - importance of bursting - NMDA spikes
    - Not spiking per se matters but the influence/effect on local polarization in the dendritic compartments

* Evidence for apical-driven plateau potentials driving formation of place-cells and determination of whether plasticity in basal dendrites occurs, even with secs between occurence of input and potentials

# Questions:

* How would a "testable" architecture look like?
* What is the role of neuromodulators in altering plasticity?
* Role for inhibitory interneurons!
