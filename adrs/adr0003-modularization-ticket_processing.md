# ARD0003 - Modularization of Ticket Processing
Creation: 28.Apr.2021

## Status (proposed, accepted, rejected, deprecated, superseded)
tbd

## Context
There are two possibilites to model the processing of tickets in the system.  
- Two modules approach:  
  - Module "Ticket Capture" - having the responsibility to capture a client's ticket.  
  - Module "Device Repair" - having the responsibility to fullfill the ticket (used mostly by the Expert during the repair process).  
<p align="center">
<img width="50%" src="images/ticket-capture-device-repair.png"/>  
</p>
- One module approach:  
  - Ticket Handler aggregating the 2 modules above into a single module.
<p align="center">
<img width="50%" src="images/ticket-handler.png"/>  
</p>
The "Two modules approach" enforces better segregation of duty and alows for higher maintainability.  
The "One Module approach" reduces system complexity, centralizing ticket handling   

## Decision

tbd


## Consequences

What becomes easier or more difficult to do because of this change?