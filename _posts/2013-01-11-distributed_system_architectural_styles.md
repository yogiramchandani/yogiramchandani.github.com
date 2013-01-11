---
layout: post
title: Distributed system architectural styles (Messaging)
tags:
- bus
- broker
- architecture
---

The intention of this post is to discuss the following styles founded on messaging:

*	Service Broker
*	Service Bus

SOA can be built on top of any of these styles (but not limited, i.e. non message based infrastructure).

### Service Broker ###
[![Service Broker](http://yogiramchandani.com/static/images/2013-01-11-distributed_system_architectural_styles/service_broker.jpg)](http://yogiramchandani.com/static/images/2013-01-11-distributed_system_architectural_styles/service_broker.jpg)

**Characteristics:**

*	Broker is physically separate.
*	All communication goes through the broker.
*	Broker handles failover, routing, Data Transformation.

**Advantages:**

*	Attempt to handle Spatial Coupling (not as well as Bus), however problem introduced - centralised Routing.
*	Concentrating all communications to a single logical entity, enables central management.
*	Enables “intelligent” routing, data transformation, orchestration.
*	Doesn’t require changes to surrounding apps.

**Disadvantages:**

*	The broker is a single point of failure, must be robust and performant. But can be overcome using redundancy – which in turn introduces complexity. 
*	Business logic is centralised.
*	Procedural programming at a large scale, without good unit testing or source control.
*	[Lack of accountability, which is the single source of truth?](http://www.udidahan.com/2011/03/24/bus-and-broker-pubsub-differences/)
*	[Cannot differentiate between Logical and Physical endpoint.](http://www.udidahan.com/2011/03/24/bus-and-broker-pubsub-differences/)

### Service Bus ###
[![Service Bus](http://yogiramchandani.com/static/images/2013-01-11-distributed_system_architectural_styles/service_bus.jpg)](http://yogiramchandani.com/static/images/2013-01-11-distributed_system_architectural_styles/service_bus.jpg)

**Characteristics:**

*	Bus is not necessarily physically separate (Think of it like a wireless card on the network).
*	Communication is distributed (No single point of failure).

**Advantages:**

*	No single point of failure.
*	Bus is simpler – no routing or service fail over.
*	[Doesn’t  break service autonomy.](http://en.wikipedia.org/wiki/Service_autonomy_principle)
*	[Reduces Spatial Coupling – “when one service is moved from one server to another this will not stop communications to that service”.](http://www.udidahan.com/2006/07/21/how-soa-helps-you-hit-the-agile-sweet-spot)
*	[Allows one Logical endpoint to scale out to multiple Physical endpoints.](http://www.udidahan.com/2011/03/24/bus-and-broker-pubsub-differences/)

**Disadvantage:**

*	More difficult to design distributed solutions than centralised ones.

