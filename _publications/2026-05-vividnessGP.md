---
title: "A novel approach to characterizing the visual dimensions of mental imagery vividness using Gaussian process regression"
collection: publications
permalink: /publications/vss2026-vividness-gp
date: 2026-05-15
venue: 'Vision Sciences Society Annual Meeting'
paperurl: 'https://www.visionsciences.org/presentation/?id=4213'
citation: 'A novel approach to characterizing the visual dimensions of mental imagery vividness using Gaussian process regression (2026) Yurdakul O.C., Huang X., Shen A., Olsson E., Ekhlasi A., Klímová M., Morales J.*, Peters M.A.K.* Vision Sciences Society Annual Meeting'
---

## Poster Supplements - _Last updated: 2026.05.15_

This is a living document where I will add any supplementary information/results about my poster, which you can find here.

<iframe width="100%" height="600" src="/files/vss2026_ogulCanYurdakul.pdf"></iframe>

### Animated Manifolds

<p style="text-align:center">
  <select id="gif-select">
    <option value="/images/vss2026_vividness_gp/label0.gif">Supersubject</option>
    <option value="/images/vss2026_vividness_gp/label1.gif">Group 1 (N = 83)</option>
    <option value="/images/vss2026_vividness_gp/label2.gif">Group 2 (N = 30)</option>
    <option value="/images/vss2026_vividness_gp/label3.gif">Group 3 (N = 17)</option>
    <option value="/images/vss2026_vividness_gp/label4.gif">Group 4 (N = 7)</option>
    <option value="/images/vss2026_vividness_gp/label5.gif">Group 5 (N = 5)</option>
    <option value="/images/vss2026_vividness_gp/label-1.gif">Group -1 (N = 14)</option>
  </select>
  <br><br>
  <img id="gif-display" src="/images/vss2026_vividness_gp/label0.gif" width="75%" />
</p>

<p style="text-align:center">
  <select id="gif-select-2">
    <option value="/images/vss2026_vividness_gp/difference_label1.gif">Subject 11 - Supersubject</option>
    <option value="/images/vss2026_vividness_gp/difference_label2.gif">Subject 136 - Supersubject</option>
    <option value="/images/vss2026_vividness_gp/difference_label3.gif">Subject 5 - Supersubject</option>
    <option value="/images/vss2026_vividness_gp/difference_label4.gif">Subject 137 - Supersubject</option>
    <option value="/images/vss2026_vividness_gp/difference_label5.gif">Subject 96 - Supersubject</option>
    <option value="/images/vss2026_vividness_gp/difference_label-1.gif">Subject 181 - Supersubject</option>
  </select>
  <br><br>
  <img id="gif-display-2" src="/images/vss2026_vividness_gp/difference_label1.gif" width="100%" />
</p>

<script>
  document.addEventListener('DOMContentLoaded', function() {
    document.getElementById('gif-select').addEventListener('change', function() {
      document.getElementById('gif-display').src = this.value;
    });
    document.getElementById('gif-select-2').addEventListener('change', function() {
      document.getElementById('gif-display-2').src = this.value;
    });
  });
</script>

### Clustering Results

### Gaussian Processes

A Gaussian process (GP) is a collection of random variables such that any finite collection of them has a jointly Gaussian distribution, so is completely specified by its mean and covariance. For a real-valued GP function $f(\vec x)$, denoted $f(\vec x) \sim \mathcal{GP}\left(m(\vec x),\, k(\vec x, \vec x')\right)$, the mean and covariance functions are defined as

$$
\begin{align}
    m(\vec x) &= \mathbb E\left[f(\vec x)\right] \\
    k(\vec x, \vec x') &= \mathbb E \left[\left(f(\vec x) - m(\vec x)\right)\left(f(\vec x') - m(\vec x')\right)\right]
\end{align}  
$$

where $k(\vec x, \vec x')$ is called the kernel function.

To formulate the regression setting, let $f$ be an unknown function from which we obtain observations $y_i$ at input locations $\vec x_i$ for $i = 1, ..., N$, via the noisy model

$$
y_i = f(\vec x_i) + \epsilon_i
$$

where $\epsilon_i \sim \mathcal{N} \left(0,\, \sigma_\epsilon^2\right)$ is the independent identically distributed additive noise and $f$ is the unknown function of interest. Within the GP regression framework, $f$ is taken to be a GP independent of $\epsilon$, commonly with prior mean 0 for convenience. This allows us to take an arbitrary query location $\vec x^\ast$ at which we would like to estimate the function value, and write the joint distribution

$$
\begin{bmatrix}f(\vec x^\ast) \\ \vec y \end{bmatrix} \sim \mathcal{N}\left(\begin{bmatrix}0 \\ \vec 0\end{bmatrix},\, \begin{bmatrix}k(\vec x^\ast, \vec x^\ast) & k(\vec X, \vec x^\ast)^{\intercal} \\ k(\vec X, \vec x^\ast) & k(\vec X, \vec X) + \sigma_\epsilon^2 I_N\end{bmatrix}\right)
$$

where $\vec y$ denotes the vector of noisy observations, $k(\vec X, \vec x^\ast)$
denotes the column vector of cross correlations $k(\vec x^\ast, \vec x_i)$, $k(\vec X, \vec X)$ denotes the correlation matrix with entries $k(\vec x_i, \vec x_j)$, and $I_N$ is the identity matrix of size $N$. By the Gaussian conditioning rule, the conditional distribution of $f(\vec x^\ast)$ on the observations becomes $\mathcal{N}\left(\mu(\vec x^\ast),\, \sigma^2(\vec x^\ast)\right)$ where
$$
\begin{align}
    \mu(\vec x^\ast) &= k(\vec x_i, \vec x^\ast)^{\intercal} \left[ k(\vec X, \vec X) + \sigma_\epsilon^2 I_N \right]^{-1} \vec y, \\
    \sigma^2(\vec x^\ast) &= k(\vec x^\ast, \vec x^\ast) - k(\vec X, \vec x^\ast)^{\intercal} \left[ k(\vec X, \vec X) + \sigma_\epsilon^2 I_N \right]^{-1} k(\vec X, \vec x^\ast).
\end{align}
$$

The choice of a kernel function is essential for GPs since it determines the form and properties of the function $f$. One commonly used kernel function (and the one used in this work) is the squared exponential kernel, defined as

$$
k(\vec x, \vec x') = \sigma_f^2 \exp\left(-\frac{\|{\vec x - \vec x'\|^2}}{2\ell^2}\right)
$$

where the signal variance $\sigma_f^2$ and the length-scale $\ell$ are hyperparameters of interest. One assumption of this kernel function is that it effectively assumes that the correlation structure is identical across the dimensions of $\vec x$, which need not be true in general. One improvement/generalization we can make is to have separate length scales for each dimension, which gives us the kernel function

$$
k(\vec x, \vec x') = \sigma_f^2 \exp\left(\frac{-1}{2} \sum_{d = 1}^D\frac{(\vec x - \vec x')^2}{\ell_d^2}\right)
$$

where $\ell_d$ is the length scale corresponding to the feature $d$ and $d = 1,..., D$ indexes the dimensions of the feature vector $\vec x \in \mathbb R^D$. 

<!-- <p style="text-align:center">
    <img src="/images/vss2026_vividness_gp/supersubject.gif" width="75%" />
    <br> <em size="-2">Supersubject vividness manifolds.</em>
</p>

<p style="text-align:center">
    <img src="/images/vss2026_vividness_gp/individual10.gif" width="75%" />
    <br> <em size="-2">Subject 10 vividness manifolds.</em>
</p>

<p style="text-align:center">
    <img src="/images/vss2026_vividness_gp/deltaV10.gif" width="75%" />
    <br> <em size="-2">Subject 10-Supersubject difference manifolds.</em>
</p> -->

<!--  -->