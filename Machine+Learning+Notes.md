
# Summary of paper- "A Few Useful Things to Know about Machine Learning"

* It is generalization that counts, i.e. performance on the test set, unknown data.

* Only data is not enough. Choosing the right representation based on the problem. If we have knowledge about probabilistic dependencies, graphical models are a good fit.

* Overfitting. bias and variance tradeoff.  
  There is a dataset with the true underlying relationship is $Y = f(X) + \epsilon$. The estimated function is $\hat{f}$. The expected squared prediction error at x can be expressed as
  \begin{aligned} E[(\hat{f}(x) - Y)^2]
  & = E[(\hat{f}(x) - (f(x) + \epsilon))^2] \\\
  & = E[(\hat{f}(x) - E[\hat{f}(x)] + E[\hat{f}(x)] - (f(x) + \epsilon))^2] \\\
  & = E[(\hat{f}(x) - E[\hat{f}(x)]^2 + E [E[\hat{f}(x) - f(x)]^2 + E[\epsilon]^2
  \end{aligned}
  
  The first term is the variance. It is error due to variation in prediction. The second term is the bias. It is the error related to how much the average predicted value is off from the actual value. The last term is the irreducible error.

* Intuition fails in high dimension.  
  the curse of dimensionality. In high dimension data is spare. Nearest examples are not near enough. 
  (provide example of relationship in 1d, 2d amd 3d)

* Theoritical guarantees are not what they seem.  
  Bounds for number for examples. They do not reflect generalization. Provides guarantee only around number of examples needed so that with a high probability, the classifier generated will be consistent (i.e. classify all training examples correctly). Also the bound is logarithmic in cardinality of hypothesis space (number of possible functions), in some cases the number of possible function is double exponential- => bound is too loose.
  Asymptotic guarantees- given infinite amount of data, correct classifier will be generated. Not useful is practice.

* Feature Engineering is important  
  (Discuss about XOR here)
  
* More data beats a clever algorithm

* Learn many models, not just one.  
  Bagging and boosting.
  
* Simplicity does not mean accurancy  
  simpler hypotheses should be preferred because simplicity is a virtue in its own right, not because of a hypothetical connection with accuracy. A learner with a larger hypothesis space that tries fewer hypotheses from it is less likely to overfit than one that tries more hypotheses from a smaller space.
  
* Representable does not mean learnable  
  Essentially all representations used in variable-size learners have associated theorems of the form “Every function can be represented, or approximated arbitrarily closely, using this representation.” But this does not mean much. The representation has to be compact and easily learnable.
  
* Correlation does not imply causation  
  Learning algorithms learn correlation. For example, there is no notion of causality in phys- ical laws. Whether or not causality really exists is a deep philosophical question with no definitive answer.

  

