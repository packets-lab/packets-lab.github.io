---
layout: post
title: Paper accepted at Computer Networks.
date: 2019-01-01
inline: false
---

M. Kheirkhah, I. Wakeman and G. Parisis, “Multipath Transport and Packet Spraying for Efficient Data Delivery in Data Centres”, in Computer Networks, vol. 162, 2019.

Modern data centres provide large aggregate network capacity and multiple paths among servers. Traffic in data centres is very diverse; most of the data is produced by long, bandwidth hungry flows but the large majority of flows, which commonly come with stringent deadlines regarding their completion time, are short. It has been shown that TCP is not efficient for any of these types of traffic in modern data centres. MultiPath TCP (MPTCP) employs multipath data transport and is efficient for long flows but ill-suited for short flows.

In this paper, we present Maximum MultiPath TCP (MMPTCP), a novel transport protocol which extends MPTCP and, compared to TCP and MPTCP, reduces short flows’ completion times, while providing excellent goodput to long flows. To do so, MMPTCP runs in two phases; initially, it randomly scatters packets in the network under a single congestion window exploiting all available paths. This is beneficial to latency-sensitive flows. After a specific amount of data is sent, MMPTCP switches to a regular MultiPath TCP mode. MMPTCP is incrementally deployable in existing data centres as it does not require any modifications outside the transport layer and behaves well when competing with MPTCP flows. We also present a topology-specific extension of MMPTCP that adjusts the numbers of subflows during the second phase of the protocol based on knowledge about the location of the receiver in the data centre.

We present extensive evaluation that shows that MMPTCP’s design objectives are met. We have implemented MMPTCP (along with MPTCP and packet spraying) in ns-3 and evaluated our protocol in simulated FatTree topologies. We have evaluated how MMPTCP performs compared to TCP and MPTCP and how its performance is affected by transient hotspots in the network. We have also experimented with different thresholds for duplicate acknowledgements and fast retransmissions and shown that MMPTCP performs well when the size of short flows is widely ranged. Finally, we have evaluated how MMPTCP performs under conditions that result in Incast, when different congestion control algorithms are used in its second phase and when varying the overall network load.
