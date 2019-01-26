---
title: "Is advance knowledge of flow sizes a plausible assumption?"
collection: publications
venue: 'NSDI 19 (to appear)'
paperurl: 'http://vojislavdjukic.github.io/files/paper1.pdf'
authors: '<u>Vojislav Dukic</u>, Sangeetha Abdu Jyothi, Bojan Karlas, Muhsen Owaida, Ce Zhang, Ankit Singla'
---

Recent research has proposed several packet, flow, and coflow scheduling methods that could substantially improve performance for data center workloads. Most of this work assumes advance knowledge of flow sizes, but the lack of a clear path to obtaining such knowledge has also prompted some work on non-clairvoyant scheduling, albeit with more limited performance benefits and narrower applicability.

We thus investigate whether flow sizes can be known in advance in practice, using both simple heuristics and learning methods. Our systematic and substantial efforts across these approaches for estimating flow sizes indicate, unfortunately, that such knowledge is likely hard to obtain with high confidence across many settings of practical interest. However, our prognosis is ultimately more positive: even simple heuristics can help estimate flow sizes for many flows, and this partial knowledge has utility even in schedulers designed for fully clairvoyant operation. These results indicate that a presumed lack of advance knowledge of flow sizes is not necessarily prohibitive for highly efficient scheduling, and suggest further exploration in two directions: (a) scheduling under partial knowledge; and (b) evaluating the practical payoff and expense of obtaining more knowledge.
