# architectural-katas

<p align="center">
<img width="50%" src="images/approach.png"/>  
</p>

## Introduction

The given Sysops Squad system has many drawbacks that include customer and call center stuff complains about losing track of the created tickets, wrong consultant shows up to fix the customer's problem, system freezes or crashes during a spike and changes in the system is very difficult due to its monolith archtecture. These drawbacks are due to not having proper architectural dicision and design. In order to resolve those problems we have considers following set of actions:
* Understanding the problems and identified the architectural characterstics for solving the problems
* Defined the new architeture style by Actor/Action and Event Storm approaches. 
* Define some ADRs

## Architecture Characteristics

We have analysed the slides and the video in order to extract the main challenges faced by sysops with the existing system.
Once we identified the main issues (represented below by the pink stickers) we verified which Architecture Characteristics (Scalabilty, Elasticity, Fault-tolerence, Testability and Evolbalility) are most relevant to address the identified issues. As a reference for the list of architecture characteristics we utilized the book [Mark Richards and Neal Ford, Fundamentals of Software Architecture](https://learning.oreilly.com/library/view/fundamentals-of-software/9781492043447/). The architecture characteristics are represented by the yellow stickers below.

<p align="center">
<img width="50%" src="adrs/images/issues-and-quality-attributes.png"/>  
</p>

## Architecture Style
There are different types of architecurual style exist (Layered, Modular-Monolith, Microkernel, Microservice and so on) and those are also mentioned in the book [Mark Richards and Neal Ford, Fundamentals of Software Architecture](https://learning.oreilly.com/library/view/fundamentals-of-software/9781492043447/). We have analised the pros and cons between the two style that include modular-monolith and microservice architecture. Finally we have decided to use microservic architecutural sytle in order to solve the current system architecutre.

<p align="center">
<img width="100%" src="adrs/images/architecture-styles-worksheet-annotated.png"/>  
</p>

## Actor/Action
Here, we have identified the actors and actions from the exiting architecture and given functinalites of the system.

<p align="center">
<img width="100%" src="images/actor-action.png"/>  
</p>

## Event Storm
The Actor/Action method allowed us to have a first view of the services and the interaction among them.
Moreover, we have utilized the event storm to build understanding and confidence on the solution approach we are proposing. As the diagram below shows, we could visualize the functions that would be implemented by each service and also the way the services would interact in the future platform.

<p align="center">
<img width="75%" src="images/sysops-event-storm.png"/>  
</p>

## Architectural Topology

<p align="center">
<img width="100%" src="images/katalysts_arch.png"/>  
</p>

| Component        | Descriptions|
| ------------- |:-------------:|
| Contract Capture Service      | right-aligned |
| Ticket Capture Service      |       |
| Ticket Allocation Service      |       |
| Device Repair Service      |       |
| Survey Fulfillment Service      |       |
| Knowledge Base Service      |       |
| Administrator Service      |       |
| Analytics Service      |       |
| Logging and Aggregration service     |       |


## Data Model

<p align="center">
<img width="100%" src="images/datamodel.png"/>  
</p>
