---
layout: post
title: Short paper accepted at IEEE/IFIP IM 2019.
date: 2018-11-16
inline: false
---

A. Messager, G. Parisis, I. Z. Kiss, R. Harper, P. Tee and L. Berthouze, “Functional Topology Inference from Network Events”, In Proceedings of IFIP/IEEE IM 2019.

In this paper we present a novel approach for inferring functional connectivity within a large-scale network from time series of emitted node events. We do so under the following constraints: (a) non-stationarity of the underlying connectivity, (b) sparsity of the time-series of events, and (c) absence of an explicit model describing how events propagate through the network. We develop an inference method whose output is an undirected weighted network, where the weight of an edge between two nodes denotes the probability of these nodes being functionally connected. Two nodes are assumed to be functionally connected if they show significantly more coincident or short-lagged events than randomly picked pairs of nodes with similar levels of activity. We develop a model of time-varying connectivity whose parameters are determined by maximising the model's predictive power from one time window to the next. We assess the accuracy, efficiency and scalability of our method on a real dataset of network events spanning multiple months.
