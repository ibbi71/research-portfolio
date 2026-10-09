# An Introduction to Optimal Transport Theory

*Individual mathematics dissertation, LSE*

## The question

How can we move mass between distributions at the lowest possible cost? And, working backwards, what can observed movements tell us about costs we cannot directly observe?

## How I approached it

I developed an exposition of the Monge and Kantorovich formulations, explaining the difference between assigning each source to one destination and allowing mass to be split between destinations. I reconstructed an existence proof for an optimal Kantorovich plan under suitable assumptions, derived the dual problem, proved weak duality and outlined the argument for strong duality.

An electricity-transmission example provided a concrete way to interpret the theory throughout. I also discussed linear programming, entropy regularisation and the Sinkhorn algorithm, before reviewing an application of inverse optimal transport to international trade.

## Main conclusions

The Kantorovich formulation gives a flexible, convex optimisation problem, while duality provides another way to understand both the minimum cost and its economic meaning.

The inverse problem is more difficult to interpret. Recovered costs depend on modelling assumptions and parameter choices, may not be uniquely identifiable, and cannot automatically be given a causal interpretation. The trade application was a useful way to examine these limitations.

This was a theoretical and expository dissertation. The computational methods and application were explained and critically reviewed rather than independently implemented; the proofs develop established results rather than claim new theorems.
