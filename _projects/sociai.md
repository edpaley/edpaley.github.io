---
layout: page
title: SociAI (Study in-progress)
description: An immersive VR system using AI-replicated human personas to answer a research hypothesis
img: assets/img/project/sociai_temp.png
importance: 3
category: research
giscus_comments: true
---

## Overview
In the era of immersive virtual environments, activities such as academic conferences and social events are increasingly taking place in VR. However, users often report difficulties in initiating small talk or engaging in natural conversation in such settings, resulting in limited social connection. This study will explore the integration of large language models (LLMs) into personalized virtual avatars that represent real individuals in VR. By embedding contextual personal information such as research interests, professional background, or shared experiences into each avatar, we aim to make social engagement more accessible and fluid. The research investigates whether these enhanced avatars can reduce social friction and improve interpersonal understanding in VR-based interactions, ultimately fostering deeper and more meaningful virtual connections.

User Studies are currently running as of Fall 2026, with more information relating to the project to come.


## My Role
I was the sole engineer for designing and creating a VR system for one-on-one conversations with an AI-driven human replica. I architected the end-to-end full stack, building a local HTTP network that connected a Unity VR client with a Python inference backend. On the backend, I integrated a local RAG pipeline using Hugging Face transformers with Llama-3.2-3B and fine-tuned an XTTS model for likeness and to stream 24kHz audio directly into Unity for real-time avatar voice synthesis.


This project is being conducted under the supervision of Prof. [Huaishu Peng](https://huaishu.me/) and Prof. [Myungin Lee](https://www.myunginlee.com/).
