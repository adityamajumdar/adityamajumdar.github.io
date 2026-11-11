---
layout: page
title: "Can LLMs Give Safe Everyday Health Advice?"
description: "FAccT 2026. Physicians graded how public LLMs answered 212 health questions submitted by everyday users."
img:
importance: 4
category: work
---

Bonam Mingole, **Aditya Majumdar**, Firdaus Choudhury, Amulya Yadav. *ACM FAccT 2026*.
[arXiv](https://arxiv.org/abs/2506.13805)

People increasingly ask chatbots about their health, but most studies of medical LLMs test them on exam questions or cases written by doctors. We wanted to see how they handle the questions ordinary people actually ask.

We ran a week-long university competition in which 34 participants submitted 212 health concerns, real or imagined. Four publicly available LLMs answered each one, both on their own and with access to a medical knowledge base. Nine board-certified physicians then graded the responses. On average, they judged 76% of the answers accurate. Interviews with seven medical professionals helped explain where and why the models fell short.

My part focused on evaluation: building pipelines that used LLMs to replicate physician grading, and testing how sensitive those judgments were to prompt design.
