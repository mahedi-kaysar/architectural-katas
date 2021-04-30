# ADR0004 - Customer and Call Center Staff modularization
Creation: 28.Apr.2021

## Status (proposed, accepted, rejected, deprecated, superseded)
accepted

## Context

Customer and Call Center Staff have a set of possible actions which overlap, indicating the superset of actions can be handled by the same module.  
Digitalization of platforms speak for unification and consolidation of systems supporting internal (to be company) and external users.   
Nevertheless, Call Center Staff diverge in operational characteristics - Considering that Call Center is an internal department of the company, there is no reputational risk in case of  outages (no reputational risk).  
On the other hand, potential downtime on modules interfacing with Customer are susceptible to reputational risks. 


## Decision

Customer actions and Call Center actions will be supported by the same module.  
Customer and Call Center will have distinct entitlements and supported by the same business service.  


## Consequences

Excelence on software Quality Control and Test Coverage for the unified module must be achieved in order to mitigate reputational risks.
