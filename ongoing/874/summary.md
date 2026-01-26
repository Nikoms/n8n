---
title: "A Real World Example of BDD (en)"
date: 2026-01-26T16:53:08.965+01:00
category: videos
tags: [BDD, acceptance testing, fintech, software development, continuous delivery, LMAX, Adaptive, Hydra, executable specifications, test automation, TDD]
excerpt: "Dave Farley explores real-world BDD style acceptance testing from Adaptive's fintech projects, showing how executable specifications drive development in complex trading systems."
---

![thumbnail](https://i.ytimg.com/vi/9P5WG8CkPrQ/maxresdefault.jpg)
[https://youtu.be/9P5WG8CkPrQ?si=gNu8-O9sqJR-qVqd](https://youtu.be/9P5WG8CkPrQ?si=gNu8-O9sqJR-qVqd)

<!--- My thoughts -->

## Content

### Introduction to Real World BDD Example

Dave Farley explores BDD (Behavior Driven Development) style acceptance testing through real-world examples from Adaptive, a London-based financial technology consultancy. Adaptive develops sophisticated, high-performance trading systems using a platform called Hydra. These tests not only verify functionality but also drive system development by acting as executable specifications.

> "It's often helpful to see what a real world example looks like — real code from a real project solving real problems."

### Technical Context: Managing Complexity with Hydra

Hydra abstracts accidental complexity — infrastructure, persistence, networking — to let developers focus on essential complexity, like business logic (e.g., account value calculation). The platform hosts single-threaded asynchronous services that encapsulate core domain logic while providing high performance, scalability, and reliability. This separation is a refinement of ideas initially pioneered at LMAX.

> "Hydra provides a blisteringly fast high quality infrastructure that takes care of pretty much all of the accidental complexity of the system."

### Acceptance Testing Strategy

Adaptive employs a two-layer testing approach:
- High-level BDD style acceptance tests specify desired system behaviors using executable specifications.
- Lower-level tests use traditional TDD for detailed unit and integration verification.

Acceptance tests begin by defining system configuration, typically including service engines, gateways, and clients. The speaker suggests separating system configuration from test code for flexibility, such as tagging tests and mapping these tags to configurations.

> "I would advise to separate the desired configuration of the system you want to test from the test itself."

### Example Acceptance Test Analysis

An example test involves setting up accounts, logging users in, and testing a deposit action. The test language is domain-specific but contains some implementation technicalities leaking into scenarios — e.g., references to API response codes or internal event emissions.

Dave suggests that tests should focus purely on the "what" (desired behavior) and hide the "how" (technicalities) within the DSL implementation. For instance, test scenarios might state "account successfully updated" rather than "API client receives empty response with status 202."

> "I think it's a good idea to keep executable specifications focused only on what the system needs to do, not how it does it."

The test code beneath the DSL is relatively simple but could benefit from further abstraction to reduce boilerplate and hide technical setup details.

### Trading Domain Scenario

A second scenario covers placing limit orders, a common trading action. The example uses domain-specific trading jargon and FIX protocol terms. Given FIX's dominance in institutional algorithmic trading, including some FIX terms is considered acceptable since they reflect the problem domain, although caution is advised to avoid excessive technical detail.

> "If you know anything about trading... you would be able to understand this example."

The scenario clearly expresses the trader's perspective and covers response verification meaningful to the user.

### Recommendations and Conclusion

Dave recommends further abstracting setup and DSL layers to improve test reuse, scaling, and clarity. He notes that Adaptive's tests cover important edge cases and failures, not just happy paths, which is essential for complex distributed systems.

> "These examples are very good real world examples of how to do a good job of BDD style acceptance testing."

The acceptance tests serve as a clear communication tool and development guide. Despite minor quibbles, Adaptive's approach demonstrates an effective method for using executable specifications in sophisticated fintech systems.

### Additional Resources

Links in the episode description provide more information on Adaptive, Hydra, LMAX architecture, the reactive manifesto, and Aeron, a high-performance messaging system underpinning Hydra.

> "This form of acceptance testing allows us to be clear and precise about what we want of our systems and to guide our development."

Thank you for exploring this practical approach to BDD style acceptance testing with Dave Farley.
