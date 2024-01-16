---
layout: post
title: Paper accepted at IEEE/ACM Transactions on Networking
date: 2021-07-21
inline: false
---

M. Alasmar, G. Parisis and J. Crowcroft, “SCDP: Systematic Rateless Coding for Efficient Data Transport in Data Centres”, in IEEE/ACM Transactions on Networking, 2021.

In this paper we propose SCDP, a novel, general-purpose data transport protocol for data centres that, in contrast to all other protocols proposed to date, natively supports one-to-many and many-to-one data communication, which is extremely common in modern data centres. SCDP does so without compromising on efficiency for short and long unicast flows. SCDP achieves this by integrating RaptorQ codes with receiver-driven data transport, in-network packet trimming and Multi-Level Feedback Queuing (MLFQ); (1) RaptorQ codes enable efficient one-to-many and many-to-one data transport; (2) on top of RaptorQ codes, receiver-driven flow control, in combination with in-network packet trimming, enable efficient usage of network resources as well as multi-path transport and packet spraying for all transport modes. Incast and Outcast are eliminated; (3) the systematic nature of RaptorQ codes, in combination with MLFQ, enable fast, decoding-free completion of short flows. We extensively evaluate SCDP in a wide range of simulated scenarios with realistic data centre workloads. For one-to-many and many-to-one transport sessions, SCDP performs significantly better compared to NDP. For short and long unicast flows, SCDP performs equally well or better compared to NDP.
