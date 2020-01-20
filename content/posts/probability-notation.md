---
title: "Probability Notation Cheatsheet"
date: 2020-01-20T09:36:35-05:00
draft: true
summary: Many presentations of probability theory rely on shorthand and intuitive, yet informal, definitions. This can be confusing for those of use just learning the subject or returning to it after years.  Here is a cheat sheet to help you along!
---

I recently found myself using Bayesian inference techniques to solve a
problem. Wanting to know more, I turned to the literature. But the notation
looked foreign to me. The symbols were recognizable, but I couldn't draw
meaning from their arrangements on the screen.

Familiarize yourself with the definitions of
[σ-algebras](https://en.wikipedia.org/wiki/%CE%A3-algebra#Definition) and
[probability
spaces](https://en.wikipedia.org/wiki/Probability_space#Definition). For the
rest of the article, assume that $(\Omega,\mathcal{F},\mathbb{P})$ is a
discrete probability space.

The first object on which I stubbed my math toes was the random variable and
its use to construct events. A discrete random variable is a function $X:
\Omega \rightarrow \mathbb{R}$. That's it.

Often, random variables are used to construct events that are passed to
$\mathbb{P}$. For example, $\mathbb{P}(X \leq 100)$. The notation $X \leq
100$ describes an event; an element in $\mathcal{F}$; a subset of $\Omega$.
The means the following.

> $X \leq 100 \triangleq \\{ \omega \in \Omega ~|~ X(\omega)  \leq 100 \\}$

More generally, if we have a constraint $C$ (like only evens or between 1 and
10), then the notation $C(X)$ is interpreted as the event $\\{ \omega \in
\Omega ~|~ C(X(\omega)) \\}$.

Similarly, use of natural languge connectives like "and" and "or" translate
to set operations. Consider $\mathbb{P}(H \leq 160 ~\mathrm{and}~ W \geq
60)$. The use of "and" refers to set intersection.

## Summary

Here is a list of common notational conventions for constructing events.

* For some $A \subseteq \mathbb{R}$,
  $X \in A \triangleq \\{ \omega \in \Omega ~|~ X(\omega) \in A \\}$.
* For some relation $R \subseteq \mathbb{R} \times \mathbb{R}$ and $t \in \mathbb{R}$,
  $X ~R~ t \triangleq \\{ \omega \in \Omega ~|~ (X(\omega), t) \in R \\}$. Common relations include $\leq$, $<$, $=$, etc.
* For events $A,B \in \mathcal{F}$, $\mathbb{P}(A ~\mathrm{and}~ B)$ is equivalent to $\mathbb{P}(A \cap B)$.

