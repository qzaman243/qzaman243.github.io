---
layout: page
title: Hybrid Log Classification
description: Regex, BERT and the Deepseek R1 LLM working together to classify logs
img: assets/img/research/log-classification-pipeline.png
importance: 3
category: engineering
---

A hybrid log classifier that sends each log line to the cheapest method that can handle it: Regex for known patterns, BERT embeddings with Logistic Regression for common cases, and the Deepseek R1 LLM for rare ones.

[Code on GitHub](https://github.com/qzaman243/Hybrid-Log-Classification-System-Using-Deepseek-R1-LLM-NLP-Regex-BERT)

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/research/log-classification-pipeline.png" title="Hybrid log classification pipeline" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Sentence Transformer embeddings and DBSCAN clustering generate regex rules; unmatched logs go to BERT + Logistic Regression or to an LLM.
</div>

## How it works

1. **Learning regex rules from the data.** Each log line is turned into an embedding with a Sentence Transformer. DBSCAN groups similar logs into clusters, and a regex pattern is written for each cluster (with the help of regex101).
2. **Regex classification.** New logs are first matched against these patterns. This fast, free step handles the most common, well-structured logs and assigns them a valid class right away.
3. **Handling unknown logs.** Logs that no pattern matches are marked _Unknown_ and sent to a model:
   - **BERT + Logistic Regression** when there are enough labelled examples of that kind of log.
   - **Deepseek R1 LLM** when there are too few examples to train on.

## Highlights

- Built and deployed a FastAPI-based REST service for real-time log processing and easy integration with other systems.
- Improved log classification accuracy by 40% compared with traditional rule-based approaches.
- Reduced operational costs by 30% by automating log analysis and reducing manual work.
- End-to-end NLP pipeline, from preprocessing to model inference and deployment.

**Technologies:** Python, FastAPI, Sentence Transformers, BERT, DBSCAN, scikit-learn, Deepseek R1 LLM
