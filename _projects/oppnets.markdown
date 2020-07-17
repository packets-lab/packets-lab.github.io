---
layout: page
title: routing in opportunistic networks
description:
img: /assets/img/oppnets.jpg
importance: 3
---

With the proliferation of smartphones and their advanced connectivity capabilities, opportunistic networks have gained a lot of traction during the past years; they are suitable for increasing network capacity and sharing ephemeral, localised content. They can also offload traffic from cellular networks to device-to-device ones, when cellular networks are heavily stressed. Opportunistic networks can play a crucial role in communication scenarios where the network infrastructure is inaccessible due to natural disasters, large-scale terrorist attacks or government censorship. Geocasting, where messages are destined to specific locations (casts) instead of explicitly identified devices, has a large potential in real world opportunistic networks, however it has attracted little attention in the context of opportunistic networking.

#### geocasting

We have developed *Geocasting Spray And Flood (GSAF)*, a simple and efficient geocasting protocol for opportunistic networks. GSAF follows an elegant and flexible approach where messages take random walks towards the destination cast. Messages that are routed away from the destination cast are extinct when devices' buffers get full, freeing space for new messages to be delivered. In GSAF, casts do not have to be pre-defined; instead users can route messages to arbitrarily defined casts. GSAF does that in a privacy-preserving fashion. We have experimentally evaluated our protocols and compare their performance to prominent geocasting protocols in a very wide set of scenarios, including different maps, mobility models and user populations. Both GSAF and DA-GSAF perform significantly better compared to all other studied protocols, in terms of message delivery ratio, latency and network overhead. DA-GSAF is particularly efficient in sparse scenarios minimising network overhead compared to all other studied protocols. Both GSAF and DA-GSAF perform very well for a wide range of device/user populations indicating that our proposal is viable for crowded and sparse opportunistic networks.

#### routing in dense networks

We are developing *GeoHawk*, a routing protocol for dense mobile networks that support opportunistic communication and content dissemination among mobile devices in crowded events. The driving use case has been the Grand Mosque, the largest mosque in the world located at the heart of the city of Makkah in Saudi Arabia. During Ramadan and Hajj seasons, the Grand Mosque can get extremely crowded, with anticipated number of visitors close to 2.5 million, after the current expansion work is completed. The proposed protocol deals with the very high density of users/devices by heavily aggregating routing information using Bloom filters. Identifiers of mobile devices that reside within specific geographical regions are disseminated in the network in the form of Bloom filters. Said geographical regions are dynamically created and destroyed; their size evolves to reflect the uncertainty in the topology, due to mobility and potential inaccuracies of the underlying location estimation mechanism. Bloom filters are also decayed to reflect information ageing. Devices exchange routing information with their neighbours and announce aggregated information (i.e. Bloom filters) in messages that propagate towards specific directions and reach distant areas of the opportunistic network. Data is then disseminated (and replicated through a simple but efficient ticketing mechanism) towards directions where the information about the existence of the destination node is stronger. Upon reaching the best known region for the destination node, a message is either flooded, if the belief that the node resides in the region is strong (as indicated by a belief threshold), or, in the opposite case, redirected to a randomly selected region.

#### opportunistic routing in stadia

TODO

#### funding

The work has been funded by EPSRC and the School of Engineering and Informatics, University of Sussex.

#### publications

A. Rajaei, D. Chalmers, I. Wakeman, and G. Parisis, “Efficient Geocasting in Opportunistic Networks”, in *Computer Communications*, vol. 127, 2018.

G. Parisis, V. Sourlas, K.V. Katsaros, W.K. Chai, G. Pavlou, and I. Wakeman, “Efficient content delivery through fountain coding in opportunistic information-centric networks”, in *Computer Communications*, 2017.

A. Rajaei, D. Chalmers, I. Wakeman, and G. Parisis, “GSAF: Efficient and Flexible Geocasting for Opportunistic Networks”, In Proceedings of the *17th IEEE International Symposium on a World of Wireless, Mobile and Multimedia Networks (WoWMoM)*, 2016.

G. Parisis, V, Sourlas, K.V. Katsaros, W.K. Chai, G. Pavlou, “Enhancing Multi-source Content Delivery in Content-Centric Networks with Fountain Coding”, In Proceedings of *CoNEXT CCDWN Workshop*, 2015.

I. Wakeman, S. Naicken, J. Rimmer, D. Chalmers and C. Fisher, "The fans united will always be connected: building a practical DTN in a football stadium", In Proceedings of the *International Conference on Ad Hoc Networks*, 2013.
