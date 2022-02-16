---
layout: post
title: "Dual Averaging Method for Regularized Stochastic Learning and Online Optimization"
date: 2022-01-24
description: [This is a brief review of paper "Dual Averaging Method for Regularized Stochastic Learning and Online Optimization",
It is also the second paper review assignment of SDSC 8014.]
categories: [Review, Assignments for SDSC8014]
keywords: Online Convex Programming, Online Optimization, review
mathjax: true
---

This article develops a new online algorithm, the regularized dual averaging (RDA) method, which can explicitly exploit the regularization
structure in an online setting. This method can exploits the full regularization structure at each online iteration and adjusts 
the learning variables by solving a simple optimization problem that involves the whole regularization term.

## Contribution
This paper proposes a new algorithm to solve the online learning problem with regularization term.

 - Traditional online algorithms, such as stochastic gradient descent (SGD), has limited capability of exploiting problem structure
 in solving regularized learning problems, but the RDA method in this paper can exploit the regularization structure.

 - Comparing with other method, the RDA method can generate much more sparse solutions in solving the online problem with a regularization term.

 - The computational complexity per iteration is O(n), the same as the SGD method, but the RDA method can converge to the optimal
 solution with a better optimal rate.

## Content of the article

### Section 2
This section presents the generic RDA method (Algorithm 1) for solving regularized stochastic learning and online 
optimization problems, and give some concrete examples, as showed below.

![Algorithm 1](/assets/images/22-02-16-RDA/algorithm1.png)

### Section 3
First, they give bounds on the regert $R_t(w)$ in regularized online optimization.

![Theorem 1](/assets/images/22-02-16-RDA/theorem1.png)

