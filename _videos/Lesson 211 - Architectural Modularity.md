---
title: "Lesson 211 - Architectural Modularity (en)"
date: 2025-09-15T11:10:51.242+02:00
category: videos
tags: [software architecture, modularity, microservices, scalability, maintainability, testability, deployability, fault tolerance]
excerpt: "Mark Richards explains architectural modularity, exploring its benefits on maintainability, testability, deployability, scalability, and fault tolerance, and cautions about the risks of improper granularity.
---

![thumbnail](https://i.ytimg.com/vi/DApenk3-0Gc/maxresdefault.jpg)
[https://youtu.be/DApenk3-0Gc?si=shH0T9aiv5si1_uq](https://youtu.be/DApenk3-0Gc?si=shH0T9aiv5si1_uq)

## My thoughts

Not specified (yet)

## TLDR;
- Modularity means breaking systems into smaller separately deployed units, unlike granularity which is about the size of those units.
- Five key drivers of architectural modularity are maintainability, testability, deployability, scalability, and fault tolerance.
- Maintainability: easier to locate and apply changes in modular systems compared to large monoliths.
- Testability: modular systems reduce the testing scope and completeness concerns compared to monoliths.
- Deployability: modular deployments involve less ceremony, higher frequency, and lower risks.
- Scalability: modules allow scaling only necessary functions rather than the entire system.
- Fault tolerance: failures affect only individual modules, not the whole system.
- Excessive coupling among modules negates these benefits, leading to increased complexity and risk, which relates to granularity issues.



## Content

### Understanding Architectural Modularity
In this lesson, Mark Richards delves into the distinction between modularity and granularity in software architecture. He clarifies that modularity refers to partitioning systems into smaller, separately deployable units of software, while granularity pertains to the size of these individual units. Mark cautions with his notable quote, "embrace modularity, but beware of granularity," highlighting that granularity is often where architectural mistakes occur. The lesson focuses on modularity, a prevailing trend driven by the need to move from large monolithic or legacy systems toward architectures such as service-based, microservices, or event-driven models.

### The Five Drivers of Architectural Modularity
Mark identifies five primary drivers explaining why architectural modularity is crucial:

#### 1. Maintainability
Maintainability is about the ease of applying and locating changes within a system. In large monolithic systems, pinpointing where to apply fixes can be challenging and uncertain, often with no team member fully understanding the entire codebase. Modularity simplifies this by allowing change application at the specific unit of software, making it easier and more reliable to maintain.

> "If I move to a level of modularity, I go to the unit of software where that change needs to be applied and it's much easier to locate that change."

#### 2. Testability
Testability encompasses the ease and completeness of testing. Making changes in monolithic systems entails the risk of breaking other parts, often requiring extensive regression testing which can be time-consuming. Modularity reduces testing scope by isolating changes to smaller units of software, thus enabling more focused and efficient testing.

> "What I should be testing is the entire system... whereas if we move to a level of modularity, I apply that same change to a smaller unit of software."

#### 3. Deployability
Deployability involves the complexity, frequency, and risk associated with deploying software. Monolithic deployments often have lengthy ceremonies, infrequent deployment cycles, and high risks due to the size of the unit. In contrast, modular systems can have simpler deployment processes, potentially daily deployments with minimal risk, such as a simple command line operation in microservices.

> "In microservices, deployment may be just a matter of a command line, enabling daily frequency and lower risk."

#### 4. Scalability
While monoliths can be scaled, it is often inefficient because the entire system is scaled regardless of actual need. Modularity allows scaling specific features or functions individually, making scaling more targeted, cost-effective, and agile.

> "In architectural modularity, scaling happens at a function level, not a system level."

#### 5. Fault Tolerance
Failures in monolithic systems can bring down the entire system since all functionalities are tightly coupled. With modularity, faults in one service affect only that service, leaving others operational and maintaining overall system availability.

> "With architectural modularity, a fault in a service only brings that service down and not the entire system."

### The Caveat of Coupling and Granularity
Mark also warns of the downside when modular services become too interdependent through excessive communication or coupling. This situation can undermine all the benefits: maintainability becomes difficult, testing requires checking all services, deployments revert to lengthy cycles, scalability demands scaling multiple modules, and a fault in one service can halt the entire system. This scenario usually stems from improper granularity, a subject Mark plans to address in a future lesson.

### Conclusion
Mark Richards' lesson offers a comprehensive and insightful explanation of why architectural modularity matters in modern software development, highlighting its core benefits while cautioning against pitfalls related to granularity and coupling. This knowledge is essential for teams aiming to transition effectively away from monolithic systems toward modular architectures that enhance maintainability, testability, deployability, scalability, and fault tolerance.




> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/674](https://github.com/Nikoms/n8n/tree/main/ongoing/674)