---
layout: definition
mathjax: true

author: "Joram Soch"
affiliation: "BCCN Berlin"
e_mail: "joram.soch@bccn-berlin.de"
date: 2020-01-22 10:58:00

title: "Moment-generating function"
chapter: "General Theorems"
section: "Probability theory"
topic: "Probability distributions"
definition: "Moment-generating function"

sources:
  - authors: "Wikipedia"
    year: 2020
    title: "Moment-generating function"
    in: "Wikipedia, the free encyclopedia"
    pages: "retrieved on 2020-01-22"
    url: "https://en.wikipedia.org/wiki/Moment-generating_function#Definition"

def_id: "D2"
shortcut: "mgf"
username: "JoramSoch"
---


**Definition:**

1) The moment-generating function of a random variable $X \in \mathbb{R}$ is

$$ \label{eq:mgf-var}
M_X(t) = \mathrm{E} \left[ e^{tX} \right], \quad t \in \mathbb{R} \; .
$$

2) The moment-generating function of a random vector $X \in \mathbb{R}^n$ is

$$ \label{eq:mgf-vec}
M_X(t) = \mathrm{E} \left[ e^{t^\mathrm{T}X} \right], \quad t \in \mathbb{R}^n \; .
$$