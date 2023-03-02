# Machine Learning Skill Checks for Midterms
### CS181
### Spring 2023
![](https://i.imgur.com/xDR9VQd.png)


# Midterm #1

The following cover content for Midterm #1. You should consider any instantiation of the questions in this section fair game for the midterm (please refer to the Midterm #1 Practice Problems for examples). 

There are two types questions on the midterm:
1. **Derivations** - performing opertations on experssions and computations
2. **Conceptual reasoning** - writing out a rigorous logical argument to support a conclusion (referencing fact or theory presented in lecture). Please note that while there is no one single correct conclusion or a single correct argument, ***this does not mean that all arguments are correct (logical)!*** Please treat conceptual reasoning questions as asking for a ***[math proof](https://heil.math.gatech.edu/handouts/proofs.pdf)*** (rather than derivation) and be as formal and rigorous as you can

**Test Aid:** Midterms are closed-book and closed-internet. However, you will be allowed to bring with you one 8'x11' sheet of paper with information front and back as a test aid. 

Things we will **never** ask you to do on the midterm:
1. Take complicated derivatives (i.e. expect you to know the derivatives of fancy functions $\tan^{-1}$, $\cosh$ etc) without reference.
2. Evaluate complicated integrals by hand (i.e. expect you to remember integration by parts, u-substitution etc).
3. Apply complex formulae or theorems from memory.

Things from course pre-req's you should be able to do:
1. Simple differentiaion (e.g. sum, product, power, constant multiple, exponential, log, sine and cosine)
2. Simple antiderviatives (e.g. sum, product, power, constant multiple, exponential, sine and cosine)
3. Using the 2nd Fundamental Theorem of Calculus (i.e. evaluating definite integrals using antiderivatives)
4. Familiarity with normal distributions (e.g. reading off moments from the normal pdf, recognizing normal pdf's, intuitive reasoning about the shape of the pdf given the formula, simple properties of normal pdfs like symmetry/unimodality etc).
5. Familiarity with Bernoulli distributions (e.g. reading off moments from the Bernoulli pdf, recognizing Bernoulli pdf's, intuitive reasoning about behaviors of Bernoulli RVs given parameters of the distribution, etc).
6. Familiarity with multi-variate normal, or Gaussian, distributions (e.g. reading off moments from the Gaussian pdf, recognizing Gaussian pdf's, interpreting the diagonal and off-diagonal entries of the covariance matrix, reasoning about the conditionals and marginals given the Gaussian pdf, simple properties of Gaussian pdfs like symmetry/unimodality etc).
7. Definition and properties of the expectation operator (e.g. defining expectation as an integral, linearity of expectations).
8. Definitions of joint, conditional and marginal pdf's and probabilities.
9. Definition of (conditionally) independent RVs
10. Matrix and vector arithmetic (excluding the formula for matrix inverse)
11. Definition and properties of matrix transpose 
12. Definition and properties of matrix inverse (not the formula!) 

## Broader Impact Analysis
- ***(Terminology)*** Can you define the terms user, affected community and socio-technical system?
- ***(Concept)*** Can you describe and give examples where the users and the affected community are not the same body? Can you describe and give examples where the users and the affected community do not have the same set of interest or goals?
- ***(Concept)*** Can you describe the pitfalls of model evaluation metrics that reports the average performance in terms of data heterogeneity?
- ***(Concept)*** Can you describe how (and give concrete examples where) sampling bias can translate into bias in model interpretation and model prediction?
- ***(Concept)*** Can you describe how (and give concrete examples where) lack of measures of model uncertainty compromises safety (*Hint:* think about out of distribution, OOD, points)?
- ***(Concept)*** Can you describe why and given examples wherein we need to not only optimize our numeric evaluation metrics, we need to consider the socio-technical system (specifically, where optimized ML models would nonetheless perform suboptimally on tasks when embedded in socio-technical systems)?
- ***(Concept)*** Can you give concrete examples where model selection cannot be informed by math/stats but by domain knowledge? Can you give concrete examples where model evaluation cannot be informed by math/stats but by domain knowledge?
- ***(Concept)*** Can you describe (and give concrete examples) ways a perfectly performing (according to all numerical metrics) model can fail in deployment (outside of incorrect human usage, incorrect implementation and other engineering problems)?

**Example in Literature:** 
  - [Why is My Classifier Discriminatory?](https://arxiv.org/abs/1805.12002)
  - [Explicitly Exluding Racial Information Does Not Exclude Racial Information in Health-care](https://news.mit.edu/2022/artificial-intelligence-predicts-patients-race-from-medical-images-0520)

## Regression

1. **Residuals and Loss Functions**
  - ***(Math)*** Can you compute mean squared error, mean absolute error and max absolute error of a regression model?
  - ***(Concept)*** Can you use these loss functions to select between two candidate models? Can show when these loss functions would agree in their ranking of two models and when they would disagree?
  - ***(Concept)*** Can you use the comparison of train test loss to detect overfitting? Can you explain why comparison of train test loss cannot detect underfitting?
  - ***(Concept)*** For each loss function, can you come up with a real life application where this loss function is more appropriate as a metric than the other two loss functions?

2. **Probabilistic Regression**
  - ***(Math)*** For a probabilistic regression model with additive observation noise, that is, given any $y = f_\mathbf{w}(\mathbf{x}) + \epsilon$, $\epsilon \sim p(\epsilon)$, can you derive the likelihood $p(y\vert \mathbf{x}, \mathbf{w})$ given that an oracle will tell you how the moments (or parameters) of the RV $\epsilon$ will be changed by the addition of a constant $f_\mathbf{w}(\mathbf{x})$ (for example, if $\epsilon$ is normal, if $\epsilon$ is Laplace, or Student-t)?
  - ***(Math)*** Can you describe with respect to which variable is $p(y\vert \mathbf{x}, \mathbf{w})$ a pdf and with respect to which variables it is not?
  - ***(Math)*** Given the likelihood of a single point, can you write down the joint likelihood of $N$ number of iid points?
  - ***(Concept)*** Can you interpret the properties of the pdf of $\epsilon$ in terms of our assumptions about the observation noise (e.g. what does it mean that our noise is mean zero, what does it mean that our noise has high variance, what does it mean that our noise is symmetric and has a thin tail)?
  - ***(Concept)*** Can you identify the hyperparameters of probabilistic regression? 
  - ***(Concept)*** Can you describe how I can choose the hyperparameters in a principled way?
  - ***(Math)*** If I want to learn the hyperparameters of probabilistic regression by maximizing the likelihood, can you write down the objective function? 
  - ***(Concept)*** Can you interpret the joint likelihood, for example, using it to compare two different regression models?
  - ***(Math)*** For Gaussian additive observation noise, can you relate the joint likelihood to MSE (e.g. through the log likelihood)?
  - ***(Math)*** Can you reason about the ordering of MSE versus ordering of log-likelihood for some reasonable additive noise model. That is is MSE for Model 1 is larger than the MSE for Model 2, what does that imply about the ordering of the log-likelihoods of these models?
  - ***(Math)*** Can you show why computing average log-likelihood is better facilitates model comparison than joint log-likelihood?
  - ***(Math)*** Can you write down the form of $f_\mathbf{w}(\mathbf{x})$ in vector notation when we are performing linear regression? Can you wrie down the form of $f_\mathbf{w}(\mathbf{x})$ when we are performing linear regression over a feature basis determined by a feaure map $\phi$.
  - ***(Math)*** Given a feature map, can you compute $\phi(\mathbf{x})$?
  - ***(Concept)*** Can you identify the design choices of basis egression? Can you describe how these choices affect the regression model?
  - ***(Concept)*** Can you describe how I can make these design choices in a principled way?

4. **Non-Probabilistic Regression**
  - ***(Math)*** For a regression problem with two variables, can you translate a given regression tree into a piecewise constant function over $\mathbb{R}^2$ and vice-versa?
  - ***(Math)*** Given the math formula of a kernel, and a training dataset, can you use kernel regression to predict the target $y$ for a test point $\mathbf{x}$?
  - ***(Math)*** Can you identify the hyperparameters of regression tree, KNN and kernel regression with a given kernel function? 
  - ***(Concept)*** Can you describe how the hyperparameters affect the behanvior of the regression model?
  - ***(Concept)*** Can you describe the role the kernel function plays in kernel regression (i.e. what does the kernel function measure)?
  - ***(Math)*** Can you show that KNN is a form of kernel regression (i.e. what is the kernel function for KNN regression, is this a valid kernel function)?
  - ***(Concept)*** Can you reason about when I'd want to use KNN vs kernel regression using an RBF kernel?
  
3. **Inference and Optimization**
  - ***(Math)*** Given a loss function (probabilistic or not), can you formalize learning a regression model as an optimization problem -- using appropriate mathematical notation? 
  - ***(Math)*** Given a loss function, do you know the steps for analytically optimizing it (assume that you can ask an oracle for help in computing derivatives and gradients)? Do you know the definition of local versus global optima? Do you know how derivative and gradients can be used to find local optima? Do you know what convexity implies about local and global optima? 
  - ***(Math)*** Can you show that maximizing the joint log-likelihood of a regression model with additive Gaussian observation noise is equivalent to minimizing the MSE? Can you show that this is not true if we change the noise model?
  - ***(Math)*** Using concepts from calculus, can you show why one would prefer to optimize MSE rather than sum of absolute error or max absolute error?
  - ***(Concept)*** If you are unable to analytically optimize your loss function, given the gradient, can you derive the steps of gradient descent (by which I mean describe the steps and justify why each step is reasonable)?
  - ***(Concept)*** What are the design choices (hyperparameters) of gradient descent (learning rate and stopping condition)? How does each choice affect the behavior of gradient descent?
  - ***(Concept)*** Do you know the two common failure modes of gradient descent (slow convergence and oscillation)? Do you know how to detect each type of failure mode? Do you know some common fixes for these failure modes?
  - ***(Concept)*** Do you know the statistical properties of the MLE (i.e. is it unbiased, it is consistent, does it have minimum variance when it is unbiased?)? Can you explain under what situations we would want our estimator to be unbiased, when we'd want consistency and why we care about variance of the estimator?
  
5. **Additional Model Evaluation:** 
  - ***(Concept)*** Do you know how to evaluate your assumption of the observation noise distribution in probabilistic regression?
  - ***(Concept)*** Do you know the common pitfalls of evaluating your model using MSE?
  - ***(Concept)*** Do you know the common pitfalls of evaluating your model using the joint log-likelihood?
  - ***(Math)*** Do you know the space/time complexity of basis regression (at train time and at test time) as a function of the number of (train or test) data points,  the dimensionality of the input and the dimensionality of the feature map?
  - ***(Math)*** Do you know the space/time complexity of KNN and kernel regression (at train time and at test time) as a function of the number of (train or test) data points and the dimensionality of the input?
  
7. **Model Interpretation** 
  - ***(Concept)***  Given a problem context, can you interpret how a linear regression model is making predictions? Can you determine if the decision process of a linear regression model is reasonable?
  - ***(Math)*** Are you able to compute predictive and confidence intervals by bootstrapping?
  - ***(Concept)*** Are you able to interpret predictive and confidence intervals?
  - ***(Concept)***  Given a problem context, can you interpret how a regression tree model is making predictions? Can you determine if the decision process of a regression tree model is reasonable?
  - ***(Concept)***  Given a problem context, can you interpret how a KNN or kernel regression model is making predictions? Can you determine if the decision process of the model is reasonable?

  
8. **Model Comparison**
  - ***(Concept)*** Can you describe the three axes of model comparison (probabilistic vs non-probabilistic, parametric vs non-parametric, complex vs simple), as well as give definitions of the first two axes?
  - ***(Concept)*** Can you compare different models along any given axes?
  - ***(Concept)*** Can you use the axes of comparison to argue which model is appropriate for which set of real-life applications?

9. **Bias-Variance Trade-off**
  - ***(Math)*** Given the bias variance decomposition of the generalization error, can you describe in words what each set of notation and each set of terms mean in the equation?
  - ***(Concept)*** Can you describe why in real-life, with few exceptions, we can't actually compute the model bias and model variance from the formula given by the decomposition of the generalization error?
  - ***(Concept)*** Can you say what is the point of looking at the bias-variance decomposition of the generalization error if we can't compute the formula in real life?
  - ***(Math)*** Can you relate bootstrapping to sampling training data sets $\mathcal{D}$ from $p(\mathcal{D})$? Can you describe the difference between sampling training data sets $\mathcal{D}$ and bootstrapping?
  - ***(Concept)*** Can you define model bias intuitively? Can you define model variance intuitively?
  - ***(Concept)*** Can you intuitively argue why model bias and variance would contribute to generalization error?
  - ***(Concept)*** Can you describe some common sources of model bias? Can you describe some common sources of model variance? 
  - ***(Concept)*** Can you relate model bias and variance to underfitting and overfitting?
  - ***(Concept)*** Can you describe some common methods for decreasing model bias? Can you describe some common methods for decreasing model variance? 
  - ***(Concept)*** Can you describe what is the "Bias-Variance Trade-off"? Can you given an example where reducing bias and reducing variance are in tension?
  - ***(Math)*** Given the formula of $\ell_1$ and $\ell_2$ regularization for regression, can you compute the regularized loss function given $\mathbf{w}$ on a data set?
  - ***(Concept)*** Can you describe how $\ell_1$ and $\ell_2$ regularization potentially increases bias and potentially decreases variance? 
  - ***(Concept)*** Can you explain the difference between $\ell_1$ and $\ell_2$ regularization -- when would I want to use $\ell_1$ vs $\ell_2$ regularization?
  - ***(Math)*** Can you define ensembling -- in particular, Bagging?
  - ***(Concept)*** Can you explain the difference between ensembling and regularization -- when would I wan to use ensembling vs regularization?

**Examples in Literature**:
  - If you want more math, read up on how kernel regression is equivalent to basis regression (this is a vitally important fact in helping us understand the behavior of neural networks later)! [Random Fourier Features](https://gregorygundersen.com/blog/2019/12/23/random-fourier-features/)
  - Not everything is a neural network -- basis regression is important and interesting: [Random Features for Large-Scale Kernel Machines](https://people.eecs.berkeley.edu/~brecht/papers/07.rah.rec.nips.pdf), [Random Fourier Features for Kernel Ridge Regression: Approximation Bounds and Statistical Guarantees](http://proceedings.mlr.press/v70/avron17a/avron17a.pdf)
  -  Understanding linear regression over an arbitrary basis helps us understand neural networks! [The generalization error of random features regression: Precise asymptotics and double descent curve](https://web.stanford.edu/~montanar/RESEARCH/FILEPAP/gen_rf.pdf)
  -  Observation noise is not always Gaussian! [Parameter estimation in non-Gaussian noise](https://academic.oup.com/gji/article/94/1/131/585745)

## Classification

1. **Geometric Interpretation of Classification**
  - ***(Math)*** Can you define soft and hard classification?
  - ***(Concept)*** Can you describe under which real-life data scenarios we would prefer soft classification over hard classification?
  - ***(Math)*** Can you derive logistic regression as soft classification using (signed) Euclidean distance to a decision boundary given by the equation $\mathbf{w}^\top \mathbf{x} = 0$?
  - ***(Math)*** Can you derive logistic regression as soft classification using (signed) Euclidean distance to a decision boundary given by the equation $\mathbf{w}^\top \phi(\mathbf{x}) = 0$, where $\phi$ is a feature map?
  - ***(Math)*** Can you visualize $\mathbf{w}^\top \phi(\mathbf{x}) = 0$, where $\phi$ is a feature map, as a decision boundary for binary soft-classification?
  - ***(Math)*** Do you know how to make hard classification decisions by thresholding soft classification probabilities?
  - ***(Concept)*** Can you describe the role that the sigmoid function plays in logistic regression?
  - ***(Math)*** Given a different function $\sigma: \mathbb{R} \to (0, 1)$, and a decision boundary $$\mathbf{w}^\top \phi(\mathbf{x}) = 0$$ can you derive a soft classification model -- i.e. can you model $p(y=1 \vert \mathbf{x})$?
  - ***(Concept)*** Given a decision boundary $\mathbf{w}^\top \phi(\mathbf{x}) = 0$ for binary classification, can you reason about the classification probability of points close to the boundary and about points far from the boundary? Can you provide justification for why the classfication probability should behave in real-life as you described? Can you provide reasons why classification probability should **not** behave in real-life as you described?

2. **Probabilistic Interpretation of Classification**
  - ***(Math)*** For a single observation $\mathbf{x}, y$ can you write down the likelihood for logistic regression over an arbitrary basis given by feature map $\phi$?
  - ***(Concept)*** Can you explain why this likelihood is a reasonable model for classifaction (why is this a good model for $\mathbf{x}, y$ where $y$ is binary)?
  - ***(Math)*** Can you write down the joint likelihood for logistic regression given a dataset and a feature map $\phi$?
  - ***(Math)*** Given a set of weights $\mathbf{w}$ for a logistic regression model, can you derive the impact a single weight $\mathbf{w}_d$ has on the log-odds?
 
  
4. **Inference and Optimization**
  - ***(Math)*** Can you show why it is not possible to direcly optimize accuracy?
  - ***(Math)*** Can you find the gradient of the joint log-likelihood for logistic regression given a dataset and a feature map $\phi$?
  - ***(Math)*** Can you show that analytic optimization of the logistic regression joint log-likelihood is not feasible?
  - ***(Math)*** Can you explain why computationally optimizing the logistic regression joint log-likelihood using gradient descent would be problemmatic (i.e. do you know where all the places you can encounter numeric instability)?
6. **Model Evaluation**
  - ***(Math)*** Can you define accuracy? Can you given an example in which classfication accuracy is a misleading metric?
  - ***(Math)*** Can you define the ROC?
  - ***(Math)*** Can you define false positive (negative) rate, true positive (negative) rate?
  - ***(Concept)*** Can you given examples of application where one rate should be prioritized above others?
  - ***(Concept)*** Can you interpret the meaning of a point on the ROC in terms of classifier behavior given a particular classification threshold?
  - ***(Math)*** Can you derive the ROC of a random classifer and a perfect classifier?
  - ***(Concept)*** Can you use the ROC to compare and select models?
  - ***(Concept)*** Can you give examples for when to prioritize accuracy and when to prioritize ROC in model selection/evaluation?

7. **Model Interpretation** (See Regression)
8. **Model Comparison** (See Regression)
9. **Bias-Variance Trade-off** (See Regression)

**Examples in Literature**:
- There is no best evaluation metric, especially when there is class imbalance! [The impact of class imbalance in classification performance metrics based on the binary confusion matrix](https://www.sciencedirect.com/science/article/pii/S0031320319300950)
- When there is class imbalance, we know little about the provable behaviors of our classifiers (i.e. you can't jus do math to anticipate failure modes). [On the Statistical Consistency of Algorithms for Binary Classification under Class Imbalance](http://proceedings.mlr.press/v28/menon13a.pdf)
- Model interpretability and fairness is rigorous and deep science (i.e. highly technical)! [Trade-Offs between Fairness and Interpretability in Machine Learning](https://projects.iq.harvard.edu/files/crcs/files/ai4sg-21_paper_24.pdf), [Examples are not Enough, Learn to Criticize! Criticism for Interpretability](https://proceedings.neurips.cc/paper/2016/file/5680522b8e2bb01943234bce7bf84534-Paper.pdf)
- Uncertainty quantification is a hard, active area of research! [Uncertainty-Aware Deep Classifiers Using Generative Models](https://ojs.aaai.org/index.php/AAAI/article/view/6015)

## Neural Networks
1. **Graphical Representation & Model Definition**
  - ***(Math)*** Can you define the terms node, width, activation and architecture?
  - ***(Math)*** Given an activation function, can you write out the analytical formula for the function that is defined by the graphical representation of a neural network?
  - ***(Math)*** Can you recast neural network regression as basis regression with a learned rather than fixed feature map?
  - ***(Math)*** Can you recast neural network probabilistic classification as logistic regression with a learned rather than fixed feature map?
  - ***(Math)*** Can you state the universal approximation theorem for neural networks?
  - ***(Concept)*** Can you explain why the universal approximation theorem is significant for deep learning?
  - ***(Concept)*** Can you describe the pros and cons of neural network regression (classifictation) compared with basis regression (logistic regression over an arbitrary basis)?
  - ***(Concept)*** Can you describe the effect of increasing NN depth and width on the complexity of the function represented by the network?

3. **Inference and Optimization**
  - ***(Math)*** Can you prove that neural network regression and classification is not convex?
  - ***(Math)*** Can you compute neural network gradients by hand (for a small network with a simple activation function) by back-propagation (applying the chain rule iteratively working backwards in the network)?
  - ***(Math)*** Can you derive the computational graph for simple functions?
  - ***(Math)*** Can you perform forward and backward automatic differentiation by hand, for small computational graphs?
  - ***(Concept)*** Can you describe for which types of neural networks is forward differentiation more efficient? For which types of NNs is backwards differentiation more efficient?
  - ***(Concept)*** Can you describe the main reasons why neural network optimization is difficult?
  - ***(Concept)*** Can you describe the three main failure modes of gradient descent for neural network optimization? Can you describe the common remedies for these failure modes?
  

5. **Model Evaluation**  (See Regression & Classification)
6. **Model Interpretation** 
  - ***(Concept)*** Can you explain the main challenges of interpreting neural networks?
  - ***(Concept)*** Can you describe (at a high level) a few methods for interpreting neural networks?


8. **Model Comparison** (See Regression & Classification)
9. **Bias-Variance Trade-off** (See Regression & Classification)

**Examples in Literature:**
- Neural network bias-variance trade-off is very intuitively challenging! We've found that sometimes overly complex models REDUCE generalization error -- [The role of over-parametrization in generalization of neural networks](https://openreview.net/forum?id=BygfghAcYX)! But bigger isn't always better -- [Deep Double Descent: where bigger models and more data hurt](https://arxiv.org/pdf/1912.02292.pdf).
- Proving even the smallest things about neural networks using math is extremely hard -- the math becomes extremely fancy [Neural Tangent Kernel: Convergence and Generalization in Neural Networks](https://proceedings.neurips.cc/paper/2018/file/5a4be1fa34e62bb8a6ec6b91d2462f5a-Paper.pdf)
- Again, understanding more about basis regression helps us understand neural network behavior [Feature Learning in Infinite-Width Neural Networks](https://arxiv.org/pdf/2011.14522.pdf)


## Bayesian vs Frequentist Models


1. **Model Definition**
 - ***(Math)*** Do you know Baye's Rule -- that is, given the joint pdf of two RV's $p(A, B)$, can you define the pdf of the *marginal* distribution of each RV, the pdf of two *conditional* distributions?
 - ***(Math)*** Can you define all the marginal and conditional pdf's for Bayesian regression, where $\mathcal{D} = \{ (\mathbf{x}, y)\}$ is the observed data, $\mathbf{w}$ is the parameters of the function (e.g. $p(\mathbf{w})$ etc)? Can you name these distributions (e.g. prior etc)?
 - ***(Math)*** Can you define the posterior predictive distribution for Bayesian regression (i.e. as an integral)?
 - ***(Concept)*** Can you interpret the prior distribution as a belief? Where do priors come from -- i.e. how is a prior determined?
 - ***(Concept)*** Given a belief about parameters $\mathbf{w}$ in plain English, can you identify a pdf that appropriately encodes this belief as a prior on $\mathbf{w}$?
 - ***(Concept)*** Can you interpret the posterior distribution as a belief -- in particular, can you relate the posterior to the prior belief and the likelihood of the data? 
 - ***(Concept)*** Can you reason about the impact of the prior variance (mean) on the posterior variance (mean)? Can you reason about the impact of the variance of the observation noise on the posterior variance? Can you reason about the impact of the number of training observations on the posterior variance and mean? 
 - ***(Concept)*** Can you reason about the impact of the prior variance (mean) on the posterior **predictive** variance (mean)? Can you reason about the impact of the variance of the observation noise on the posterior **predictive** variance? Can you reason about the impact of the number of training observations on the posterior **predictive** variance and mean? 

2. **Inference**
  - ***(Math)*** Can you define *inference* for Bayesian models -- that is, what object(s) are we interested in learning?
  - ***(Concept)*** Can you describe what is challenging about Bayesian inference (e.g. consider how to compute the posterior predictive, how to infer the posterior when the prior and the likelihood aren't conjugate etc)?
  - ***(Math)*** Can you give an example of a Bayesian model with non-conjugate prior and likelihood?
  - ***(Concept)*** Can you describe the two strategies we have for performing (approximate) Bayesian inference when the posterior is intractable?
  - ***(Math)*** Can you define what we mean by sampling from a target pdf?
  - ***(Concept)*** Can you describe what is hard about sampling?
  - ***(Concept)*** Can you describe our general strategy for finding ways to sample from complex distributions (i.e. how do we build up to sampling from complex distributions by understanding how to sample from simple distributions)?
  - ***(Math)*** Can you define the two common point estimates of the posterior (posterior mode and posterior mean)? 
  - ***(Concept)*** Can you say which point estimate is more commonly computed and why?
  - ***(Concept)*** Can you explain why reducing the posterior to point estimates can be useful? Can you explain when reducing the posterior to each point estimate would be inappropriate?
  - ***(Math)*** Can you derive the equivalence of the MAP of Bayesian linear regression --with Gaussian likelihood and Gaussian prior-- to $\ell_2$ regularized maximium likelihood regression? Can you derive the equivalence of the MAP of Bayesian linear regression --with Gaussian likelihood and Laplace prior-- to $\ell_1$ regularized maximium likelihood regression?
  - ***(Math)*** Can you state in plain English the Berstein-von Mises Theorem and explain why we care?

3. **Model Comparison** 
  - ***(Concept)*** Since point estimates of Bayesian posteriors are often equivalent to solutions of regularized MLE regression, what is the point of setting up a full Bayesian model -- that is, why not always do regularized MLE regression?
  - ***(Concept)*** Can you describe where the predictive uncertainty in MLE regression comes from? Can you describe where the predictive uncertainty in Bayesian regression comes from? 
  - ***(Concept)*** What are the pro's and con's of interpreting the predictive uncertainty in MLE regression? What are the pro's and con's of interpreting the predictive uncertainty in Bayesian regression?
  - ***(Concept)*** Can you compare Bayesian and MLE models in terms of their computational tractability? In terms of computational tractability, are there situations where I prefer Bayesian regression over MLE regression? Are there situations where I prefer MLE regression?
  - ***(Concept)*** Can you compare Bayesian and MLE models in terms of their bias and variance:
     - where does the bias of a Bayesian model come from? Where does the bias of an MLE model come from?
     - how do we manage overfitting in MLE models? How do we manage overfitting in Bayesian models?
  
**Examples in Literature:**
- Not so long ago, Bayesian inference was hugely controversial! There are some fundamental philosophical and practical differences between these two schools of thought: [Comparison of Frequentist and Bayesian Inference](https://ocw.mit.edu/courses/mathematics/18-05-introduction-to-probability-and-statistics-spring-2014/readings/MIT18_05S14_Reading20.pdf). Yes, the controversy is deeply ***philosophical***: [The False Dilemma: Bayesian vs. Frequentist](https://www.colorado.edu/amath/sites/default/files/attached-files/vallverdu08.pdf).
- In the era of big data and deep models, is there any room for Bayesian thinking? Yes, combining the desirable features of deep learning and Bayesian models is a subfield of ML called Deep Bayes, for example: [Being Bayesian, Even Just a Bit, Fixes Overconfidence in ReLU Networks](https://arxiv.org/abs/2002.10118)
- But inference in Deep Bayes can be incredibly difficult, for example: [You can take a whole class on make inference tractable and usable](https://onefishy.github.io/am207/schedule.html). There is an entire yearly conference devoted to it: [Advances in Approximate Bayesian Inference](http://approximateinference.org).
