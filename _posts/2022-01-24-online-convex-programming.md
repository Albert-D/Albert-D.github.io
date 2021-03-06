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

![Theorem 1](/assets/images/22-01-24-online-convex-programming/theorem1.png)

Then they propsoed a diﬀerent algorithm that performs suprisingly well,

![Algorithm 2](/assets/images/22-01-24-online-convex-programming/algorithm2.png)

### Section 3

In this section, they establish that repeated games are online linear programming problems, and an application of our algorithm 
is universally consistent.  
Firstly, they formulated a Repeated Game as an Online Linear Program, and used this Generalized Inﬁnitesimal Gradient Ascent 
(GIGA) algorithm to solve the problem,

![Algorithm 3](/assets/images/22-01-24-online-convex-programming/algorithm3_1.png)
![Algorithm 3](/assets/images/22-01-24-online-convex-programming/algorithm3_2.png)

and they prove that GIGA is universally consistent,

![Lemma 1](/assets/images/22-01-24-online-convex-programming/lemma1.png)

### Section 4
This section shows how one can naively translate algorithms for mixing experts into algorithms for online linear programs, 
and online linear programming algorithms into algorithms for online convex programs.  
An **Online Linear Programming Algorithm** (OLPA) can be constructed from an **Expert Algorithm** (EA), as follows:

![Algorithm 5](/assets/images/22-01-24-online-convex-programming/algorithm5.png)

Then we can Convert an OLPA to an Online Convex Programming Algorithm in Exact way or in Approximate way.


## Weakness and improvement
The algorithm in this work assumed the gradient is easy to obtain, so it is not suitable for situations where it is difficult 
to find a gradient. On the other hand, this gradient descent based algorithm allows us to extend this method for more efficient 
result, for instance, choose a flexible learning rate.