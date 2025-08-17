---
title: Should Test-Driven Development (TDD) Be Used MORE In Software Engineering? (en)
date: 2025-08-17T10:50:39.929+02:00
category: videos
tags: [test-driven development, TDD, software design, refactoring, unit testing, approval testing, software engineering, software quality, programming best practices]
excerpt: A deep dive into why Test-Driven Development (TDD) should be more widely used: how it works, its design benefits, teaching challenges, importance of writing tests first, and how it improves software quality.
---

![thumbnail](https://i.ytimg.com/vi/6yb7jKpxTjM/maxresdefault.jpg)
[https://youtu.be/6yb7jKpxTjM?si=g5pg_4IkZik6vAqI](https://youtu.be/6yb7jKpxTjM?si=g5pg_4IkZik6vAqI)

<!--- My thoughts -->

## Content

### What is Test-Driven Development (TDD)?
Test-Driven Development is a software development approach where you start by writing a test that describes a small piece of behavior you want your software to have. Initially, this test will fail since the functionality doesn’t yet exist. You then write just enough code to pass that test. After the test passes, you refactor your code to improve its design without changing its behavior. This cycle continues, gradually building a robust suite of tests that serve as a regression safety net and drive good design.

As Emily Bash explains, “TDD involves first thinking about the problem, writing a test list, breaking the problem into small pieces, then writing a test one at a time, seeing it fail, then writing just enough code to make the test pass, followed by refactoring.” This process ensures that you are always working with either all tests passing or a single predictable failure, encouraging small, safe steps forward.

### How TDD Drives Better Design
A common misconception is that TDD inhibits good design. In reality, it encourages it. When you write a test first, you are consciously designing the external interface of your code from the perspective of a consumer. The implementation that follows is tactical and less focused on design initially. The refactoring stage that comes afterwards is when design improvements happen internally.

Emily emphasizes this dual focus: “At the point of writing a test, we are designing the interface. When implementing, we aim to get quick working code. Then in refactoring, we improve the internal design.” This cycle enforces better factored, testable, and modular code.

TDD naturally pressures developers to write code that is easier to test, which by design leads to higher quality through better modularity, abstraction, cohesion, and separation of concerns. As one speaker put it, “You have to be pretty stupid to write code that's hard to test, because starting with a test forces you to consider testability.”

### Skills and Challenges in Learning TDD
Learning the mechanics of TDD—writing tests first, making them pass, refactoring—can be achieved in a few weeks. However, the real challenge is in improving design skills, which is a lifelong process. TDD exposes deficiencies in design skills because testability requires good design.

Both speakers agreed that teaching design directly is difficult, but teaching TDD effectively teaches design implicitly. “I don't know a better way to teach design than teaching people TDD,” one said.

An anecdote involving a top-tier programmer, Martin Thompson, illustrated this well: even an expert programmer improved substantially after adopting TDD, gaining better design insights.

### The Importance of Writing Tests First
Writing tests *after* implementation loses most of TDD's value. Tests written post-implementation tend to tightly couple to the specifics of the code, making refactoring difficult and reducing design feedback.

“TDD is about listening to the feedback from the test while you're designing, not afterward,” said one of the speakers.

Thus, true TDD is defined by the practice of *writing the test first.*

### Approval Testing vs Canonical TDD
Approval testing, sometimes used in legacy code, captures the current behavior by generating output to compare against a baseline. Unlike the canonical TDD cycle, approval tests do not specify the expected assertion upfront; instead, the output is reviewed after running.

While useful for characterization, approval testing is not the same as TDD because it lacks the upfront specification and design-driving feedback.

### Practical Tips for Practicing TDD
To help those struggling with TDD, methodological advice includes writing out the test’s assertion in comments before writing any code. Start with what should be true after the code runs, then describe the action and the initial state, then implement backwards from there. This aids clarity and design thinking.

### Benefits of Wider Adoption of TDD
If TDD were more widely adopted, the software industry would have more flexible, maintainable, and business-aligned software. The discipline fosters better designs that facilitate easier and safer changes over time, which benefits everyone.

### Conclusion
Test-Driven Development is far more than "writing tests first." It is a powerful design methodology that aids clarity of purpose, drives better modular design through testability, and provides continuous, confident feedback during development. While it requires practice and a commitment to learning design principles, it pays dividends in software quality and maintainability. As one summary put it: “If more people used TDD, we’d get better designed software that's more flexible and cheaper to change, following business needs more closely. That’s what everyone wants.”
