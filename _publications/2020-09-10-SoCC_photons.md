---
layout: publication
title: "Photons: Lambdas on a diet"
venue: 'SoCC 20'
authors: ['Vojislav Dukic', 'Rodrigo Bruno', 'Ankit Singla', 'Gustavo Alonso']
firstpage: True
---

Serverless computing allows users to create short, stateless functions and invoke hundreds of them concurrently to tackle massively parallel workloads. We observe that even though most of the footprint of a serverless function is fixed across its invocations --- language runtime, libraries, and other application state --- today's serverless platforms do not exploit this redundancy.

Such an inefficiency has cascading negative impacts: longer startup times, lower throughput, higher latency, and higher cost.
To mitigate these problems, we have built <i>Photons</i>, a framework leveraging workload parallelism to co-locate multiple instances of the <i>same</i> function within the same runtime. Concurrent invocations can then share the runtime and application state transparently, without compromising execution safety. Photons reduce function's memory consumption by <i>25%</i> to <i>98%</i> per invocation, with no performance degradation compared to today's serverless platforms. We also show that our approach can reduce the overall memory utilization by <i>30%</i>, and the total number of cold starts by <i>52%</i>.
