---
title: Lesson 167 - Architecture vs Design (en)
date: 2025-08-16T23:57:42.972+02:00
category: videos
tags: [software architecture, design vs architecture, microservices, strategy pattern, software design, software development, system architecture]
excerpt: Mark Richards explains the spectrum between software architecture and design, detailing criteria to differentiate them and examples to clarify decision responsibilities.
---

![thumbnail](https://i.ytimg.com/vi/0tEBv2kAuNY/maxresdefault.jpg)
[https://youtu.be/0tEBv2kAuNY?si=vizR1lxq2pKyabTa](https://youtu.be/0tEBv2kAuNY?si=vizR1lxq2pKyabTa)

## My thoughts

Très bonne vidéo. Elle explique clairement que la différence entre architecture et design n’est pas binaire, mais un spectre de décisions, allant des choix structurels et stratégiques aux détails tactiques du code. Le cadre proposé, basé sur la portée, l’effort, la stratégie et l’impact des compromis, est un excellent outil pour savoir qui doit prendre chaque décision. Utile pour clarifier responsabilités et impact dans un projet logiciel.

## TLDR;
- The difference between architecture and design is a spectrum, not a binary choice.
- Criteria to differentiate include: structural aspect vs source code focus, strategic vs tactical nature, level of effort, and significance of trade-offs.
- Architectural decisions often involve system structure, many people, high effort, and significant trade-offs.
- Design decisions focus more on source code details, are tactical, require low effort, and have less significant trade-offs.
- Examples: microservices are architectural; strategy design pattern use is design; breaking up a payment service lies in the middle but leans architectural.
- Understanding this spectrum clarifies who should have decision responsibility (architect vs developer) and the impact of decisions on the system.



## Content

### Understanding the Difference Between Architecture and Design

In lesson 167 of Software Architecture Monday, Mark Richards explores the nuanced distinction between software architecture and design. Far from being a simple binary, he explains that these concepts exist on a spectrum defined by several key criteria.

> "The difference between architecture and design is not a binary decision but rather a spectrum of decisions that lie between architecture and design."

### Defining the Spectrum Criteria

Richards outlines four criteria to determine where a decision falls on this spectrum:

- **Structural Aspect vs. Source Code:** Architectural decisions involve the system's structure, like component organization, deployment units, and communication patterns. Design decisions focus more on source code organization.
- **Strategic vs. Tactical:** Strategic decisions involve multiple people and can take weeks or months; tactical ones are typically decided by one or two people in hours or days.
- **Level of Effort:** Higher effort tends to indicate architectural decisions; lower effort usually signals design.
- **Significance of Trade-offs:** Significant trade-offs tend to be architectural; less significant ones lean towards design.

These criteria help clarify decision-making responsibility and the overall impact of choices made.

### Examples on the Spectrum

**Microservices Architecture:**

- A classic architectural decision as it defines system structure.
- Strategic, involving many people and time.
- High effort and significant trade-offs regarding complexity, cost, and performance.

**Strategy Design Pattern:**

- Primarily about coding practices, hence a design decision.
- Tactical and quickly decided.
- Low effort and minor trade-offs.

**Breaking Up a Payment Service:**

- Falls in the middle of the spectrum but leans architectural.
- Involves structural changes with some deployment considerations.
- More tactical, involving a small group making decisions quickly.
- Moderate effort with significant trade-offs concerning communication, performance, and data integrity.

> "This kind of tool helps avoid stepping on each other's toes or making a decision that we probably shouldn't have the responsibility to make."

### Why This Distinction Matters

Understanding where a decision falls helps assign responsibility appropriately—architects handle decisions with broader strategic impact, while developers manage tactical design choices. It also highlights the collaboration necessary before finalizing decisions.

Richards emphasizes the importance of this clarity to ensure smooth workflows and better system outcomes.

### Conclusion

This lesson provides a practical framework for distinguishing architecture from design, emphasizing the collaborative, spectrum-based nature of software decision-making. By applying these criteria, teams can better navigate responsibilities and system impacts in their projects.

Stay tuned for the next Software Architecture Monday lesson in two weeks!




> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/398](https://github.com/Nikoms/n8n/tree/main/ongoing/398)