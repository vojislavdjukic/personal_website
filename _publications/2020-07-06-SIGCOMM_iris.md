---
layout: publication
title: "Beyond the Mega-Data Center: Networking Multi-Data Center Regions"
venue: 'SIGCOMM 20'
paperurl: '/files/sigcomm20-dukic.pdf'
videourl: 'https://dl.acm.org/doi/abs/10.1145/3387514.3406220#sec-supp'
authors: ['Vojislav Dukic', 'Ginni Khanna', 'Christos Gkantsidis', 'Thomas Karagiannis', 'Francesca Parmigiani', 'Ankit Singla', 'Mark Filer', 'Jeffrey L. Cox', 'Anna Ptasznik', 'Nick Harland', 'Winston Saunders', 'Christian Belady']
firstpage: True
---

The difficulty of building large data centers in dense metro areas is pushing big cloud providers towards a different approach to scaling: multiple smaller data centers within tens of kilometers of each other, comprising a "region". We show that networking this small number of nearby sites with each other is a surprisingly challenging and multi-faceted problem. We draw out the operational goals and constraints of such networks, and highlight the design trade-offs involved using data from Microsoft Azure's regions.

Our analysis of the design space shows that network topologies that achieve lower latency and allow greater flexibility in data center placement are, unfortunately, encumbered by their much greater cost and complexity. We thus present and demonstrate a novel optical-circuit-switched architecture, Iris, that lowers these cost and complexity barriers, making a richer topology design space more accessible to operators of regional networks. With Iris, topologies which, in comparison to a simple hub-and-spoke topology can increase the area in which a new DC can be placed by 2-5x, can be implemented at a cost within 1.1x of the simple hub-and-spoke topology, and 7x cheaper than a natural packet-switched network. 