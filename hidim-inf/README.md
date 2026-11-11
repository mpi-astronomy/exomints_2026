# Hi-Dim Team
Lead: Beatriz

Contributors: Patricio, Nora, Tamara, Max, Gilles, Morgan (@mfouesneau), David, Beatriz, Paul

## Rational

Nested sampling isn’t inherently doomed, but its cost becomes hard to sustain as retrievals add more molecules, cloud properties, temperature parameters, and complex physics. Each likelihood evaluation requires a forward-model calculation, while degeneracies and multiple plausible solutions can force many evaluations: modern retrievals commonly need 
10^4 - 10^7 and some JWST analyses have required up to  10^8. That makes high-dimensional, repeated, or survey-scale analyses a serious time and compute bottleneck. 

Here we aim to broaden the toolkit, not abandon nested sampling: test simulation-based inference and flow-matching approaches for fast posterior estimation, use emulators to reduce forward-model costs, and validate their results against established samplers. 
We will perform tests with/against nested sampling on datasets at lower computational cost, though it still needs broader validation before being treated as a drop-in replacement.

