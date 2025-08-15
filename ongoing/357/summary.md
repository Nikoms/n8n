---
title: Should Test-Driven Development (TDD) Be Used MORE In Software Engineering?
date: 2025-08-16T00:56:42.797+02:00
category: videos
tags: [undefined]
---

![thumbnail](https://i.ytimg.com/vi/6yb7jKpxTjM/maxresdefault.jpg)
[https://youtu.be/6yb7jKpxTjM?si=HP5yYOtz64dUILtH](https://youtu.be/6yb7jKpxTjM?si=HP5yYOtz64dUILtH)

<!--- My thoughts -->

## Content

### Understanding Test-Driven Development (TDD)
Test-driven development (TDD) is a disciplined approach to software development that starts with writing a list of test cases representing small pieces of the problem to be solved. Each test is written first and is expected to fail initially, providing a clear signal that the feature is yet to be implemented. After writing the failing test, developers add the minimum code necessary to pass that test, then refactor the code to improve design and maintainability while keeping all tests passing.

As Emily Bash explains, "TDD involves first thinking about the problem you're going to solve and writing a test list... you write the test, get it to fail, write just enough code to make that test pass, and then refactor."

The emphasis on writing the test first means developers design the external interface of the code from the perspective of its consumer, greatly influencing the quality and shape of the software's API before implementation details come into play.

### The Design Benefits of TDD
One of the key values of TDD is its positive influence on software design. Writing tests first forces developers to think about how the code will be used, inherently driving better design decisions. Michael Feathers highlights the deep relationship between testability and good design, where testable code tends to be better modularized, cohesive, and loosely coupled.

The process of refactoring after tests pass also focuses on improving internal implementation design. Emily adds, "It's this enormously powerful tool that drives us to design better code from the outside... it gives us a more stable platform for better implementation detail because we know it works."

The continuous feedback loop during TDD promotes safer, incremental changes that maintain a robust regression test suite, giving developers confidence in their changes and a clearer understanding of system behavior.

### Learning and Teaching TDD
While the core skills of TDD can be learned in a couple of weeks, mastering the design principles it fosters is a lifelong journey. Many struggle initially because they must rethink their approach to problem-solving by focusing first on specifying desired behavior rather than immediately implementing code.

Emily shares insight on teaching TDD, recommending developers write test cases and assertions as comments before coding, encouraging thoughtful design upfront: "Start with the assertion, then say what triggers the assertion, then say what state the system needs to be in. The test almost writes itself."

Highly skilled programmers, such as Martin Thompson, have reported becoming even better at programming through TDD, underscoring its value even among expert developers.

### Addressing Common Critiques and Misunderstandings
Some objections to TDD arise from misconceptions, such as the belief that TDD inhibits design or that tests must be written after the implementation. Contrary to these myths, writing tests first is crucial; it provides design feedback and prevents tight coupling between tests and implementation.

Writing tests after the fact may serve as regression tests but loses much of the value of TDD by tightly coupling tests to the code, making future changes risky and difficult.

Another common challenge is that developers sometimes feel they cannot write tests without fully understanding the implementation. Experienced practitioners advise focusing on the interface and desired behaviors rather than internal code structure, which helps separate specification from implementation.

### Approval Testing and Its Role
Approval testing is a technique often used for characterization of legacy code by capturing current behavior. While useful, it differs from canonical TDD because the assertion isn't defined upfront but discovered through output comparison. This makes it less a tool for driving design and more for verifying behavior after implementation.

Emily clarifies, "The approval test is always based on my solution... it doesn't seem like the same thing as TDD to me. It's not driving me to design in a certain way; it's just verifying I'm still getting what I wanted."

### Why TDD Should Be More Widely Used
The consensus is clear: Test-driven development should be adopted more broadly because it improves software design and quality, enabling faster adaptation to changing business needs. TDD teaches developers to write better, more maintainable code by ingraining the discipline of specifying behavior first and refactoring continuously.

Emily concludes, "If [TDD] were more widely used, we'd get better designed software that was more flexible, cheaper to change and update, and better aligned with business needs."

---

This in-depth discussion reveals that beyond the simple notion of "writing tests first," TDD is a powerful engineering discipline that shapes how we reason about and craft software. It promotes clear thinking about requirements, sharpens design skills, and builds robust, maintainable systems with strong feedback loops, making it a critical practice for modern software engineering.
