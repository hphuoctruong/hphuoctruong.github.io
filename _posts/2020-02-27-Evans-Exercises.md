---
layout: post
title: Exercises and Solutions - Chapter 2 - Evans' PDEs
---



> **Exercise 2.9.** Denote $B_1^+$ the upper open half-ball \[ B_1^+:= \left\\{ x \in \mathbb{R}^N: \lvert x \rvert < 1 \text{ and } x_n > 0 \right\\}.\] Assume that $u \in C(\overline{B_1^+})$ is harmonic in $B_1^+$, with $u = 0$ . Set ABC
for every $x \in B_1$ and $\widetilde{x} = (x_1,\ldots, x_N)$. Show that $v$ is harmonic in $B_1$.

**Solution.**
\begin{align*}
  & \phi(x,y) = \phi \left(\sum_{i=1}^n x_ie_i, \sum_{j=1}^n y_je_j \right)
  = \sum_{i=1}^n \sum_{j=1}^n x_i y_j \phi(e_i, e_j) = \\
  & (x_1, \ldots, x_n) \left( \begin{array}{ccc}
      \phi(e_1, e_1) & \cdots & \phi(e_1, e_n) \\
      \vdots & \ddots & \vdots \\
      \phi(e_n, e_1) & \cdots & \phi(e_n, e_n)
    \end{array} \right)
  \left( \begin{array}{c}
      y_1 \\
      \vdots \\
      y_n
    \end{array} \right)
\end{align*}
