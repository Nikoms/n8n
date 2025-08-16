---
title: Lesson 167 - Architecture vs Design (en)
date: 2025-08-17T00:16:20.827+02:00
category: videos
tags: [software architecture, design, architecture vs design, microservices, strategy design pattern, software development, decision making, system design]
excerpt: Discussion on understanding the spectrum between software architecture and design, criteria to differentiate them, and examples illustrating how decisions vary in responsibility and impact.
---

![thumbnail](https://i.ytimg.com/vi/0tEBv2kAuNY/maxresdefault.jpg)
[https://youtu.be/0tEBv2kAuNY?si=vizR1lxq2pKyabTa](https://youtu.be/0tEBv2kAuNY?si=vizR1lxq2pKyabTa)

## My thoughts

Not specified (yet)

## TLDR;
- Architecture vs Design is a spectrum, not a binary distinction.
- Criteria to differentiate include structural impact, strategic vs tactical nature, effort level, and significance of trade-offs.
- Architectural decisions involve system structure, are strategic, require high effort, and have significant trade-offs.
- Design decisions are focused on source code, tactical, require low effort, and have less significant trade-offs.
- Responsibility for decisions depends on where they lie on the spectrum: architects handle architectural decisions; developers handle design decisions.
- Examples: Microservices (architectural, strategic, high effort, significant trade-offs), Strategy design pattern (design, tactical, low effort, less significant trade-offs), Splitting payment service (between architecture and design, tactical, moderate effort, significant trade-offs).
- Using these criteria helps clarify responsibility and impact of decisions in software projects.



## Content

### Understanding the Difference Between Architecture and Design
In lesson 167 of Software Architecture Monday, Mark Richards explores a nuanced perspective on the difference between architecture and design. Contrary to thinking of these as distinct categories, Richards explains that the difference is better understood as a spectrum of decisions that range from architectural to design considerations. "The difference between architecture and design is not a binary decision but rather a spectrum of decisions," he states.

### Key Criteria to Distinguish Between Architecture and Design
Richards offers four criteria to help determine where a decision lies on the spectrum:

1. **Structural Aspect vs. Source Code:** Architectural decisions influence the structural organization of components, their coupling, deployment units, communications, and database interactions. Design decisions relate to coding practices and source code organization.

2. **Strategic vs. Tactical:** Strategic decisions typically involve multiple people, take weeks or months, and have broader impact. Tactical decisions can be made quickly by one or two people.

3. **Level of Effort:** Architectural decisions generally require greater effort and resources, whereas design decisions are less demanding.

4. **Significance of Trade-offs:** Every decision involves trade-offs; significant and impactful trade-offs usually signal architectural concerns, while minor trade-offs suggest design.

### Why This Distinction Matters
This framework serves two important purposes. First, it helps identify who should be responsible for making a decision—the architect or the development team—while emphasizing the importance of collaboration. Second, it clarifies the overall impact of decisions, as architectural decisions tend to influence system-wide aspects significantly more than design choices.

### Practical Examples
Richards illustrates these criteria with three examples:

- **Choosing Microservices:** An architectural decision because it determines system structure, requires strategic planning with many stakeholders, involves high effort, and includes significant trade-offs like complexity and cost versus scalability and fault tolerance. "This is why this is on the far end of the architecture side of the spectrum."

- **Using the Strategy Design Pattern:** Falls clearly in the design category as it relates to source code, is tactical and quickly made, involves low effort, and has minor trade-offs. "A development team or a developer would have the responsibility for making this decision."

- **Breaking Up a Payment Service into Multiple Services:** This decision lies in the middle of the spectrum. It affects deployment units and structural aspects but is more tactical and requires moderate effort. The trade-offs, such as potential performance impacts and data integrity concerns balanced against improved agility, are significant but not as extreme as microservices. "This is where most of your decisions will lie."

### Conclusion
By applying these criteria and understanding the spectrum between architecture and design, teams can better assign responsibilities and anticipate the impacts of their decisions. Mark Richards encourages the thoughtful use of this framework to avoid overlapping roles and to ensure the right people make the right decisions at the right level. "This kind of tool helps avoid stepping on each other's toes or making a decision that we probably shouldn't have the responsibility to make."

Thank you for engaging with this lesson, and stay tuned for the next installment of Software Architecture Monday.




> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/409](https://github.com/Nikoms/n8n/tree/main/ongoing/409)