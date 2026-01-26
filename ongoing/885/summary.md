---
title: "BDD Explained (Behaviour Driven Development) (en)"
date: 2026-01-26T16:42:43.742+01:00
category: videos
tags: [BDD, Behavior-Driven Development, Test Driven Development, TDD, Acceptance Testing, Ubiquitous Language, Domain-Driven Design, Continuous Delivery, Software Testing, Software Development]
excerpt: "Dave Farley explains the true origins and principles of Behavior-Driven Development (BDD) and how it helps build better software by focusing on specifying behavior, using a common language, and writing executable specifications."
---

![thumbnail](https://i.ytimg.com/vi/zYj70EsD7uI/maxresdefault.jpg)
[https://youtu.be/zYj70EsD7uI?si=_iFhOWn5w-zlpHpa](https://youtu.be/zYj70EsD7uI?si=_iFhOWn5w-zlpHpa)

<!--- My thoughts -->

## Content

### Introduction to Behavior-Driven Development (BDD)
Dave Farley explains that BDD has become synonymous with user-focused functional testing, but originally it was designed as a better way to teach and practice test-driven development (TDD). He recalls how in the early 2000s, working with ThoughtWorks and pioneering XP and TDD at scale, they noticed many developers misunderstood TDD by focusing too much on unit testing coverage and writing tests after coding. BDD was conceived to shift the focus to specifying behavior upfront, enhancing learning and value.

### The Origins and Philosophy of BDD
Chris Matz and Dan North were key figures in shaping BDD, emphasizing the importance of language. They preferred the term "specification" over "test" and "scenario" over "test case". Their Given-When-Then model structured tests as setup, action, and expected outcome, aiming to clarify intentions. Dan North introduced the technique of starting every test case with "should" to mentally prime developers to focus on desired behaviors.

### Ubiquitous Language and Domain-Driven Design
BDD is strongly influenced by the concept of ubiquitous language from Eric Evans's Domain-Driven Design. This means using one consistent language across business, development, and testing teams to avoid miscommunication. By using the same terms to describe requirements, designs, and tests, the software is more closely aligned to the problem domain, enhancing clarity and collaboration.

### Acceptance Testing and Executable Specifications
Acceptance testing and acceptance test-driven development are core components related to BDD. Automated acceptance tests act as executable specifications confirming business criteria are met. Capturing requirements as small, clear BDD scenarios from the external user's perspective helps ensure correct functionality before coding begins. This approach reinforces building the right software that meets user needs.

### Avoiding Implementation Details in BDD Scenarios
A key principle in BDD is to separate "what" the system does from "how" it does it. Dave highlights common mistakes where scenarios leak technical details, such as specifying button presses or UI navigation. Instead, scenarios should focus on behaviors, e.g., "when I add numbers" rather than "when I press add button." This makes specifications more durable, flexible, and focused on outcomes regardless of internal implementation changes.

### BDD Beyond High-Level Functional Tests
While BDD is often linked to user-focused functional testing, Dave stresses its value at all levels, including unit tests. All tests should express desired behavior from the perspective of an external user—whether that user is a person or another developer. Writing behavior-focused tests at the unit level ensures clarity and maintainability across the codebase.

### Practical Example
Dave provides an example in Python where a test starting with "should" verifies that starting a car's engine results in the engine running. This example captures behavior without describing how the engine or car actually works, illustrating behavioral separation. Such tests allow flexibility in implementation while ensuring correctness.

### Conclusion
BDD is an important methodology that tightly integrates with acceptance test-driven development and acceptance testing. Adopting a behavioral focus in all tests improves communication, software quality, and alignment with business goals. Whether writing large functional tests or small unit tests, emphasizing behavior over implementation offers substantial benefits.

Dave Farley's insights remind developers to think carefully about the language used in tests and the perspective from which they write them, always aiming to specify behavior clearly and unambiguously for better software delivery.
