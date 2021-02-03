---
layout: post
title: IEEE/ACM Transactions on Networking paper accepted!
date: 2021-02-03
inline: false
---

M. Alasmar, R. Clegg, N. Zakhleniuk and G. Parisis, “Internet Traffic Volumes Are Not Gaussian – They Are Log-Normal: An 18-Year Longitudinal Study With Implications for Modelling and Prediction”, in IEEE/ACM Transactions on Networking, 2021.

Software-defined networking (SDN) enables advanced operation and management of network deployments through (virtually) centralised, programmable controllers, which deploy network functionality by installing rules in the flow tables of network switches. Although this is a powerful abstraction, buggy controller functionality could lead to severe service disruption and security loopholes, motivating the need for (semi-)automated tools to find, or even verify absence of, bugs. Model checking SDNs has been proposed in the literature, but none of the existing approaches can support dynamic network deployments, where flow entries expire due to timeouts. This is necessary for automatically refreshing (and eliminating stale) state in the network (termed as soft-state in the network protocol design nomenclature), which is important for scaling up applications or recovering from failures. In this paper, we extend our model (MoCS) to deal with timeouts of flow table entries, thus supporting soft state in the network. Optimisations are proposed that are tailored to this extension. We evaluate the performance of the proposed model in UPPAAL using a load balancer and firewall in network topologies of varying size.
