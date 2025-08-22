---
title: Lesson 167 - Architecture vs Design (en)
date: 2025-08-22T17:33:26.163+02:00
category: videos
tags: [software architecture, design, architecture vs design, microservices, strategy design pattern, software development, decision making, system design]
excerpt: Mark Richards explains the nuanced spectrum between software architecture and design, providing criteria to distinguish them and examples to clarify responsibility in decision-making.
---

![thumbnail](https://i.ytimg.com/vi/0tEBv2kAuNY/maxresdefault.jpg)
[]()

## My thoughts

The video outlines four key criteria to differentiate between architecture and design decisions:

- Whether the decision involves structural aspects of the system (such as component organization, deployment units, and communication) or just source code.
- Whether the decision is strategic (involving many people and taking weeks or months) or tactical (quick decisions by few people).
- The level of effort required, with higher effort decisions leaning more towards architecture.
- The significance of trade-offs, where more impactful pros and cons indicate architectural decisions and less significant ones indicate design decisions.

## TLDR;
- The difference between architecture and design is a spectrum, not binary.
- Criteria to determine a decision's place on the spectrum: structural aspect, strategic vs tactical, level of effort, and significance of trade-offs.
- Architectural decisions involve system structure, strategic planning, high effort, and significant trade-offs.
- Design decisions focus on source code organization, are tactical, low effort, and have less significant trade-offs.
- Responsibility for decisions varies: architects handle more strategic and impactful architectural decisions, developers handle tactical design decisions.
- Many decisions fall between the two extremes, combining architectural and design elements.
- Using criteria helps clarify who should ultimately be responsible for decisions and clarifies the impact on the system.



## Content

### Understanding the Spectrum Between Architecture and Design
Mark Richards explains that architecture and design are not strictly separate but exist on a continuum. This nuanced perspective helps professionals understand how decisions vary based on their characteristics rather than viewing these disciplines in isolation.

> "The difference between architecture and design is not a binary decision but rather a spectrum of decisions that lie between architecture and design."

### Criteria to Determine Placement on the Spectrum
Four key criteria assist in locating a decision on the architecture-design spectrum:

- **Structural Aspect:** Does the decision affect the overall system organization such as components, deployment units, and communication patterns, or is it primarily about how source code is written?
- **Strategic vs Tactical:** Strategic decisions involve many stakeholders and take weeks or months; tactical decisions involve fewer people and can be made quickly.
- **Level of Effort:** Architectural decisions usually require high effort, while design decisions are often low effort.
- **Significance of Trade-offs:** Important trade-offs with systemic impact lean toward architecture; minor trade-offs align with design.

### Example 1: Microservices as an Architectural Decision
Choosing microservices embodies architectural decision criteria:

- It impacts system structure by defining deployment units.
- It is strategic, involving many people over weeks or months.
- The effort required is substantial.
- Trade-offs are significant, balancing scalability and fault tolerance with complexity and cost.

> "Choosing to use microservices involves significant trade-offs with high impact, placing it clearly on the architecture side of the spectrum."

### Example 2: Strategy Design Pattern as a Design Decision
Choosing the strategy pattern typifies a design decision:

- It concerns code organization rather than system structure.
- It is tactical, typically decided within an hour by a small team.
- The effort required is low.
- Trade-offs are minor and less impactful.

> "This falls on the far end of the design spectrum because it is a tactical, low-effort decision with less significant trade-offs."

### Example 3: Breaking up a Payment Service – A Middle Ground
Deciding to break a payment service into multiple services sits between architecture and design:

- It affects structure by creating new deployment units and communications.
- It is more tactical than strategic, decided by a few people relatively quickly.
- Effort is moderate, involving code movement and some architectural considerations.
- Trade-offs are significant, influencing performance, data integrity, and system agility.

> "This decision lies in the gray area but leans towards the architectural side due to the impact and trade-offs involved."

### Why This Distinction Matters
Understanding where a decision lies on this spectrum helps clarify who should take responsibility. Architects typically own strategic, high-impact architectural decisions, while developers handle tactical design choices. Collaboration remains crucial, but ultimate accountability varies.

> "This kind of tool helps avoid stepping on each other's toes or making a decision that we probably shouldn't have the responsibility to make."

Mark concludes that applying this framework empowers both architects and developers to manage decision-making responsibilities effectively, ultimately improving system outcomes and teamwork in software development.





> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/601](https://github.com/Nikoms/n8n/tree/main/ongoing/601)