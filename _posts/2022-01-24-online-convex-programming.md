---
layout: post
title: "Online Convex Programming and Generalized Inﬁnitesimal Gradient Ascent"
date: 2022-01-24
description: [This is a brief review of paper "Online Convex Programming and Generalized Inﬁnitesimal Gradient Ascent",
It is also the first paper review assignment of SDSC 8014.]
categories: [Review, Assignments for SDSC8014]
keywords: Online Convex Programming, Online Optimization, review
mathjax: true
---

In this paper, the author presented effective gradient descent algorithms to solve the online convex programming problem. 
The author fisrt eastablished a Greedy Projection algorithm, and prove the average regret of Greedy Projection approaches zero. 
Then they defined a different Lazy Projection algorithm which also had a well performance. The repeated games is established 
as online linear programming problems in their work, and the application of their algorithm is universally consistent. 
Fianlly, they showed how to translate algorithms for mixing experts into algorithms for online convex programs.

## Contribution

The main contribution of this work is to introduce a general online convex programming problem, and present a simple but 
efficient gradient desent algoritm which has many advantage:

- Gradient descent is a simple, natural algorithm that is widely used and this algorithm can handle an arbitrary 
sequence of convex functions, that is more general than the experts setting.

- The regret of the Greedy Projection algorithm and Lazy Projection algorithm in this paper hava been proved to be bounded.

- Repeated games can be established as online linear programming problems, and their algorithm is extended to games with 
an arbitrary number of actions and can be proved universally consistent.

- Compared to the expert algorithms, the bounds on the performance of this algorithm are better.

## Content of the article

### Section 2

In this section, the author introduced some defination of online convex programming problem, and then presented the frist 
algorithm,
![Algorithm 1](/assets/images/22-01-24-online-convex-programming/algorithm1.png)
The regret of this Greedy Projection algorithm is:


## Weakness and improvement
The algorithm in this work assumed the gradient is easy to obtain, so it is not suitable for situations where it is difficult 
to find a gradient. On the other hand, this gradient descent based algorithm allows us to extend this method for more efficient 
result, for instance, choose a flexible learning rate.