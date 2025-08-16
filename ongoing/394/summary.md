---
title: Lesson 167 - Architecture vs Design (en)
date: 2025-08-16T23:45:41.783+02:00
category: videos
tags: [software architecture, design, microservices, decision making, software development, strategy, tactics, architectural decisions]
excerpt: Mark Richards discusses the spectrum between software architecture and design, outlining criteria to distinguish decisions, their impact, and responsibility.
---

![thumbnail](https://i.ytimg.com/vi/0tEBv2kAuNY/maxresdefault.jpg)
[https://youtu.be/0tEBv2kAuNY?si=vizR1lxq2pKyabTa](https://youtu.be/0tEBv2kAuNY?si=vizR1lxq2pKyabTa)

<!--- My thoughts -->

## Content

### Understanding the Difference Between Architecture and Design

In software development, distinguishing between architecture and design is crucial but often misunderstood. This lesson explores why the difference is not a simple binary but exists on a spectrum. Mark Richards explains how decisions in software projects can range from architectural to design based on various criteria.

"The difference between architecture and design is not a binary decision but rather a spectrum of decisions that lie between architecture and design."

### Key Criteria to Determine Architecture vs. Design

Mark introduces four primary criteria to evaluate where a decision lies on the architecture-design spectrum:

- **Structural Aspect:** Does the decision concern the organization of source code into components or deployment units and their communication (architecture), or does it relate to how source code is written and organized internally (design)?
- **Strategic vs. Tactical:** Is the decision strategic, requiring many stakeholders and weeks or months of planning, or tactical, resolvable quickly by one or two people?
- **Level of Effort:** Does the decision involve substantial effort (architectural) or minor changes (design)?
- **Significance of Trade-offs:** Are the trade-offs of the decision significant and impactful (architecture) or relatively minor (design)?

### Why This Distinction Matters

Mark highlights two main reasons this distinction is important:

- **Decision Responsibility:** Understanding where a decision falls helps determine who should ultimately make it—architects or developers—although collaboration is essential.
- **Impact Awareness:** Architectural decisions typically have a larger impact on system quality and function than design decisions.

"Knowing when you make a decision what's the overall impact matters; architectural decisions tend to have a higher impact."

### Examples Along the Spectrum

Mark gives clear examples illustrating decisions at various points on the spectrum:

- **Using Microservices:** This decision is architectural because it defines the system's structural style. It is strategic, involves many stakeholders over weeks or months, requires high effort, and carries significant trade-offs like complexity and performance impacts.

- **Applying the Strategy Design Pattern:** This is a design decision focused on organizing source code. It is tactical, decided quickly by few people, requires low effort, and has less significant trade-offs.

- **Breaking a Payment Service into Multiple Services:** This example lies in the middle. It affects system structure somewhat, involves a few people tactically, requires moderate effort, and has fairly significant trade-offs like communication overhead and data integrity concerns.

### Practical Use of the Spectrum

This framework helps teams avoid confusion and overlap in decision-making responsibility. Architects can focus on bigger-picture structural choices, while developers manage detailed design decisions.

"This kind of tool helps avoid stepping on each other's toes or making a decision we probably shouldn't have the responsibility to make."

### Conclusion

Understanding where a decision lies between architecture and design leads to clearer responsibilities, better collaboration, and decisions that align with system impact. Utilizing criteria like structure, strategy, effort, and trade-offs guides teams toward more effective software development.

Stay tuned for more insights in upcoming lessons of Software Architecture Monday.
