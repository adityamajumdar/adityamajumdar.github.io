---
layout: page
title: "Teaching LLMs to Handle Code-Mixed Language"
description: "Using AI feedback to improve how LLMs translate text that mixes languages, such as Hindi and English."
img:
importance: 6
category: work
---

Wenbo Zhang, **Aditya Majumdar**, Amulya Yadav. *Under review.*
[arXiv](https://arxiv.org/abs/2411.09073)

Many multilingual speakers mix languages within a single sentence, for example switching between Hindi and English. Multilingual LLMs still handle this poorly.

Our framework, CHAI, tackles the problem in two steps. First, we tested how well LLMs can label the quality of code-mixed translations compared with human annotators. Then we used those LLM labels as preference data to train models through reinforcement learning from AI feedback, which avoids the cost of collecting human preferences at scale. In human-judged comparisons, CHAI-trained models outperformed leading open-source LLMs on code-mixed translation.
