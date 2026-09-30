---
title: "Positive-Unlabeled Preference Optimization For Chest X-ray Report Generation"
collection: publications
category: conferences
permalink: /publication/2026-12-01-pu-dpo-chest-xray
excerpt: 'Retrospective radiology reports omit findings, and models trained on them learn to under-report. We recast the DPO objective as positive-unlabeled learning so that omission noise no longer corrupts the preference signal.'
date: 2026-12-01
venue: 'Advances in Neural Information Processing Systems (NeurIPS)'
paperurl: 'https://arxiv.org/abs/2608.05341'
---

Vision-language models for radiology report generation are trained on retrospective clinical reports, which suffer from *omission noise*: a finding may be genuinely present in the image yet go unmentioned in the report. Models trained with standard objectives inherit these omissions and learn to under-report findings themselves.

The problem persists under preference optimization. A report that mentions a finding absent from the reference is treated as dispreferred, even when the finding is real and the reference is simply incomplete, so the preference signal actively rewards under-reporting.

We propose **PU-DPO**, which reformulates the direct preference optimization objective as positive-unlabeled learning. Unmentioned findings are treated as unlabeled rather than negative, which prevents omission noise from corrupting the preference signal and keeps the model from being penalized for correct findings the reference happens to leave out.
