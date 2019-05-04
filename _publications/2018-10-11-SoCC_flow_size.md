---
title: "Network Scheduling in the Dark"
collection: publications
venue: '(Poster) SoCC 18'
paperurl: '/files/SoCC18_poster.pdf'
authors: ['Vojislav Dukic', 'Sangeetha Abdu Jyothi', 'Bojan Karlas', 'Muhsen Owaida', 'Ce Zhang', 'Ankit Singla']
firstpage: False
---

<b>Motivation:</b> Advance knowledge of future events in a dynamic system can often be used to take actions that improve system performance. In data center networks, such knowledge could potentially benefit many problems, including routing and flow scheduling, circuit switching, packet scheduling in switch queues, and transport protocols.

Indeed, past work on each of these topics has explored this, and in many cases, claimed significant improvements. Nevertheless, little of this work has achieved deployment in data centers, which largely use techniques that are agnostic to traffic information, such as shortest path routing with randomization, and first-in-first-out queueing at switches.

A significant roadblock for traffic-aware scheduling is that in practice, traffic characteristics can be hard to ascertain accurately in a timely fashion. In particular, past work on network flow and packet scheduling has assumed advance knowledge of flow sizes. In tightly controlled environments, developing an API for applications to expose such information is plausible, even though it could require changes to a large number of applications. However, even in such environments, the application itself may not know such information a priori -- data analysis jobs, for instance, may start sending out the results of a computation before the execution finishes and the final size of the result is known. Further, for public cloud data centers, this API approach would require having their customers modify their applications.

<b>Contribution:</b> We thus examine both simple heuristics and learning methods to determine flow sizes in advance and evaluate their accuracy and utility. Our system, Flux, leverages behavioral patterns of cloud applications. It uses Gradient Boosting Decision Trees (GBDT) to correlate CPU, memory, disk, and network utilization to future network traffic. Flux entails no modifications to applications.

We tested Flux using various workloads -- data processing on Spark, a Web workload on Apache Tomcat, training neural networks on TensorFlow -- achieving high accuracy in flow size prediction, with R^2 values ranging from 73% to 97%.

We also explore the use of predicted flow sizes in three known network scheduling techniques, finding that Flux can reduce average flow completion times by 1.1x to 10.5x compared to information-agnostic techniques, even after accounting for the inaccuracies in our estimates. Our early results show promise across workloads with substantial variation in underlying data and run configurations, indicating that our framework can learn which underlying system characteristics are predictive of traffic for different applications and workloads.

<b>Conclusion:</b> Our results indicate that accurate-enough flow size estimation is possible and it can be used to provide significant speedups when combined with existing network scheduling techniques. Thus, we are presently investigating the generality and limits of this approach. %This approach thus holds promise for applying the best-known scheduling techniques without explicitly asking applications to expose traffic characteristics.
