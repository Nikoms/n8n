---
title: Should Test-Driven Development (TDD) Be Used MORE In Software Engineering?
date: 2025-08-16T01:07:04.609+02:00
category: videos
tags: [undefined]
---

![thumbnail](https://i.ytimg.com/vi/6yb7jKpxTjM/maxresdefault.jpg)
[https://youtu.be/6yb7jKpxTjM?si=HP5yYOtz64dUILtH](https://youtu.be/6yb7jKpxTjM?si=HP5yYOtz64dUILtH)

<!--- My thoughts -->

## Content

### Understanding Test-Driven Development (TDD)
Test-driven development (TDD) is a disciplined software engineering approach that involves breaking down a problem into small testable parts. As Martin Fowler summarizes and Emily elaborates, the TDD cycle is:
- Write a test based on the requirements and the external perspective of the code.
- Confirm the test fails, ensuring it fails for the right reasons.
- Write the minimal implementation code to pass the test.
- Refactor the code to improve internal design while ensuring tests still pass.
- Repeat these steps for each test case.

This iterative process keeps developers constantly aware of whether their code behaves as expected and guided by design feedback from the tests themselves.

> "At the point at which we're writing a test, we are consciously designing the external view of our code from the perspective of a consumer. Then refactoring drives our internal implementation design."

### The Impact of TDD on Software Design
One of the greatest strengths of TDD is its influence on software design quality. Because tests are written first as clients of the code, developers naturally build interfaces that are easier to use and understand. The subsequent implementation is tactical, followed by refactoring to create a clean internal structure.

Michael Feathers and others highlight the deep relationship between testability and good design. Code designed to be testable tends to be modular, cohesive, loosely coupled, and has clear separation of concerns.

> "You have to be pretty stupid to write code that's hard to test. So TDD forces you toward better design."

### Practical Challenges and Learning TDD
Despite its benefits, TDD can be tough to learn, primarily because it exposes deficiencies in design skills—a lifelong learning journey. Beginners often struggle to separate concerns sufficiently or find it difficult to visualize the interface before implementation.

A practical tip to ease the learning process is to write the test assertion first in comments, then outline the setup and trigger actions backward before actual coding begins. This helps clarify the goal and the test's design in advance.

> "If you're struggling with TDD, try writing the test backwards in comments, starting with the assertion."

### The Role of Test-First and Distinguishing TDD from Unit Testing
A crucial point emphasized is the necessity of writing tests first. Writing tests after implementation, even if they provide regression coverage, is not TDD as it loses design feedback and results in tightly coupled tests and code that become difficult to maintain.

> "Test first is test driven; test after is not. Writing tests after cuts you off from design feedback and halves the value of the tests."

### Approval Testing and Alternative TDD Approaches
Approval testing is recognized as a valuable tool, especially for legacy code through characterization testing. However, it diverges from canonical TDD because the assertions are discovered after implementation rather than defined upfront.

While approval tests can support an iterative feedback loop, they do not drive design in the way traditional TDD does.

> "Approval testing verifies that the solution hasn't changed rather than verifying you got the right design from the start."

### Broader Benefits of TDD to the Software Industry
Broad adoption of TDD would likely lead to better-designed, more flexible, and easier-to-maintain software. It would align software more closely with ever-changing business needs and reduce technical debt over time.

Teaching TDD is effectively teaching design, providing signals that prompt developers when to reconsider and improve their code's structure.

> "If TDD were used more widely, we'd get better-designed software that changes safely and quickly to meet business needs."

### Conclusion
Both Emily and her guest conclude strongly in favor of wider use of TDD, highlighting its role as a design tool, the confidence it affords developers through fast feedback cycles, and its impact on delivering higher-quality software. While acknowledging the learning curve and some nuances with alternative testing approaches, they assert that TDD is a powerful discipline every software engineer should embrace.
