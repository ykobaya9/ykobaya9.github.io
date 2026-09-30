---
title: "Learning-To-Measure: In-context Active Feature Acquisition"
collection: publications
category: conferences
permalink: /publication/2026-07-01-learning-to-measure
excerpt: 'We introduce Learning-to-Measure (L2M), a meta-learning framework that pairs reliable uncertainty quantification over unseen tasks with an uncertainty-guided acquisition agent, enabling in-context active feature acquisition without per-task retraining.'
date: 2026-07-01
venue: 'International Conference on Machine Learning (ICML)'
paperurl: 'https://arxiv.org/abs/2510.12624'
---

Active feature acquisition (AFA) is a sequential decision-making problem: which feature should we measure next in order to most improve a prediction for this particular instance? In practice, AFA methods must learn from retrospective data that carries systematic missingness in the features and offers only limited task-specific labels.

We propose **Learning-to-Measure (L2M)**, a meta-learning framework with two components: reliable uncertainty quantification over unseen tasks, obtained via autoregressive pre-training, and an uncertainty-guided acquisition agent that greedily maximizes conditional mutual information. L2M operates directly on datasets with retrospective missingness and solves the AFA task in-context, so no per-task retraining is required.

Across synthetic and real-world tabular benchmarks, L2M matches or surpasses task-specific baselines, with the largest gains under scarce labels and high missingness rates.
