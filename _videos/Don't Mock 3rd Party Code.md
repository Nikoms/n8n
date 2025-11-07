---
title: "Don't Mock 3rd Party Code (en)"
date: 2025-11-07T11:17:50.399+01:00
category: videos
tags: [Test Driven Development,Mocking,Unit Testing,Software Design,TDD,Code Abstraction,Software Testing,Continuous Delivery,Software Engineering]
excerpt: "This article explains why mocking third-party libraries is generally a bad idea in test driven development and advocates for simple abstractions to improve code quality and testability."
---

![thumbnail](https://i.ytimg.com/vi/v6hP2MXoVrI/maxresdefault.jpg)
[https://youtu.be/v6hP2MXoVrI?si=-0TQE57vs4LmqIs2](https://youtu.be/v6hP2MXoVrI?si=-0TQE57vs4LmqIs2)

## My thoughts

Not specified (yet)

## TLDR;
- Mocking is a controversial but valuable tool in test driven development (TDD).
- Common misuse: mocking third-party code, which is risky and usually a mistake.
- Unit tests measure code behavior: return values, state changes, or interactions.
- Good tests measure code in controlled, repeatable ways to aid design and change.
- Over-mocking tightly couples tests to implementation, making refactoring difficult.
- Good design hides complexity and minimizes communication between code parts.
- Abstraction layers should be created over third-party code rather than directly mocking it.
- Testing should focus on what matters, not on internal implementation details.
- Acceptance tests are better for verifying interactions with complex external systems.
- Mocking third-party libraries leads to fragile, complicated tests; simple facades improve testability.
- Keep code easy to read, test, and change by avoiding mocking the generic third-party libraries directly.



## Content

### Understanding the Role of Mocking in Test Driven Development
Mocking is a widely used and often debated technique in test driven development (TDD). Some argue against its use, claiming it complicates tests and creates tight coupling between test code and the actual implementation. Yet, mocking remains an immensely valuable tool when used appropriately in TDD. This article explores mocking, emphasizing why mocking third-party code tends to be a bad idea.

### The Three Types of Unit Test Outcomes
Unit tests generally measure one of three outcomes: a simple return value, a change in state, or the interaction between parts of the system. Of these, interaction testing — the province of mocking — is the most complex and easiest to misuse. Good unit tests serve as precise measurements of code behavior, helping determine if the system behaves as expected under controlled conditions.

### Unit Tests as Measurements for Better Design
Unit tests function like measurements in carpentry, where precise, repeatable measurements ensure stronger, better-fitting constructions. Similarly, unit tests should create a predictable starting state for the system and verify its responses. This focus on measurement aims not only to verify correctness but also to support design that is modular, loosely coupled, and maintainable.

### Mocking and Test Doubles: Clarifying Terminology
A mock is a kind of test double used to verify that interactions with other parts of the system occur as expected. However, many mocking libraries provide broader features to create different kinds of test doubles, which can confuse terminology. Fundamentally, test doubles help measure system behavior or simplify testing by isolating parts of the code.

### The Relationship Between TDD and Design
TDD helps surface issues in design by encouraging code that is easy to test and refactor. Writing tests before code can prevent tight coupling of tests to implementation details, which often occurs if tests are written after the code. To ensure maintainability, tests should assert meaningful behavior, not fragile implementation details.

### Managing Complexity Through Good Design
Good design minimizes complexity by reducing unnecessary interactions between components, promoting clear abstractions, and hiding detail at boundaries. This approach aligns with design principles like "tell, don't ask," favoring clear commands over data inspection. Breaking code into small, cohesive, and testable units facilitates easier testing and maintenance.

### Problems with Mocking Third-Party Code
Directly mocking complex, general-purpose third-party libraries creates fragile tests tightly coupled to implementation details. This often results in complicated tests that are cumbersome to maintain. For example, attempts to mock web frameworks or databases require extensive simulation of library behavior, adding unnecessary complexity and reducing test clarity.

### The Benefits of Abstraction Over Third-Party Code
Rather than mocking third-party libraries directly, creating a simple, custom abstraction or facade can isolate your code from external dependencies. This abstraction encapsulates the interaction with external code, making your codebase clearer, easier to test, and more resilient to changes in third-party APIs. Tests on your abstraction are simpler, faster, and less tightly coupled, focusing on what your code needs to do rather than how third-party code works.

### When to Use Acceptance Tests Instead of Unit Tests
For system boundaries such as user interfaces or databases, acceptance tests that deploy the application in a production-like environment are more appropriate than detailed unit tests with mocks. Acceptance tests verify the whole system integration, ensuring real components work together as expected without overcomplicating unit tests.

### Conclusion
Mocking is a valuable technique in TDD but is best used carefully. Avoid mocking third-party libraries directly; instead, prefer layering simple abstractions that encapsulate external dependencies. This results in clearer, maintainable code and tests that are easier to write, understand, and evolve. Ultimately, the goal is to write code that is easy to read, test, and change, with well-measured and focused tests supporting continuous improvement and quality.





> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/769](https://github.com/Nikoms/n8n/tree/main/ongoing/769)