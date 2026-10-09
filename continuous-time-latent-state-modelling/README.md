# Continuous-Time State-Space Modelling of NBA Shooting

*Two-person LSE Applied Statistics project*

## The question

Do NBA players experience changes in shooting form during a game, and can modelling those changes help predict their next shot? We wanted to distinguish a persistent change in form from apparent streaks caused by chance or differences in shot difficulty.

## How we approached it

We used shot data from the 2022–2025 NBA regular seasons, organised into player-game sequences. The main training sample contained 493,888 attempts across 44,417 sequences.

We extended an existing continuous-time state-space model from free throws to live-play field goals. An unobserved shooting state followed a mean-reverting Ornstein–Uhlenbeck process, with a logistic observation model linking it to make-or-miss outcomes. This allowed the model to account for irregular gaps between shots. A separate expected-field-goal model controlled for shot location, distance, type and game context.

We approximated the likelihood using a discretised state space and forward algorithm, then estimated parameters numerically. We compared model fit and held-out predictions with logistic-regression benchmarks.

## What we found

The latent-state model fit the training data better, both before and after adjusting for shot difficulty. Estimated half-lives of roughly 41–55 minutes suggested a slower within-game performance component, closer to a "hot game" than immediate shot-to-shot momentum.

However, it predicted unseen shots from the final 40% of the 2025 season less well than the logistic benchmarks. The main lesson was that a model can capture retrospective temporal patterns without making better next-shot forecasts. The results did not establish a predictive advantage for the latent shooting state.
