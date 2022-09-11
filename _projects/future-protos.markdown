---
layout: page
title: network protocols for the future
description:
img: /assets/img/dc-proto.jpg
importance: 1
---

**Low Earth Orbit (LEO) satellite constellations**. Very large constellations of Low Earth Orbit (LEO) satellites are currently being deployed; private companies (e.g., SpaceX, OneWeb) lead the race and billion-dollar investments are already in place [1]. This will give rise to unprecedented wide-area network deployments that will provide 100% geographic coverage and exhibit a unique combination of characteristics; (1) aggregate bandwidth in the order of hundreds of Tbps, which is comparable to today’s aggregate fibre capacity; (2) multiple paths in a dense and constantly changing network topology; (3) sub-10ms round-trip time between the Earth and the first hop satellite; (4) low but varying end-to-end latency that can be smaller than what the best theoretical fibre path can support. LEO deployments present significant challenges calling for a rethink of routing and data transport mechanisms to ensure efficient usage of network resources. In this research strand we are rethinking data transport over LEO satellite networks.

**Data centre networks**. Modern data centres provide large aggregate network capacity and multiple paths among servers. Traffic in data centres is very diverse; most of the data is produced by long, bandwidth hungry flows but the large majority of flows, which commonly come with stringent deadlines regarding their completion time, are short. It has been shown that TCP is not efficient for any of these types of traffic in modern data centres. MultiPath TCP (MPTCP) employs multipath data transport and is efficient for long flows but ill-suited for short flows.

#### LEO satellite network simulations

We developed a LEO satellite constellation simulation model1 within OMNeT++ and INET, which is validated by comparing the results with existing work. Our model builds upon the fundamentals of the Open Source Satellite Simulator (OS3 ), which was ported to the latest version of INET framework.


#### polyraptor

We developed *polyraptor*, a novel, general-purpose data transport protocol for data centres that, in contrast to all other protocols proposed to date, natively supports one-to-many and many-to-one data communication, which is extremely common in modern data centres. SCDP does so without compromising on efficiency for short and long unicast flows. SCDP achieves this by integrating RaptorQ codes with receiver-driven data transport, in-network packet trimming and Multi-Level Feedback Queuing (MLFQ); (1) RaptorQ codes enable efficient one-to-many and many-to-one data transport; (2) on top of RaptorQ codes, receiver-driven flow control, in combination with in-network packet trimming, enable efficient usage of network resources as well as multi-path transport and packet spraying for all transport modes. Incast and Outcast are eliminated; (3) the systematic nature of RaptorQ codes, in combination with MLFQ, enable fast, decoding-free completion of short flows. We extensively evaluate SCDP in a wide range of simulated scenarios with realistic data centre workloads. For one-to-many and many-to-one transport sessions, SCDP performs significantly better compared to NDP. For short and long unicast flows, SCDP performs equally well or better compared to NDP.

#### reinforcement learned congestion control

We are investigating the integration of reinforcement learning in data transport with the aim to learn congestion control algorithms, which can adapt to changes in application workloads and requirements, for next-generation networks (e.g. data centres and very low earth orbit satellite constellations). We employ reinforcement learning, which, in combination with a deep neural network for policy approximation, improve the policy (i.e. rate adaptation in the face of congestion) dynamically, by learning from collected experiences, which are generated using network simulations conducted in Omnet++.

#### multipath TCP

We developed *Maximum MultiPath TCP (MMPTCP)*, a novel transport protocol which extends MPTCP and, compared to TCP and MPTCP, reduces short flows’ completion times, while providing excellent goodput to long flows. To do so, MMPTCP runs in two phases; initially, it randomly scatters packets in the network under a single congestion window exploiting all available paths. This is beneficial to latency-sensitive flows. After a specific amount of data is sent, MMPTCP switches to a regular MultiPath TCP mode. MMPTCP is incrementally deployable in existing data centres as it does not require any modifications outside the transport layer and behaves well when competing with MPTCP flows. We also present a topology-specific extension of MMPTCP that adjusts the numbers of subflows during the second phase of the protocol based on knowledge about the location of the receiver in the data centre.

We present extensive evaluation that shows that MMPTCP’s design objectives are met. We have implemented MMPTCP (along with MPTCP and packet spraying) in ns-3 and evaluated it in simulated FatTree topologies. We have evaluated how MMPTCP performs compared to TCP and MPTCP and how its performance is affected by transient hotspots in the network. We have also experimented with different thresholds for duplicate acknowledgements and fast retransmissions and shown that MMPTCP performs well when the size of short flows is widely ranged. Finally, we have evaluated how MMPTCP performs under conditions that result in Incast, when different congestion control algorithms are used in its second phase and when varying the overall network load.

#### funding

Research in this strand has been funded by the School of Engineering and Informatics, an Amazon research award (providing AWS EC2 instances) and GEANT's Innovation Programme.

#### publications

A. Valentine and G. Parisis, “Developing and experimenting with LEO satellite constellations in OMNeT++”, In Proceedings of the 8th OMNeT++ Community Summit, 2021.

M. Alasmar, G. Parisis and J. Crowcroft, “SCDP: Systematic Rateless Coding for Efficient Data Transport in Data Centres”, in IEEE/ACM Transactions on Networking, 2021.

M. Kheirkhah, I. Wakeman and G. Parisis, “Multipath Transport and Packet Spraying for Efficient Data Delivery in Data Centres”, in Computer Networks, vol. 162, 2019.

M. Alasmar and G. Parisis, “Evaluating modern data centre transport protocols in OMNeT++/INET”, In Proceedings of the 6th OMNeT++ Community Summit, 2019.

M. Alasmar, G. Parisis and J. Crowcroft, “Polyraptor: Embracing Path and Data Redundancy in Data Centres for Efficient Data Transport”, In Proceedings of ACM SIGCOMM (poster session), 2018.

M.Kheirkhah, I.Wakeman and G.Parisis, “MMPTCP: A Multipath Transport Protocol for Data Centres”, In Proceedings of IEEE INFOCOM, 2016.

M.Kheirkhah, I.Wakeman and G.Parisis, “Multipath-TCP in ns-3”, In Proceedings of the Workshop on ns-3 (WNS3), 2014.

G. Parisis, T. Moncaster, A. Madhavapeddy, J. Crowcroft, “ Trevi: watering down storage hotspots with cool fountain codes”, In Proceedings of HotNets-XII, 2013.
