## Ensemble methods and Random Forests

#### Voting classifiers
---
*hard voting* - A simple way to create a better classifier is to **aggregate** the predictions of each individual classifier and predict the class that gets the most votes.

*soft voting* - For classifiers that estimate class probabilites we have to measure the average probability of belonging to each class and predict the class with the highest probability. It achieves higher performance than hard voting because gives more information.


#### Bagging and Pasting
---
* One approach is to use the same training algorithm for every predictor, but use random subsets of the training data.
    * Bagging - When sampling *with* replacement (the same traning instance can be resampled more than once);
    * Pasting - When sampling *without* replacement;
