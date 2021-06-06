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

In scikit-learn ```The BaggingClassifier``` automatically performs *soft voting* instead of *hard voting* if the base classifier can estimate class probabilities (i.e., if it has a ```predict_proba()``` method), which is the case with Decision Trees classifiers.


It is possible to sampling features (```max_features``` and ```bootsrap_features```). Each predictor will be trained on a subset of the input features. It is useful when we are dealing with high-dimensional features such as images.
* Random Patches method - Sampling both traning instances and features;
* Random Subspaces method - Sampling only features;

Sampling features give a bit more bias, but provides us a lower variance.

#### Random Forests
- Is a ensemble of Decision Trees, generally trained via bagging method. Furthermore, when splitting each node during the construction of a tree, the best split is found either from all input features or a random subset of the total features. The purpose of these extra sources of randomness is to decrease the variance of the forest estimator, at the cost of a slight increase in bias. Indeed, individual decision trees typically exhibit high variance and tend to overfit. 

- In contrast to the original publication (PUT HERE THE ORIGINAL PUBLICATION), the scikit-learn implementation combines classifiers by averaging their probabilistic prediction, instead of letting each classifier vote for a single class.




