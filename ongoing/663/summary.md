---
title: "Lesson 211 - Architectural Modularity (en)"
date: 2025-09-15T11:07:28.794+02:00
category: videos
tags: [software architecture, modularity, microservices, scalability, fault tolerance, maintainability, testability, deployability]
excerpt: "Mark Richards discusses architectural modularity in software systems, outlining its benefits and cautioning against granularity issues that can undermine these advantages.
---

![thumbnail](https://i.ytimg.com/vi/DApenk3-0Gc/maxresdefault.jpg)
[https://youtu.be/DApenk3-0Gc?si=shH0T9aiv5si1_uq](https://youtu.be/DApenk3-0Gc?si=shH0T9aiv5si1_uq)

<!--- My thoughts -->

## Content

### Understanding Architectural Modularity: Why It Matters

Mark Richards opens this 211th lesson of Software Architecture Monday by explaining the vital distinction between modularity and granularity in software architecture. Modularity is the act of breaking a system into smaller, independently deployable software units, whereas granularity concerns the size of these units. He quotes, "Embrace modularity, but beware of granularity," emphasizing that granularity often causes pitfalls.

### The Five Key Drivers of Architectural Modularity

Richards highlights five main drivers that make architectural modularity important:

1. **Maintainability**
   - In large monolithic systems, identifying where to apply changes is difficult because not all team members understand the entire codebase.
   - With modularity, changes are localized to specific units, making it easier and more efficient to identify and apply fixes.
   - "It's much easier to locate that change" when working with modular units.

2. **Testability**
   - Testability refers both to the ease and completeness of testing.
   - Large monoliths require extensive regression testing, often covering thousands of tests which may take hours or days.
   - Modular units reduce testing scope significantly, enabling faster and more focused tests.

3. **Deployability**
   - Deployability concerns the deployment ceremony, deployment frequency, and deployment risk.
   - Monolithic systems often require complex, lengthy deployment processes, with code freezes and mock deployments.
   - Modular systems, such as microservices, allow simple command-line deployments that can be done daily, greatly lowering risk.

4. **Scalability**
   - While scaling monoliths is possible, it is costly and inefficient as the entire system scales, regardless of demand.
   - Modularity enables scaling at the function or feature level, scaling only the parts that need it.

5. **Fault Tolerance**
   - Failure in a monolith can cause the entire system to go down.
   - Modular systems isolate faults to individual services, preventing system-wide failures.

### The Caution: The Impact of Coupling and Granularity

Richards warns that the benefits of modularity can be lost if services become tightly coupled:

- Inter-service communication may increase, causing maintainability issues.
- Changes in one service require testing across others, negating testability gains.
- Deployment can become complex again, often leading to infrequent or weekend releases.
- Scalability suffers if scaling one module necessitates scaling others.
- Fault tolerance diminishes as failures propagate across services.

He notes that these problems relate mostly to granularity, a topic slated for a future lesson.

### Conclusion

This lesson provides a comprehensive overview of why organizations are breaking large monolithic or legacy systems into modular architectures such as microservices or event-driven systems. By focusing on modularity and its drivers—maintainability, testability, deployability, scalability, and fault tolerance—architects can build more manageable, adaptable, and resilient systems. However, attention must be paid to granularity to avoid undermining these benefits.
