# Title: Backpropagation through time and the brain
# Authors: Lillicrap & Santoro (2019)

### Main Takeaway: BPTT - Credit assignment through time and space comes with additional problems (vanishing/exploding gradients) - need additional neuro-inspired components to overcome (memory and attention).

# General Notes:

* BPTT: Requires a potentiation of the time shared weight matrix for each time step that we want to propagate back. Spectral radius of weight matrix needs to be close to one 1 otherwise explosion/vanishing gradient - (depending on length of trained sequence)
    * If gradient vanishes - simply need to long time to train! More epochs

* Alternative approaches:
    * Echo state networks: recurrent weights that are not learned - avoid gradient computation at cost of expressivity
    * Unitary RNNs: constrain weight matrix to be unitary - eigenvalues are 1
    * Set initial weight matrix to be orthogonal to produce better behaved gradients at beginning of training
    * Gatting mechanism controls for flow of info into recurrent memory units. Gradient of error wrt held gate value is indep of computations in intervening timesteps
        * Problem: Functional overload of a unit
    * Truncated BPTT: BPTT on fixed window size of time steps - window slides to keep number of products small
        * Less prone to exploding/vanishing at cost of not being able to assign credit outside of truncation window.
        * Also more plausible since less activations are stored
    * Forward-Mode differentiation: Runs forward in time - Online keep track of param sensitivity of hidden state - Real-Time Recurrent Learning - Large propagated sensitivities possible. Large memory as well computation requirements
    * Eligibility trace based updating

* Feedforward nets - BP more plausible than also through time since we would need to store the activations of all hiddens. For FFW activity states live in unique sets of neurons

* Role of replay forward and backward - systems consolidation (memories to cortex encoding)
    * Hippocampus thought to encode memories by establishing attractor states in CA3. In turn, partial reactivation of these CA3 attractors induces re-activation if neocortical neurons responsible for initial encoding.

* Attention: Assume that hidden states are stored outside of model but readily accessible - Attended states are used to update - SKIP CONNECTION
    * Augmenting Gated RNNs with own large external memory - read and write
    * Alternative: Use fixed number of slots for updating - retrieval via query vector and attention weight proportional to cosine dissimilarity
        * Discrete vs continuous attention - allow for gradient flow!
        * Query vector is linear combination of all hidden states - not learned? or fully end-to-end

# Questions:

* TBPTT with an adaptive window size?! Based on evolution of the product? Dynamic!
