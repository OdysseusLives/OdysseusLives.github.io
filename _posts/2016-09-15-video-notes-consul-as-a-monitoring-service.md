---
layout: post
title:  "Video Notes: Consul as a Monitoring Service"
date:   2016-09-15 10:16:00
categories: technical
---

\#videoNotes

# [Consul as a Monitoring Service](https://www.youtube.com/watch?v=UK3EFUcS-Ps)
Presenter: Seth Vargo 

Location: DevconTLV 

Date: March 2016

## Summary
Rating: 5/5

Great introduction to Consul. This starts with the problems that are experienced with a service-oriented architecture at scale, and why Consul was created. 

The speaker is well rehearsed, provides great information, and maintains a great use of great visuals. There's a lot of great information here delivered in easily digestible bites that form a cohesive narrative. 

## Notes

### Why is Consul needed
Using service or microservice architecture introduces questions: 
- how do I identify a service
- how do I talk to the nearest service

#### SOA primer
- Autonomous
- Limited scope
- Loose coupling 

### Service Discovery 
How to find the correct node to talk to in a cluster

- the closest 
- the least burdened

Traditionally: use HAProxy or NGNX in front of the services so you can use a well-known IP in your web-app yet get load balancing and round-robining

You can “pretend that you don’t need service discovery”

Yet you’ve introduced a single point of failure 

And how do find healthy/unhealthy nodes?

And how do you give immediate configuration to a node?

These are the 4 basic SOA/microservices problems 

### Service Discovery 
How do I find the things?

Done with HTTP API + DNS API

Also: Datacenter aware 

### Load Balancing
Accurately balance the weight 

Adding nodes to a cluster and routing traffic there immediately becomes easy

### Health Checking
Don’t send traffic to bad nodes

Unhealthy nodes are discovered immediately, and traffic is routed away from these immediately 

### Key Value Configuration 
Turn and toggle feature flags/ runtime components 

### Leader election

Has leader election algorithm (or make your own)

Can communicate with servers in different datacenters 

### Semaphore Locking
Consul lock can be used for providing high availability (HA) to bits that don’t normally allow for HA ~ Vault, Redis 
solves the “exactly one must always be running”

Also useful for rolling restarts, kernel upgrades.  I.e., you can update 2 of 50 at a time

### Responsive

Done via health checks

Traditional monitoring service (like nagios or sensu)

- pull model 
- silo with a central point of failure 
- can’t restart a server for you, if it needs it 
- a human must touch machines after machines are on fire 

Consul is bidirectional

- receive messages from consul servers
- send messages to consul servers

unhealthy nodes are not returned from health or dns queries

### Scalable
Notifies on state change only, rather than sending thousands of requests 

- Not sending unneccesary network traffic across the load

This is the advantage of a gossip-based protocol: nodes around a particular node will report a node is missing.  

- The surrounding nodes “narc” that a node is missing from the cluster.

- Liveliness is determined by your peers

Can run with a ```-dev``` flag on your local machine to get up and running quickly 

## Quotes
“Nothing’s complete without an animated gif.”