---
title: "Test Driven Development vs Behavior Driven Development (en)"
date: 2026-01-26T16:33:45.916+01:00
category: videos
tags: [Test Driven Development, Behavior Driven Development, Software Testing, Software Design, BDD, TDD, Software Quality, Continuous Delivery]
excerpt: "Dave Farley explains the differences and synergies between Test Driven Development and Behavior Driven Development, emphasizing how focusing on system behavior leads to better tests and higher quality code."
---

![thumbnail](https://i.ytimg.com/vi/Bq_oz7nCNUA/hqdefault.jpg?sqp=-oaymwEjCNACELwBSFryq4qpAxUIARUAAAAAGAElAADIQj0AgKJDeAE=&rs=AOn4CLBDb_scKXZO_ZM1-tZjA99pTfmngw)
[https://youtu.be/Bq_oz7nCNUA?si=Yi8SATeX_Dx4b5j0](https://youtu.be/Bq_oz7nCNUA?si=Yi8SATeX_Dx4b5j0)

<!--- My thoughts -->

## Content

### Understanding the Evolution from TDD to BDD
Dave Farley reflects on his experience with both Test Driven Development (TDD) and Behavior Driven Development (BDD), explaining why despite the effectiveness of TDD, there was a need to help develop BDD. He stresses that while TDD involves writing tests before code to direct development, BDD builds on this by focusing on the behavior of systems rather than just tests or tools. Farley highlights that BDD is often misunderstood as just tool-supported natural language testing (e.g., Gherkin, Cucumber), but it is fundamentally about specifying behavior across all testing levels.

### The Core Philosophy of Test Driven Development
TDD, named by Kent Beck in the late 1990s, was increasingly adopted in software development to interlace testing with design. Writing the tests after the code often results in systems that work but become difficult to evolve, due to tightly coupled tests to implementation details. Farley recounts experiences at ThoughtWorks, where emphasizing writing tests first prevented common project failures and ensured tests remained robust against code changes. He insists that TDD means the development is guided by tests written first, not tests added post-development.

### Why Behavior Driven Development Was Invented
Dan North and Chris Matz observed many teams misunderstood TDD and focused incorrectly on tests rather than behavior. They proposed BDD to reframe TDD as behavior-driven specifications rather than just testing. BDD introduced better vocabulary and structures like "Given, When, Then" to clearly describe system scenarios. This approach aids better communication with stakeholders and focuses development on system outcomes rather than technical testing tools alone.

### Tools and Misconceptions Around BDD
While tools like Cucumber and SpecFlow have popularized BDD by allowing specifications in near natural language, Farley points out that BDD should not be conflated with these tools. These tools have contributed tremendously but add complexity and are not ideal for fine-grained unit testing where BDD is equally applicable. He distinguishes acceptance testing as part of BDD’s broader strategy, which focuses on higher-level functional specifications.

### Tackling Common Criticisms of TDD
Common criticisms of TDD include tests being hard to write, tests restricting code changes, and poor code design outcomes. Farley counters these are problems arising from poor TDD practices rather than TDD itself. Using a behavioral approach to tests helps make tests easier to write, more robust to change, and encourages good design qualities.

### Examples Illustrating Behavioral Testing
Farley contrasts fragile, implementation-coupled tests with robust behavioral tests he wrote before code. These behavioral tests specify what the code does, not how, thus making them easier to write and maintain. He explains how his own projects’ tests focused on behavior helped organize thinking and incremental development.

### The Relationship Between TDD, BDD, and Code Quality
Good software design includes working functionality, modularity, cohesion, appropriate coupling, separation of concerns, and abstraction. Farley demonstrates how a BDD-inspired approach to TDD helped him achieve these design goals. The design he discusses is modular, cohesive, loosely coupled, and well abstracted, supporting multiple implementations without breaking dependent code.

### Conclusion: The Value of a Behavioral Perspective
Farley concludes that a behavioral approach to testing, whether via TDD or BDD, provides the best early feedback on design quality and improves both testing and code quality. He urges developers to focus on behavior-driven perspectives to maximize these benefits, affirming that this mindset shift is the most valuable insight from BDD.

---

This comprehensive view of TDD and BDD reveals how focusing on behavior rather than test mechanics can enhance software development practices significantly.
