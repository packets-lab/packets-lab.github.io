---
layout: post
title: Paper accepted at IEEE INFOCOM 2016.
date: 2015-11-27
inline: false
---

M.Kheirkhah, I.Wakeman and G.Parisis, “MMPTCP: A Multipath Transport Protocol for Data Centres”, In Proceedings of IEEE INFOCOM, 2016.

Modern data centres provide large aggregate network capacity and multiple paths among servers. Traffic is very diverse; most of the data is produced by long, bandwidth hungry flows but the large majority of flows, which commonly come with strict deadlines regarding their completion time, are short. It has been shown that TCP is not efficient for any of these types of traffic in modern data centres. More recent protocols such MultiPath TCP (MPTCP) are very efficient for long flows, but are ill-suited for short flows. In this paper, we present Maximum MultiPath TCP (MMPTCP), a novel transport protocol which, compared to TCP and MPTCP, reduces short flows' completion times, while providing excellent goodput to long flows. To do so, MMPTCP runs in two phases; initially, it randomly scatters packets in the network under a single congestion window exploiting all available paths. This is beneficial to latency-sensitive flows. After a specific amount of data is sent, MMPTCP switches to a regular MultiPath TCP mode. MMPTCP is incrementally deployable in existing data centres as it does not require any modifications outside the transport layer and behaves well when competing with legacy TCP and MPTCP flows. Our extensive experimental evaluation in simulated FatTree topologies shows that all design objectives for MMPTCP are met.
