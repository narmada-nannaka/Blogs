---
title: "Architecture Patterns"
slug: architecture-patterns

---

Unlike design patterns, architecture patterns can be applied right from the start of the solution planning. 

# Integration Types
## Information Portal
A portal where information is pulled from diverse systems - aggregate and present them in a single holistic view. For example, encompass entities to present information fired from different micros-services. 

## Data Replication
Multiple applications will have a copy of the same data. Data replication solves multiple purposes including restoring data during a disaster recovery event. For example - customer details are shared across flight management systems - ticket ordering,  billing and so on. 

## Shared Business Function
In contrast to the above pattern, this avoids data redundancy by creating a common service that can be accessed by other systems. In other words, integrate by data but by the same service. For example, customer address is a common example that can be implemented as a business function that can be tapped on by multiple systems. 

## Service-oriented architecture
A service is a typically well-defined function that is universally available to perform a specific operation. These services are made available for use by other systems that can act as service consumers. 

## Distributed Business Process Management
All relevant applications fall under the specific business function. Business capabilities are categorized and the applications specific to them fall under them. 

## Business to Business direct integration
Enterprises interact to share business data externally. 

Pattern Examples: 

Application Architecture = MVC, State Machine, Rules Engine
Integration Architecture = Service Bus, Adapter, ETL, Hub and spoke, REST
Infrastructure and platform Architecture = Horizontal scaling, vertical scaling, infrastructure virtualization, 3-tiered layering, DMZ, 

Microservices architecture - CQRS (Command Query and Responsbility segregation)
Domain driven design
Event-driven architecture
cloud-native architecture
APIs and API management
Digital decoupling

encompass data and functionality scope by boundaries to define the domain. This paves path for the domain-driven design. The domains defined will allows the micro-services. 

##Event Storming

The goal is to understand the ideal business process  not the current or future state technical implementation

A workshop done involving business (domain experts) and technology (architects and engineers) to model and understand business processes. 

Identify the process and the actors involved. 

lay out your boundaries around the context as we decompose the domains. 

it focusses on business processes, design level modelling. Not on classes, objects and databases = not preferred for technical discussions. 

Conversation starter

Definition of the language is understood when defining the big picture. 

what's the time limit for event storming session = challenge is to get the time of the SMEs. 
3 hour sessions to an all day sessions. 

Outcome = high level event map  which shows the sequence of events. Color coding for domain category and actors clearly identified. 

Use past tense to write the event. Order thim in sequence and identify any hot spots that requires resolution. 

Strategic Domain driven design - at least 1 or 2 iterations before moving to the tactical domain driven design phase. 

Develop ubiquitous language - design artifacts and development artifacts make up for the context artifacts.

Examples: Robotic Process Automation (RPA). If you do RPA on top of a broken process you won't get the business efficiency you are after. This is a perfect example to explore the ideal solution before automating the processes. 

second phase is where the developers and other Domain experts are involved to define the module context map and microservices. 

Development level coupling vs run-time coupling. 

cloud native vs cloud-based architecture

cloud native provides consistent user performance. Modular services make it easy to understand a number of deployment and operational tasks. Manageability ease of task, serverless is an example of cloud-native architecture. Infrastructure computing is not a point of concern. Increase velocity of business, method to get the team to take advantage through containerization, microservices. 





