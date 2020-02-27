---
layout: post
title: Existence of solutions
---
We consider the Cauchy problem
\begin{equation}\label{eq(1)}
x' = f(t,x(t)),\quad x(t_0) = x_0,
\end{equation}
where $f \in K_{loc}(I\times \mathbb{R}^n,\mathbb{R}^n), (t_0,x_0) \in I \times \mathbb{R}^n$.



> **Theorem 2.1.** Assume that $x = x(t)$ is a solution to \eqref{eq(1)} on an interval $(a,b) \subset I$. Then the following statements are equivalent:
> 1. $x$ is right extendable;
> 2. $b < \sup I$ and $\liminf_{t \to b^-} \lvert x(t) \rvert < \infty$;
> 3. $b < \sup I$ and $\lim_{t \to b^-} x(t)$ exists and is finite.

**Proof.**

$(1) \Rightarrow (2).$ Assume that $x$ is right extendable. Then there exists a solution $\widetilde{x}$ of \eqref{eq(1)} on $(a,\widetilde{b})$, where $\widetilde{b} > b$ and $\widetilde{x} = x$ on $(a,b)$. From this, we easily get $b < \widetilde{b} < \sup I$ and
\[ \liminf_{t \to b^-} \lvert x(t) \rvert = \lim_{t \to b^-} \lvert \widetilde{x}(t) \lvert = \rvert x(b) \lvert < \infty. \]

$(2) \Rightarrow (3).$ Since $\liminf_{t \to b^-} \rvert x(t) \lvert < \infty$, there exists an increasing sequence \( \left(t_n \right)_{n \in \mathbb{N}^*}\)  such that $t_n \to b$ and \( \lvert x(t_n) \rvert \to \alpha \in \mathbb{R}\). In particular, $(\rvert x(t_n)\lvert)_{n \in \mathbb{N}^*}$ is bounded, therefore there exists a $c \in \mathbb{R}^n$ such that 

$(3) \Rightarrow (1).$
