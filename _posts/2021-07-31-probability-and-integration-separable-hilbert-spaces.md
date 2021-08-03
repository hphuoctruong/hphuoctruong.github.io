---
title: Probability and Integration on Separable Hilbert Spaces
author: Phuoc-Truong Huynh
date: 2021-07-31 12:00:00 +0200
categories: [Seminar]
tags: [inverse problems, bayesian, optimization]
toc: true
math: true
pin: true
---

Let $$E,F$$ be separable Banach spaces.

## Gaussian measure.

Recall that for every measure $$\mu$$ on $$E$$ and $$f:E \to F$$ is measurable, the push-forward measure $$f_* \mu$$ is defined as

$$ f_*\mu (B) = \mu \left(f^{-1}(B) \right),\quad \forall B \in \mathbb{B}(F).$$

**Definition (Gaussian measure).** A Borel measure on $$E$$ is said to be a [Gaussian measure](https://en.wikipedia.org/wiki/Gaussian_measure){:target="_blank"}. if for every continuous linear functional $$f: E \to \mathbb{R}$$, the push-forward measure $$f_* \mu$$ is a Gaussian measure on $$\mathbb{R}.$$

**Definition (Mean).** Let $$\mu$$ be a probability measure on $$E$$. The mean of $$\mu$$ is defined by

$$m_{\mu} := \int_{E} x d\mu(x).$$

**Definition (Covariance operator).** The [covariance operator](https://en.wikipedia.org/wiki/Covariance_operator){:target="_blank"} $$C_{\mu}$$ of $$\mu$$ is $$C_{\mu}: E^* \times E^* \to \mathbb{R}$$ defined by

$$C_{\mu}(u^*,v^*) = \int_{E}\langle u^*,x - m_{\mu}\rangle_{E^*,E} \langle v^*,x - m_{\mu}\rangle_{E^*,E}d\mu(x)$$

for every $$u^*,v^* \in E$$.

In other words, $$C_{\mu} \in E^* \otimes E^*$$.

**Hilbert space.** We assume that $$H$$ is a Hilbert space. In this case, for centered measure $$\mu$$ on $$H$$, the covariance operator can be seen as an operator $$C_{\mu}: H \to H$$ defined by

$$\langle C_{\mu} u, v \rangle_{H} = \int_{H} \langle u, x \rangle_H \langle v, x \rangle_H d\mu(x).$$

It can be seen that $$C_{\mu}$$ is positive, self-adjoint and of trace class. In particular, $$C_{\mu}$$ is a compact operator.

**Theorem.** Let $$\mu$$ be a centered Gaussian measure on $$H$$. Then $$C_{\mu}: H \to H$$ is of trace class and

$$\text{tr}(C_{\mu}) = \int_{H} \|x\|^2 d\mu(x).$$

Conversely, if $$K : H \to H$$ is positive, self-adjoint and of trace class, then there exists a Gaussian measure $$\mu$$ on $$H$$ such that $$C_{\mu} = K.$$

**Definition (Cameron-Martin space).** Let $$C_{\mu}$$ be a positive, self-adjoint operator on $$H$$.

The Cameron-Martin space is defined as the completion of $$\text{range}(C_{\mu}^{\frac{1}{2}})$$ with the inner product

$$\langle u, v \rangle_{\mu} := \langle u, v \rangle_H + \langle C_{\mu}^{-\frac{1}{2}} u, C_{\mu}^{-\frac{1}{2}} v \rangle_H,\quad u,v \in \text{range}(C_{\mu}^{\frac{1}{2}}).$$

**Example.** 
