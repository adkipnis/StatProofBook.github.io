---
layout: proof
mathjax: true

author: "Joram Soch"
affiliation: "BCCN Berlin"
e_mail: "joram.soch@bccn-berlin.de"
date: 2019-05-02 16:30:00

title: "Partition of the log model evidence into accuracy and complexity"
chapter: "Model Selection"
section: "Bayesian model selection"
topic: "Log model evidence"
theorem: "Partition into accuracy and complexity"

proof_id: "P3"
shortcut: "lme-anc"
username: "JoramSoch"
---


**Theorem:** The log model evidence can be partitioned into accuracy and complexity

$$ \label{eq:LME}
\mathrm{LME}(m) = \mathrm{Acc}(m) - \mathrm{Com}(m)
$$

where the accuracy term is the posterior expectation of the log-likelihood function

$$ \label{eq:Acc}
\mathrm{Acc}(m) = \left\langle p(y|\theta,m) \right\rangle_{p(\theta|y,m)}
$$

and the complexity penalty is the Kullback-Leibler divergence of posterior from prior

$$ \label{eq:Com}
\mathrm{Com}(m) = \mathrm{KL} \left[ p(\theta|y,m) \, || \, p(\theta|m) \right] \; .
$$


**Proof:** We consider Bayesian inference on data $y$ using model $m$ with parameters $\theta$. Then, Bayes' theorem makes a statement about the posterior distribution, i.e. the probability of parameters, given the data and the model:

$$ \label{eq:AnC-s1}
p(\theta|y,m) = \frac{p(y|\theta,m) \, p(\theta|m)}{p(y|m)} \; .
$$

Rearranging this for the model evidence, we have:

$$ \label{eq:AnC-s2}
p(y|m) = \frac{p(y|\theta,m) \, p(\theta|m)}{p(\theta|y,m)} \; .
$$

Logarthmizing both sides of the equation, we obtain:

$$ \label{eq:AnC-s3}
\log p(y|m) = \log p(y|\theta,m) - \log \frac{p(\theta|y,m)}{p(\theta|m)} \; .
$$

Now taking the expectation over the posterior distribution yields:

$$ \label{eq:AnC-s4}
\log p(y|m) = \int p(\theta|y,m) \log p(y|\theta,m) \, \mathrm{d}\theta - \int p(\theta|y,m) \log \frac{p(\theta|y,m)}{p(\theta|m)} \, \mathrm{d}\theta \; .
$$

By definition, the left-hand side is the log model evidence and the terms on the right-hand side correspond to the posterior expectation of the log-likelihood function and the Kullback-Leibler divergence of posterior from prior

$$ \label{eq:LME-AnC}
\mathrm{LME}(m) = \left\langle p(y|\theta,m) \right\rangle_{p(\theta|y,m)} - \mathrm{KL} \left[ p(\theta|y,m) \, || \, p(\theta|m) \right]
$$

which proofs the partition given by (\ref{eq:LME}).

$$\tag*{$\blacksquare$}$$


**Dependencies:**

- [Bayes' theorem](/Proof/bayes-th.html)
- derivation of the log model evidence
- expectation with respect to a random variable
- Kullback-Leibler divergence of two random variables


**Source:**

- Penny et al. (2007): "Bayesian Comparison of Spatially Regularised General Linear Models". *Human Brain Mapping*, vol. 28, pp. 275–293.
- Soch et al. (2016): "How to avoid mismodelling in GLM-based fMRI data analysis: cross-validated Bayesian model selection". *NeuroImage*, vol. 141, pp. 469–489.