---
layout: post
title: Paper accepted at IEEE/IFIP NOMS AnNet workshop 2016.
date: 2015-11-27
inline: false
---

P. Tee, G. Parisis, and I. Wakeman, Towards an Approximate Graph Entropy Measure for Identifying Incidents in Network Event Data, In Proceedings of the IEEE/IFIP NOMS International Workshop on Analytics for Network and Service Management (AnNet), 2016.

A key objective of monitoring networks is to identify potential service threatening outages from events within the network before service is interrupted. Identifying causal events, Root Cause Analysis (RCA), is an active area of research, but current approaches are vulnerable to scaling issues with high event rates. Elimination of noisy events that are not causal is key to ensuring the scalability of RCA. In this paper, we introduce vertex-level measures inspired by Graph Entropy and propose their suitability as a categorization metric to identify nodes that are a priori of more interest as a source of events. We consider a class of measures based on Structural, Chromatic and Von Neumann Entropy. These measures require NP-Hard calculations over the whole graph, an approach which obviously does not scale for large dynamic graphs that characterise modern networks. In this work we identify and justify a local measure of vertex graph entropy, which behaves in a similar fashion to global measures of entropy when summed across the whole graph. We show that such measures are correlated with nodes that generate incidents across a network from a real data set.
