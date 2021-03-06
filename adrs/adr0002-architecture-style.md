# ADR0002 - Architecture Style
Creation: 26.Apr.2021

## Status (proposed, accepted, rejected, deprecated, superseded)
accepted

## Context
The current architecture style of the system is a monolith.  
The following limitations (red stikers) were identified when analysing the documentation/slides and video. The architecture characteristics (quality attributes) which needs to be addressed is shown in yellow.  
<p align="center">
<img width="50%" src="images/issues-and-quality-attributes.png"/>  
</p>
Moreover, it has been perceived that costs are not a main limiting driver for the architecture style. 
  
  
The possible Architecture styles are provided below. On the diagram we have the above identified architecture characteristics highlighted for the architectures which maximize the architecture characteristic.  
The **Microservices architecture** is the recommended architecture, as it maximizes the benefits of the most relevant architecture characteristics. 
<p align="center">
<img width="75%" src="images/architecture-styles-worksheet-annotated.png"/>  
</p>

## Decision

A Microservice Architecture with some elements of event-driven architecture to be used

## Consequences
Budget to be re-assured in light of the choice. Strong attention to platform monitoring/operation to mitigate operational issues.
