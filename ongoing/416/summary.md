---
title: Lesson 167 - Architecture vs Design (en)
date: 2025-08-17T00:24:18.234+02:00
category: videos
tags: [software architecture, design decisions, microservices, strategy pattern, system design, software development, architectural decisions, tactical decisions]
excerpt: Mark Richards explains the spectrum between software architecture and design, outlining criteria like structural impact, strategic nature, effort, and trade-offs to help clarify decision responsibilities.
---

![thumbnail](https://i.ytimg.com/vi/0tEBv2kAuNY/maxresdefault.jpg)
[https://youtu.be/0tEBv2kAuNY?si=vizR1lxq2pKyabTa](https://youtu.be/0tEBv2kAuNY?si=vizR1lxq2pKyabTa)

<!--- My thoughts -->

## Content

### Introduction to the Spectrum of Architecture and Design
In lesson 167 of Software Architecture Monday, Mark Richards explores the nuanced difference between architecture and design. Contrary to a common binary view, the difference is better understood as a spectrum of decisions varying in scope and impact.

> "The difference between architecture and design is not a binary decision but rather a spectrum of decisions that lie between architecture and design."

Mark introduces criteria to help determine where a particular decision falls on this spectrum, enabling clearer accountability and understanding of impact.

### Criteria to Differentiate Architecture and Design
Four main criteria guide us in positioning decisions along the architecture-design spectrum:

- **Structural Aspect:** Does the decision concern the system's structural organization (components, coupling, deployment units, communication, databases) or just the source code?
- **Strategic vs Tactical:** Are many people involved over weeks/months (strategic) or can it be decided quickly by one or two people (tactical)?
- **Effort Required:** Is the decision high effort (architectural) or low effort (design)?
- **Significance of Trade-offs:** Does the decision involve significant trade-offs impacting the system deeply or less significant ones?

### Why Distinguish Between Architecture and Design?
Knowing the nature of decisions helps assign responsibility correctly:

> "After collaboration, who ultimately has the responsibility for that decision?"

Architects should handle the architectural decisions, while developers often manage design decisions. This distinction also helps anticipate the overall impact of those decisions on the system.

### Example 1: Choosing Microservices (Architectural Decision)
Mark uses the example of deciding to use microservices as an architectural decision.

- It strongly concerns system structure since it defines component and deployment organization.
- The decision is strategic, involving many people and potentially taking weeks or months.
- It requires a high level of effort to implement.
- There are significant trade-offs, including benefits like scalability and fault tolerance counterbalanced by complexity and cost.

> "These trade-offs tend to be fairly significant... which is why this is on the far end of the architecture side of the spectrum."

### Example 2: Using the Strategy Design Pattern (Design Decision)
The choice to apply the strategy design pattern is mainly about how source code is organized.

- It primarily impacts code structure, not system architecture.
- The decision is tactical and can often be made quickly by a developer.
- It requires low effort compared to architectural decisions.
- Trade-offs are less significant.

> "A development team or a developer would have the responsibility for making this decision."

### Example 3: Breaking up a Payment Service (Middle of the Spectrum)
Deciding to break up a monolithic payment service into several services for different payment types illustrates a decision in-between architecture and design.

- It involves structural changes like creating new deployment units and altering communication patterns.
- The decision leans more tactical but is not as quick or isolated as design decisions.
- The effort needed is moderate since it primarily involves moving source code and re-architecting data access.
- Trade-offs are fairly significant due to effects on performance, data integrity, and agility.

> "This is where a lot of your... decisions will lie, more on the architectural side but balanced."

### Conclusion: Using the Spectrum to Assign Responsibility
By applying these criteria, developers and architects can effectively decide who should own particular decisions.

> "This kind of tool helps avoid stepping on each other's toes or making a decision that we probably shouldn't have the responsibility to make."

Understanding the spectrum between architecture and design not only clarifies roles but also highlights the varying impact decisions have on software systems.

### Looking Ahead
Mark Richards will continue exploring software architecture topics in future lessons, inviting viewers to stay tuned for the upcoming sessions in the Software Architecture Monday series.
