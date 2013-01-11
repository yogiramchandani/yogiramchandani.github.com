---
layout: post
title: Enterprise Service Bus
tags:
- esb
- architecture
---

### Enterprise Service Bus ###

[![Service Broker](http://yogiramchandani.com/static/images/2013-01-11-enterprise_service_bus/esb.jpg)](http://yogiramchandani.com/static/images/2013-01-11-enterprise_service_bus/esb.jpg)

[\* http://en.wikipedia.org/wiki/File:ESB_Component_Hive.png](http://en.wikipedia.org/wiki/File:ESB_Component_Hive.png)

[**Characteristics:**](http://www.consultoriajava.com/articulos/esb_arquitecture_software_product.shtml)

*	An architectural style built on top of a Broker or a Bus, when built on top of a Broker its very similar to an EAI
*	[No global standard for ESB](http://davidchappellopinari.blogspot.co.uk/2005_12_01_archive.html)
*	Big differences between vendors
*	Protocol Bridging
*	Handles application adapters, routing of messages based on rules, and data transformation engine
*	"Enterprise Service Bus," author David Chappell states that "Rather than conform to the hub-and-spoke architecture of traditional enterprise application integration products, ESB provides a highly distributed approach to integration." * Most big vendors still follow the hub-and-spoke architecture
*	general agnosticism to operating-systems and programming-languages; for example, it should enable interoperability between Java and .NET applications
*	Using the broker pattern, single point of failure, must be robust and performant. But can be overcome using redundancy – which in turn introduces complexity:

>> [Two patterns for distributed systems: Enterprise Service Bus (pdf) Page 6/15](http://www.hillside.net/plop/2011/papers/B-31-Fernandez.pdf)

**Advantages:**

*	Infrastructure features managed centrally.
*	Standardises communication for heterogeneous services. 

**Disadvantages:**

*	[Too much responsibility. Many requests will be serviced by infrastructure features that they do not need.](http://www.infoq.com/articles/ESB-alternative)
*	[Causes vendor lock-in.](http://www.infoq.com/articles/ESB-alternative)
*	Hard to test infrastructure features.
*	Slower communication due to infrastructure overhead.
*	On [Content Based](http://www.udidahan.com/2011/03/20/careful-with-content-based-routing) Routing : 

>>“[When implementing a Content-Based Router, special caution should be taken to make the routing function easy to maintain as the router can become a point of frequent maintenance](http://www.eaipatterns.com/ContentBasedRouter.html)”<br/>
- Enterprise Integration Patterns
Gregor Hohpe and Bobby Woolf



