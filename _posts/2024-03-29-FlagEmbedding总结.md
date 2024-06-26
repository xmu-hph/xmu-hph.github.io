---
title: FlagEmbedding总结
date: 2024-03-29 16:46:00 +0800
categories: [tools, notes]
tags: [tools]     # TAG names should always be lowercase
math: true
mermaid: true
img_path: /commons/2024-03-29-FlagEmbedding总结/
author: hupenghui
---

<!-- markdownlint-capture -->
<!-- markdownlint-disable -->
> FlagEmbedding主要是用transformers库中封装好的加载模型和加载数据的函数，同时对数据也进行了自己的处理。
{: .prompt-tip }
<!-- markdownlint-restore -->

## 云计算基础

1. `linux`操作指南：[A Linux Command Line Primer](https://www.digitalocean.com/community/tutorials/a-linux-command-line-primer?mkt_tok=MTEzLURUTi0yNjYAAAGSFo_O1wLPctD8jliDqbpU_MLnw5gLdckxO5Cnpurii1b-RlfTDwHFC0FG1ycJd9ekllBsBJdCzVGiC3vpHWLSnzhTYji_yxex08-Y4ApL9Sc)
2. `sql`命令指南：[How To Use SQL](https://www.digitalocean.com/community/tutorial-series/how-to-use-sql?mkt_tok=MTEzLURUTi0yNjYAAAGSFo_O1zcuTP_S-hygPjxD2N52H_KAt8-iF1I1aIiYGib-pRhVIKzdWCZfcsNDbqSg7FWAokIg8I63QzbHdBr9-W6CIPxiRpq6z9f5k6mgBkw)
3. 在服务器中搭建一个静态网页：[How To Deploy a Static Website to the Cloud with DigitalOcean App Platform](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-static-website-to-the-cloud-with-digitalocean-app-platform?mkt_tok=MTEzLURUTi0yNjYAAAGSFo_O15XPxeeKkw92vbYuhbfcvXwGtbcHdxk6Lo5WXjsuflbb01uinpMUqxTJdtgEGSKzlKeMcx0DNcZhcHQH1EKwOajih8a0wTOspXnnqJQ)（很离谱，这里面的图片一张都看不见，主打一个意会。）

## 机器学习基础

1. 使用库函数：[How To Create an Intelligent Chatbot in Python Using the spaCy NLP Library](https://digitalocean.com/community/tutorials/how-to-create-an-intelligent-chatbot-in-python-using-the-spacy-nlp-library?mkt_tok=MTEzLURUTi0yNjYAAAGSINyQ6i7z2o1q-kdDz6aRJ_YSzJopCQi9pJgJP682KHusgDMgJvWV7iaXJxGmDOTFauH00JMwbf9lCvXeZwaqgMlvTjPaG2wPPuLsf8OL5wc)
2. 计算机视觉技术：[An Introduction to Computer Vision in JavaScript using OpenCV.js](https://www.digitalocean.com/community/tutorials/introduction-to-computer-vision-in-javascript-using-opencvjs?mkt_tok=MTEzLURUTi0yNjYAAAGSINyQ6kXsKXJ8-M9BhOodS8BOGANDzh4JdgE9CFy5VfPdJQpSQPWmyoZd2pw0dz4Cjb59Sy6vxGKUYlqonXFbVBWle6d9xObL1qZr733P-po)
3. 手写数字识别：[Introduction to PyTorch: Build a Neural Network to Recognize Handwritten Digits](https://www.digitalocean.com/community/tutorials/introduction-to-pytorch-build-a-neural-network-to-recognize-handwritten-digits?mkt_tok=MTEzLURUTi0yNjYAAAGSINyQ6sfhQxaHWJ4EsZk8M5MeJTkDcC41xjtkU_2tRbNGXuod8Mu6VobXoOvjwpg8hqwby0gP981UTO7bjekRnbKcgSJyiFq2WL-dksJ8j3c)
4. 深度强化学习：[Bias-Variance for Deep Reinforcement Learning: How To Build a Bot for Atari with OpenAI Gym](https://www.digitalocean.com/community/tutorials/how-to-build-atari-bot-with-openai-gym#understanding-bias-variance-tradeoffs)

### 总结

机器学习问题和用户交互问题的解决方案的结构是不同的，机器学习问题解决方案是导入数据、导入模型、处理数据、评估指标，而用户交互问题不是自己独立的，他需要跟用户交互，所以除了读取静态数据外，还应该有读取动态数据（用户交互数据），然后根据动态数据决定执行什么函数，处理数据，输出结果。最关键的是，这个东西感觉用户不友好，看了代码感觉还是啥也看不懂，没有机器学习那么顺。`ctrl+g`是github中的搜索快捷键，非常有用。看我`mentor`用羡慕坏了。

## 网页展示

1. 使用`html`：[How To Build a Website with HTML](https://www.digitalocean.com/community/tutorial-series/how-to-build-a-website-with-html?mkt_tok=MTEzLURUTi0yNjYAAAGSJgLu-N6L3wqhU9nzBFR1sPciz6L-LEalPGluUazOJef9BSzqBz528Zuc24Ixb-GEEPhRlKN6NdHGPpoVS-O34CqWL2ps6bOPdLwXQSBocb8)
2. 使用`css`：[How To Build a Website With CSS](https://www.digitalocean.com/community/tutorial-series/how-to-build-a-website-with-css?mkt_tok=MTEzLURUTi0yNjYAAAGSJgLu-KOW4pS2D7bV5nbxprRLv68rFCDzx6Hq6sMTHbHIaeY3NhRSS4mfi-JWGTNohVq1pPzv57JAW08kn2PI5TIL70fQduX6spUFABTK8gw)
3. 使用`wordpress`：[How To Install WordPress on Ubuntu 20.04 with a LAMP Stack](https://www.digitalocean.com/community/tutorials/how-to-install-wordpress-on-ubuntu-20-04-with-a-lamp-stack?mkt_tok=MTEzLURUTi0yNjYAAAGSJgLu-J7RUZGMF4_ysYKHPStL9EkHf9h_uHegQ33PKhzAu8SPMaoibEtEfrpQJAJkb5Lfv928kr-O8dGNi-gfwuPZcLkaXP7AwAY0tPpnlgo)

### 总结

这些都是一个教程，太长了，我实在是懒得看下去。
