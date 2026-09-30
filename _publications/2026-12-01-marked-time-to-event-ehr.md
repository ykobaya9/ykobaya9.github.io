---
title: "One Loss to Rule Them All: Marked Time-to-Event for Structured EHR Foundation Models"
collection: publications
category: conferences
permalink: /publication/2026-12-01-marked-time-to-event-ehr
excerpt: 'We propose ORA, a marked time-to-event pre-training objective that jointly models event timing and the associated measurements, yielding more generalizable EHR representations than next-token prediction.'
date: 2026-12-01
venue: 'Advances in Neural Information Processing Systems (NeurIPS)'
paperurl: 'https://arxiv.org/abs/2602.00541'
---

Clinical events recorded in electronic health records (EHR) are irregularly sampled and mix discrete events with numerical measurements such as laboratory values or treatment dosages. The sequential form of EHR has led prior EHR foundation models to borrow next-token prediction from language modeling, but that objective fails to capture the full structure of the data: it ignores the timing between events and discards the continuous measurements attached to them.

We introduce **ORA**, a marked time-to-event pre-training objective that jointly models *when* the next event occurs and *what* value it carries.

Evaluating on MIMIC-IV and CUMC with both Transformer and Mamba backbones across 14 linear-probe tasks spanning classification, regression, and time-to-event prediction, we find that ORA consistently yields more generalizable representations than next-token prediction and than pre-training losses that ignore continuous measurements. The gains are clearest on the regression and time-to-event tasks that conventional classification-only evaluation leaves unmeasured.
