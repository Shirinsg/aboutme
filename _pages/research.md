---
layout: page
permalink: /research/
title: research
description: Reliable learning-based solvers for imaging inverse problems.
nav: true
nav_order: 1
---

<!-- _pages/research.md
     Each theme lists the papers whose BibTeX entry has `research = {<theme>}` in _bibliography/papers.bib.
     To move a paper to another theme, change that field. -->

Modern imaging systems increasingly rely on learned priors (denoisers, diffusion models, and other generative models) to reconstruct images from incomplete or noisy measurements. These methods are powerful, but they are trained on one distribution and deployed on another. My research asks **when such solvers can be trusted, how to detect when they cannot, and how to design new ones with guarantees.**

---

### Robustness under model mismatch

What happens to a learned reconstruction method when its prior or measurement model does not match the data it sees at test time? I study plug-and-play (PnP) and deep equilibrium architectures under mismatched priors and forward models. I characterize how mismatch affects convergence and reconstruction error, and develop lightweight adaptation strategies, such as domain adaptation and test-time training, that recover performance with little target data.

<div class="publications">
{% bibliography --group_by none --query @*[research=mismatch]* %}
</div>

---

### Detecting and measuring distribution shift

Before correcting for a shift, one has to know it is there. I develop methods that use diffusion models to **detect out-of-distribution inputs and estimate distribution shift directly from measurements**, without access to clean ground-truth images. These include covariance-based OOD scores and measurement-domain divergence estimates.

<div class="publications">
{% bibliography --group_by none --query @*[research=shift]* %}
</div>

---

### Diffusion and generative priors for inverse problems

I work on using diffusion, flow-based, and other generative models as priors for imaging problems such as phase retrieval, Poisson denoising, and video restoration. This includes models that learn directly in the measurement domain, one-step posterior sampling for noisy measurements, and flow-based reconstruction through regularized minimization.

<div class="publications">
{% bibliography --group_by none --query @*[research=generative]* %}
</div>

---

### Optimization and convergence theory

Underlying all of this is optimization. I analyze the convergence of nonconvex PnP-ADMM with MMSE denoisers, develop closed-form proximal operators, and study analysis-based and block-coordinate PnP methods for blind and structured inverse problems.

<div class="publications">
{% bibliography --group_by none --query @*[research=optimization]* %}
</div>

---

### Looking ahead: flow matching with guarantees

Flow matching has emerged as a flexible alternative to diffusion models, and it has deep connections to optimization and minimization theory. My next goal is to exploit those connections to design **principled flow-based solvers for imaging inverse problems with provable guarantees**, combining the expressiveness of modern generative models with the reliability of classical optimization.
