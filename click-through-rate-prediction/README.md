# Click-Through-Rate Prediction with AFM–MLP

*LSE Machine Learning group project*

## The question

Can combining attention over pairwise feature interactions with a multilayer perceptron improve predictions of whether someone will click on a mobile advertisement?

## How we approached it

We proposed and implemented AFM–MLP, an adaptation of DeepFM that combines an Attentional Factorisation Machine (AFM) with a multilayer perceptron (MLP). The AFM learns which pairs of features are most useful, while the MLP uses the same learned embeddings to model more complex interactions.

We worked with a random sample of 10 million observations from the Avazu dataset, encoded categorical features and added time-of-day and day-of-week features. We implemented the models in PyTorch and compared AFM–MLP with logistic regression, Factorisation Machines, AFM and DeepFM. Performance was measured on a held-out test set using AUC and log-loss.

## What we found

AFM–MLP achieved the best observed test results, with an AUC of 0.7432 and log-loss of 0.4036. Its improvement over AFM was modest, however, suggesting that attention-weighted pairwise interactions accounted for most of the predictive gain in this experiment.

That makes the simpler AFM worth considering when computational resources are limited. Restricted compute, sequential hyperparameter tuning and the lack of evaluation across multiple random seeds also limit the conclusion: we would need more experiments to establish how consistently the extra MLP helps.
