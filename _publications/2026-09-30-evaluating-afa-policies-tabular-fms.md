---
title: "Evaluation of Active Feature Acquisition Policies with Tabular Foundation Models"
collection: publications
category: preprints
permalink: /publication/2026-09-30-evaluating-afa-policies-tabular-fms
excerpt: 'Scoring feature acquisitions by the total predictive entropy of a prior-data fitted network introduces an epistemic bias that penalizes sparsely observed features. We target the posterior expected (aleatoric) entropy instead, which reduces value estimation bias and yields credible intervals with strong empirical coverage.'
date: 2026-09-30
status: 'Under review'
---

Active feature acquisition learns policies that sequentially acquire features to maximize information about a target variable. We study how to learn and evaluate such policies from finite offline data using **prior-data fitted networks (PFNs)** — off-the-shelf models that output posterior predictive distributions without task-specific training.

Our central observation concerns what happens when the offline data covers features unevenly. Under imbalanced coverage, using total predictive entropy as a reward creates an *epistemic bias* that penalizes acquiring sparsely observed features: the reward conflates epistemic uncertainty, which arises from a lack of offline data, with aleatoric uncertainty, which arises from features that are genuinely uninformative. A policy scored this way learns to avoid exactly the features it has the least evidence about.

To address this, we evaluate feature acquisitions against the **posterior expected (aleatoric) entropy** rather than the total predictive entropy a PFN outputs.

Empirical evaluations on synthetic and real-world datasets show that this approach consistently reduces value estimation bias and yields credible intervals with strong empirical coverage, which can translate to improved downstream policy selection.
