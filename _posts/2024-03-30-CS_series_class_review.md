---
title: CS series class review
date: 2024-03-30 16:01:00 +0800
categories: [tools,notes]
tags: [tools]     # TAG names should always be lowercase
math: true
mermaid: true
img_path: /commons/2024-03-30-CS_series_class_review/
author: hupenghui
---

## basics for reinforcement learning

$$
\begin{equation}
  \nabla_{\theta}\sum_{s}\sum_{a}P(s)\pi(a|s)r(s,a)=\sum_{s}\sum_{a}\nabla_{\theta}[P(s)\pi(a|s)]r(s,a)
  \label{eq:series}
\end{equation}
$$

We can decompose the return into reward in every step : $r(\tau)=\sum_{i} r(s_i,a_i)$,In the way we can calculate the mean of every reward: \eqref{eq:series} .

$$
\begin{equation}
  {R}=\sum_{s_1}\sum_{a_1}p(s_1)\pi(a_1|s_1)r(s_1,a_1)+\sum_{s_1}\sum_{a_1}\sum_{s_2}\sum_{a_2}p(s_1)\pi(a_1|s_1)p(s_2|s_1,a_1)\pi(a_2|s_2)r(s_2,a_2)+\cdots
  \label{eq:mean_return}
\end{equation}
$$

The mean of the return will be \eqref{eq:mean_return}:

$$
\begin{equation}
  {R}=\sum_{s_1}\sum_{a_1}p(s_1)\frac{\pi(a_1|s_1)}{\pi_o(a_1|s_1)}\pi_o(a_1|s_1)r(s_1,a_1)+\sum_{s_1}\sum_{a_1}\sum_{s_2}\sum_{a_2}p(s_1)\pi(a_1|s_1)p(s_2|s_1,a_1)\pi(a_2|s_2)\frac{\pi_o(a_1|s_1)\pi_o(a_2|s_2)}{\pi_o(a_1|s_1)\pi_o(a_2|s_2)}r(s_2,a_2)+\cdots
  \label{eq:importance_sample}
\end{equation}
$$

if we use importance sample, then the mean of the return will be \eqref{eq:importance_sample}:

$$
\begin{equation}
  {R}=\sum_{s_1}\sum_{a_1}p(s_1)\pi_o(a_1|s_1)\frac{\pi(a_1|s_1)}{\pi_o(a_1|s_1)}r(s_1,a_1)+\sum_{s_1}\sum_{a_1}\sum_{s_2}\sum_{a_2}p(s_1)\pi_o(a_1|s_1)p(s_2|s_1,a_1)\pi_o(a_2|s_2)\frac{\pi(a_1|s_1)\pi(a_2|s_2)}{\pi_o(a_1|s_1)\pi_o(a_2|s_2)}r(s_2,a_2)+\cdots
  \label{eq:factor_resequence}
\end{equation}
$$

We can change the sequence of the factor in above equation \eqref{eq:factor_resequence}.

TRPO:Cause we use the value function to evaluate the total return,so we can get a different equation for the relation between $R(\pi)$ and $R(\pi_0)$

![trpo](trpo1.png){: w="400" h="300"}

but the trace of new $\pi$ we can't obtain,we can obtain the trace of old $\pi$,so trpo try to use only one step new $\pi$ and all others old $\pi$, importance sample original need all step to be decided by new $\pi$,but we take away off,only one step new $\pi$,this is not the return of new $\pi$,but satisfy the first order requirements.
