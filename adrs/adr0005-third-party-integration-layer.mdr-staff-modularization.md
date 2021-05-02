# ADR0005 - Third Party Integration Layer
Creation: 02.may.2021

## Status (proposed, accepted, rejected, deprecated, superseded)
accepted

## Context
There are two options to integrate the application with services outside the company - example Google Maps.  

1 - Direct integration: Here the microservices will call directly the external APIs in order to access their services.  
pros:
- reduced development time  
- less operational overhead  
cons:
- coupling internal services with external APIs/applications  

2 - Indirect access by using a 3rd party layer: Here the application microservices will call internal APIs on the 3rd party layer. The 3rd party layer will communicate with the external APIs.  
pros:  
- decopling the internal services from external apis
- individual scaling based on load  
cons:  
- operational overhead  
- increate development time  
## Decision

We decided to use Direct Integration.

## Consequences

Internal Microservices coupled with external APIs
