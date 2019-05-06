---
layout: main
title: 'Overpaying the cloud'
date: 2019-05-06
permalink: /posts/2019/05/performance_oriented_cloud/
tags:
  - cloud computing
  - performance optimization
  - elastic cloud
  - cloud economy
---

Cloud providers use resource overbooking to reduce the cost of running infrastructure and increase the profit. Overbooking means that multiple cloud tenants are being charged for the same physical resource. This model works because not all users use the resource all the time, and then by statistical multiplexing users have an illusion that the resource is fully at their disposal. Overbooking has some obvious problems: (a) statistical multiplexing doesn't work every time. With non-zero probability multiple tenants will use the same resource, which causes poor and unpredictable performance; and (b) tenants pay for the resources they don't use.

There are various reports that quantify negative effects of the overbooking policy on cloud tenants -- [ioverbook](https://ieeexplore.ieee.org/abstract/document/6973784), [awsinsider](https://awsinsider.net/articles/2017/11/20/rightscale-aws-overpay-6-billion.aspx), [kostner](https://kostner.com/2019/02/28/there-is-no-reason-to-overpay-for-cloud/). According to these reports, tenants on average do not utilize 35% of resources they are paying for.


Quantifying unused resources
------

The rule of thumb for cloud computing users is pay-for-what-you-use. Obviously, the overbooking model is far from providing this policy. The first step in fighting it is to make cloud users aware of the existence of this problem. Thus, I'm writing a simple script for AWS that will estimate resource utilization over time and use it to calculate the cost of resources that are not being used.

The code is under construction and can be found [here](https://github.com/vojislavdjukic/cloud-waste-meter).

Let me know how much do you waste.