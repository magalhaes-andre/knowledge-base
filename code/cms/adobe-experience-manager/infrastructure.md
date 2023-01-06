# AEM Infrastructure

## Clustering

## Dispatcher

Mainly, it is caching and/or load balancing. The usage of the load balancer is also helpful to protect the AEM server from attack, because it will be using cached pages. The main objective of the dispatcher is to cache the maximum content possible, and with that it won't need to access the layout engine. 

### Caching Strategies

- Cache as much content as possible (static pages)
- Access the layout engine as minimally.

### Caching Methods


- Invalidate pages which the content has been updates and replaces with new content
- Auto-invalidation automatically removes contents not relevant.


### Implementation of Multiple Dispatchers

It is possible, the only request is that n Dispatchers need to be able to access the CQ instance directly. A Dispatcher cannot handle requests coming from another Dispatcher.

### Cache Directory location

Web Server Root.

## Servlet Engine

The servlet engine behaves as a server within each CQ instance runs. Even if you run CQ without an application server, you'll always need a Servlet Engine

## Adobe Marketing Cloud

Adobe branded solution for digital marketing.

## AEM Available Interfaces

- CRX Explorer
- CRX Delite
- Apache Felix
- Site Admin
- etc/Tool