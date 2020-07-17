---
layout: page
title: software-defined network verification
description:
img: /assets/img/sdn-ver.jpg
importance: 2
---


Software-defined networking (SDN) enables advanced operation and management of network deployments through (virtually) centralised, programmable controllers, which deploy network functionality by installing rules in the flow tables of network switches. Although this is a powerful abstraction, buggy controller functionality could lead to severe service disruption and security loopholes, motivating the need for automated tools to find, or even verify absence of, bugs.

In this strand of work, we are developing *MoCS*, a highly expressive, optimised SDN model that allows capturing subtle real-world bugs, in a reasonable amount of time. This is achieved by (1) analysing the model for possible partial order reductions, (2) statically pre-computing packet equivalence classes and (3) indexing packets and rules that exist in the model. We demonstrate its superiority compared to the state of the art in terms of expressivity, by providing examples of realistic bugs that a prototype implementation of *MoCS* in *Uppaal* caught, and performance/scalability, by running examples on various sizes of network topologies, highlighting the importance of our abstractions and optimisations. *MoCS* also supports timeouts of flow table entries, thus enabling modelling of soft state in the network. Optimisations are proposed that are tailored to this extension. We evaluate the performance of the proposed model in Uppaal using a load balancer and firewall in network topologies of varying size.

#### funding

The work has been funded by the School of Engineering and Informatics, University of Sussex.

#### publications

V. Klimis, G. Parisis and B. Reus, “Model Checking Software-Defined Networks with Flow Entries that Time Out”, In Proceedings of *Formal Methods in Computer-Aided Design (FMCAD)*, 2020.

V. Klimis, G. Parisis and B. Reus, “Towards Model Checking Real-World Software-Defined Networks”, In Proceedings of the *32nd International Conference on Computer-Aided Verification (CAV)*, 2020.
