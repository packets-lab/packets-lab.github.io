---
layout: post
title: Paper accepted at IEEE/ACM Transactions on Networking
date: 2021-02-03
inline: false
---

M. Alasmar, R. Clegg, N. Zakhleniuk and G. Parisis, “Internet Traffic Volumes Are Not Gaussian – They Are Log-Normal: An 18-Year Longitudinal Study With Implications for Modelling and Prediction”, in IEEE/ACM Transactions on Networking, 2021.

Getting good statistical models of traffic on network links is a well-known, often-studied problem. A lot of attention has been given to correlation patterns and flow duration. The distribution of the amount of traffic per unit time is an equally important but less studied problem. We study a large number of traffic traces from many different networks including academic, commercial and residential networks using state-of-the-art sta- tistical techniques. We show that traffic obeys the log-normal distribution which is a better fit than the Gaussian distribution commonly claimed in the literature. We also investigate an alternative heavy-tailed distribution (the Weibull) and show that its performance is better than Gaussian but worse than log- normal. We examine anomalous traces which exhibit a poor fit for all distributions tried and show that this is often due to traffic outages or links that hit maximum capacity. We demonstrate that the data we look at is stationary if we consider samples of 15- minute long or even 1-hour long. This gives confidence that we can use the distributions for estimation and modelling purposes.

We demonstrate the utility of our findings in two contexts: predicting that the proportion of time traffic will exceed a given level (for service level agreement or link capacity estimation) and predicting 95th percentile pricing. We also show that the log-normal distribution is a better predictor than Gaussian or Weibull distributions in both contexts.
