# Course Project Description

The aim of the project is to acclimate you to the process of conducting research in statistical modeling or machine learning: 1) tackle an intimidatingly general problem 2) narrow the scope to a specific set of parameters to study 3) replicate existing literature studying these parameters 4) innovate on top of existing work incrementally, and 5) consider the wider socio-technological impact of your work.

Students who make meaningful novel or insightful contributions in their course projects have the opportunity to develop their project into a workshop or conference publication during the Spring 2020 semester. Examples of publications from AM207 Fall 2019:

1. [BaCOUn: Bayesian Classifers with Out-of-Distribution Uncertainty](https://arxiv.org/pdf/2007.06096.pdf)
2.  [Learned Uncertainty-Aware (LUNA) Bases for Bayesian Regression using Multi-Headed Auxiliary Networks](https://arxiv.org/pdf/2006.11695.pdf)
3.[CRUDS: Counterfactual Recourse Using Disentangled Subspaces](http://whi2020.online/static/pdfs/paper_74.pdf)

### Grading
Your grade is based on:

1.  How well your deliverable satisfies the project specifications (described below)
2.  Your progress leading up to the final deliverable. There will be a series of check points with your project TF and instructor through out the semester. Your final grade will account for how much progress you've made by each check point.

### Instructions

 **Team:** Form a team of 2-4 people
 
**Topic:** Choose a paper from the approved list of papers (we are limiting 2 teams per paper, on a first-come-first-serve basis). You may propose a paper, but it must be approved by your instructor.

**Mentoring:** You will have a designated TF for your project and you are welcomed to schedule meetings between your team and the instructor.

**Project deliverable: **A well-formatted Jupyter notebook (optimized for readability) containing:

    1.   **Clear exposition of : **
        *   _**Problem statement**_ - what is the problem the paper aims to solve?
        *   _**Context/scope**_ - why is this problem important or interesting?
        *   _**Existing work**_ - what has been done in literature?
        *   _**Contribution**_ - what is gap in literature that the paper is trying to fill? What is the unique contribution
        *   _**Technical content (high level)**_ - what are the high level ideas behind their technical contribution
        *   _**Technical content (details)**_ - **_highlight (not copy and paste entire sections)_ **the relevant details that are important to focus on (e.g. if there's a model, define it; if there is a theorem, state it and explain why it's important, etc).
        *   _**Experiments**_ - which types of experiments were performed? What claims were these experiments trying to prove? Did the results prove the claims?
        *   _**Evaluation (your opinion)**_ - do you think the work is technically sound? Do you think the proposed model/inference method is practical to use on real data and tasks? Do you think the experimental section was strong (there are sufficient evidence to support the claims and eliminate confounding factors)?
        *   _**Future work (for those interested in continuing research in a related field)**_ - do you think you can suggest a concrete change or modification that would improve the existing solution(s) to the problem of interest? Try to implement some of these changes/modifications.
        *   _**Broader Impact**_ - how does this work potentially impact (both positively and negatively) the broader machine learning community and society at large when this technology is deployed? In the applications of this technology, who are the potentially human stakeholders? What are the potential risks to the interest of these stakeholders in the failure modes of this technology? Is there potential to exploit this technology for malicious purposes?

Your exposition should focus on summarization and highlighting (aiming for an audience of peers who have taken AM207). There is no point rewording the paper itself. Reorganize and explain the ideas in a way that makes sense to you, that features the most salient/important aspects of the paper, that demonstrates understanding and synthesis.

2.  **Code:**
        *   At least one clear working pedagogical example demonstrating the problem the paper is claiming to solve. 
        *   At lease a bare bones implementation of the model/algorithm/solution (in some cases, you may be able to make assumptions  to simplify the model/algorithm/solution with the approval of your instructor)
        *   Demonstration on at least one instance that your implementation solves the problem.
        *   Demonstration on at least one instance the failure mode of the model/algorithm/solution, with an explanation for why failure occurred (is the dataset too large? Did you choose a bad hyper parameter?). The point of this is to point out edge cases to the user.

You are welcome to study any code that is provided with the paper, you are however not allowed to copy code. Your implementation must be your own. If a public repo is available for your paper, you are encouraged to first try reproducing some results using the authors code -- this will give you an idea of how their algorithm/model works.

**Examples of Project from Fall 2019:**

[Github repo of Fall 2019 AM207 projects](https://github.com/onefishy/am207_fall19_projects)

### List of Pre-Approved Papers

#### I. Deep Generative Models & Density Estimation

1. SUMO: Unbiased Estimation of Log Marginal Probability for Latent Variable Models](https://arxiv.org/pdf/2004.00353.pdf)
        2.  [The Information Autoencoding Family: A Lagrangian Perspective on Latent Variable Generative Models](http://auai.org/uai2018/proceedings/papers/361.pdf)
        3.  [Lagging Inference Networks and Posterior Collapse in Variational Autoencoders](https://arxiv.org/pdf/1901.05534.pdf)
        4.  [Reinterpreting Importance-Weighted Autoencoders](https://arxiv.org/pdf/1704.02916.pdf)
        5.  [CRUDS: Counterfactual Recourse Using Disentangled Subspaces](http://whi2020.online/static/pdfs/paper_74.pdf)
        6.  [Failure Modes of Variational Autoencoders and Their Effects on Downstream Tasks](https://arxiv.org/pdf/2007.07124.pdf)
        7.  [Debiasing Evidence Approximations:on Importance-weighted Autoencoders And Jackknife Variational Inference](https://openreview.net/pdf?id=HyZoi-WRb)
        8.  [Amortized Inference Regularization](https://papers.nips.cc/paper/7692-amortized-inference-regularization.pdf)
        9.  [Flows for simultaneous manifold learning and density estimation](https://arxiv.org/pdf/2003.13913.pdf)
        10.  [Why Normalizing Flows Fail to Detect Out-of-Distribution Data](https://arxiv.org/pdf/2006.08545.pdf)

#### II. Deep Bayesian Models

1.  [Rethinking Parameter Counting in Deep Models: Effective Dimensionality Revisited](https://arxiv.org/pdf/2003.02139.pdf)
        2.  [On the Expressiveness of Approximate Inference in Bayesian Neural Networks](https://arxiv.org/pdf/1909.00719.pdf)
        3.  [Bayesian Deep Learning and a Probabilistic Perspective of Generalization](https://arxiv.org/pdf/2002.08791.pdf)
        4.  [Learned Uncertainty-Aware (LUNA) Bases for Bayesian Regression using Multi-Headed Auxiliary Networks](https://arxiv.org/pdf/2006.11695.pdf)
        5.  [BaCOUn: Bayesian Classifers with Out-of-Distribution Uncertainty](https://arxiv.org/pdf/2007.06096.pdf)
        6.  [How Good is the Bayes Posterior in Deep Neural Networks Really?](https://arxiv.org/pdf/2002.02405.pdf)
        7.  [Expressive Priors in Bayesian Neural Networks: Kernel Combinations and Periodic Functions](http://auai.org/uai2019/proceedings/papers/25.pdf)
        8.  [Simple and Principled Uncertainty Estimation with Deterministic Deep Learning via Distance Awareness](http://www.gatsby.ucl.ac.uk/~balaji/udl2020/accepted-papers/UDL2020-paper-057.pdf)

#### III. Deep Ensembles

1.  [A Simple Baseline for Bayesian Uncertainty in Deep Learning](https://arxiv.org/pdf/1902.02476.pdf)
        2.  [Deep Ensembles: A Loss Landscape Perspective](https://arxiv.org/pdf/1912.02757.pdf)
        3.  [Pitfalls of In-domain Uncertainty Estimation and Ensembling in Deep Learning](https://openreview.net/pdf?id=BJxI5gHKDr)
        4.  [Accurate Uncertainty Estimation and Decomposition in Ensemble Learning](http://www.columbia.edu/~jwp2128/Papers/LiuPaisleyetal2019.pdf)

#### IV. Deep Models with Uncertainty, Evaluation of Uncertainty

1.  [Uncertainty Estimation Using a Single Deep Deterministic Neural Network](https://arxiv.org/pdf/2003.02037.pdf)
        2.  [A Systematic Comparison of Bayesian Deep Learning Robustness in Diabetic Retinopathy Tasks](https://arxiv.org/pdf/1912.10481.pdf)
        3.  [Decomposition of Uncertainty in Bayesian Deep Learning for Efficient and Risk-sensitive Learning](http://proceedings.mlr.press/v80/depeweg18a/depeweg18a.pdf)
        4.  [Predict Responsibly: Increasing Fairness by Learning to Defer](https://openreview.net/pdf?id=SJUX_MWCZ)

#### V. Variational Inference

 1.  [Yes, but Did It Work?: Evaluating Variational Inferenc](https://arxiv.org/pdf/1802.02538.pdf)
        2.  [Sticking the Landing: Simple, Lower-Variance Gradient Estimators for Variational Inference](https://arxiv.org/pdf/1703.09194.pdf)
        3.  [The Thermodynamic Variational Objective](https://arxiv.org/pdf/1907.00031.pdf)

#### VI. Gaussian Processes

1.  [An Empirical Study on The Properties of Random Bases for Kernel Methods](https://papers.nips.cc/paper/6869-an-empirical-study-on-the-properties-of-random-bases-for-kernel-methods.pdf)
        2.  [Randomly Projected Additive Gaussian Processes for Regression](https://arxiv.org/pdf/1912.12834.pdf)
        3.  <span style="font-family: inherit;"><span style="font-size: 1rem;">[Bayesian Gaussian Process Latent Variable Model](http://proceedings.mlr.press/v9/titsias10a/titsias10a.pdf)
