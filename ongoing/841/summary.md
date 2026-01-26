---
title: "CRUD API + Complexity = Death by a 1000 Papercuts (en)"
date: 2026-01-26T16:26:41.152+01:00
category: videos
tags: [CRUD, software architecture, business rules, entities, event-driven architecture, domain-driven design, microservices, event sourcing]
excerpt: "Derek Colmartin explains why focusing solely on CRUD over entities can obscure business rules and cause maintenance issues, advocating for an explicit task-driven approach that captures user intent and simplifies complex domain logic."
---

![thumbnail](https://i.ytimg.com/vi/kalD8TcRBCc/maxresdefault.jpg)
[https://youtu.be/kalD8TcRBCc?si=iUGOc0EeGUy64uRN](https://youtu.be/kalD8TcRBCc?si=iUGOc0EeGUy64uRN)

<!--- My thoughts -->

## Content

### Understanding the Limitations of CRUD with Entities
Derek Colmartin from CodeOpinion.com explains how traditional CRUD methods, focusing on entities in Create, Read, Update, Delete operations, often push the responsibility of understanding workflows and business rules onto the end users. This means critical information remains in users’ minds rather than being captured within the system itself. While CRUD can be appropriate for simple scenarios, it becomes unwieldy as the domain grows in complexity.

He highlights that many common approaches, especially RESTful services modeled around entities, result in clients fetching entity representations, modifying them, and sending them back, treating the application service as little more than a proxy to the database. This pattern can easily lead to scattered and duplicated business logic either on the client or server side, creating maintenance challenges and confusing end users about system behavior.

### Why CRUD Fails to Capture User Intent
Using simplistic CRUD forms, users can change any entity property without clear intent, leading to a fragile system where subtle but important business rules must be enforced in code to maintain data integrity.

For example, Derek shares rules like "a product cannot be for sale if its quantity is zero or its price is zero." Enforcing these rules in code means that if a user sets zero quantity, the system automatically disables the sale status. However, this can confuse other users who do not understand why the product is marked unavailable, as the implicit business rules are hidden in the codebase.

He explains that gradually adding such business rules results in a "death by a thousand paper cuts" where multiple conditional checks accumulate, making the system harder to manage and reason about. Moreover, the logic may reside in multiple places if there are several clients or services interacting with the same data.

### Moving Beyond CRUD: Focusing on Explicit User Tasks
The alternative Derek proposes is to move away from generic CRUD operations and instead design the system around explicit user tasks or business capabilities. This means users declare their intent clearly when performing modifications.

In the inventory example, instead of arbitrarily changing the quantity on hand, the user performs predefined tasks such as "ship product," "receive product," or "inventory adjustment." Each task has clear business semantics and encapsulates the reasons behind the changes. This approach captures user intent explicitly and makes the operations more meaningful and manageable.

### Implementing Behavior-Driven Entities
Central to this approach is encapsulating state-changing logic within entity classes themselves. Properties like price, cost, and quantity are made private with state changes occurring only through well-defined methods representing business operations. This ensures all business rules related to these changes remain centralized and consistent.

Derek shows that while certain properties—like name and description—can remain simple CRUD fields when intent does not matter, other key business-related properties must be manipulated only via explicit actions. This helps maintain clarity both in the UI and the backend.

### Benefits and Broader Impact
By requiring users to explicitly state what they are doing, systems become easier to understand and maintain. Validation and user feedback improve, as users get immediate clarity on why certain actions cannot proceed.

Such explicit actions also fit naturally into event-driven architectures, allowing the system to publish meaningful events about exactly what operations were performed, enabling better monitoring, auditing, and system integration.

### Final Thoughts
CRUD itself is not inherently bad and remains suitable for simple scenarios. However, as Derek explains, when domain complexity rises, relying solely on CRUD and entities leads to hidden logic, confusing user experiences, and maintainability issues. Transitioning to task-focused, behavior-driven design captures intent clearly and enforces business rules effectively, offering a robust foundation for complex systems and event-driven design.

He encourages developers to reflect on their approach and consider implementing explicit business capabilities within their entities, improving clarity, user experience, and system correctness.
