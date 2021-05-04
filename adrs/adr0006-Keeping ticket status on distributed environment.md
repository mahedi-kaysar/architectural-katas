# ADR0006 - Keeing Ticket State on Distributed environment
Creation: 04.may.2021

## Status (proposed, accepted, rejected, deprecated, superseded)

accepted

## Context

On a monolith architecture style the system can keep the transaction integrity at all times at cost of scalability. Duplication of data entities do no occur as all entities are accessible from the same runtime/application.
On a distributed architecture entities are segregated functionally per microservice. Nevertheless, some entity information might span across mulitple microservices. In our specific case, the status of a ticket (captured, allocated, fixed) spam accross multiple microservices: the "Ticket Capture", "Ticket Allocation" and "Device Repair". These microservices all contribute to the overall state of the Ticket.

There are 2 possible approaches to obtain the ticket status:
- microservices interested in the ticket status query all three services to reconstitute the final status.  
cons:
  - not easy to control, for instance if a new microservice, which updates the status, is added, all the other microservices must be updated.

- consolidate the state into a single microservice, propagating the changes on status done by other microservices. Microservices/UI interested into the status must query a single service.  
pros:
  - status is consolidated (owned) by one microservice 
cons:
  - other microservices needs to publish event changes.

## Decision

Centralize ticket updates (and also history) on "Ticket Capture". "Ticket Capture" must be highly available (due to exposure to end clients). Keeping the information there in an asynchronous manner does not hinder the availability of other services.

## Consequences

Single queue to capture status/history update to be consumed by "Ticket Capture"
