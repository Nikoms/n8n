# How to Write Acceptance Tests
![thumbnail](https://i.ytimg.com/vi/JDD5EEJgpHU/maxresdefault.jpg)
[https://youtu.be/JDD5EEJgpHU?si=KlxjA9eN_PlU_1fD](https://youtu.be/JDD5EEJgpHU?si=KlxjA9eN_PlU_1fD)

<!--- My thoughts -->

## Content

### Introduction to Robust Acceptance Testing

Keeping acceptance tests running smoothly as systems evolve is challenging. In this episode, Dave Farley shares his preferred four-layer approach to writing acceptance tests that focus on what the system should do rather than how it works. "Acceptance tests are always written from the perspective of an external user of the system," he emphasizes, highlighting the importance of separating behavior from implementation.

### Understanding Acceptance Tests and Their Challenges

Acceptance tests evaluate the system in realistic scenarios from an external viewpoint, often called executable specifications. These tests aim to validate business-facing behaviors and support development. However, they are complex and can be fragile—small system changes often break tests. As Dave says, "If the tests are asserting behavior and the behavior of the system changes, fair enough, but even small changes can often cause breakages."

### The Four-Layer Approach

Dave proposes a four-layer architecture to organize tests and supporting infrastructure:

1. **Test Cases:** Written in the problem domain language, these describe what the system should do without technical details. For example, "buy a book by searching, adding to the cart, checking out, and paying."

2. **Domain-Specific Language (DSL):** Implements the test actions shared among cases, enabling reuse and determinism. The DSL simplifies writing test cases by providing optional parameters, defaults, and aliasing, making tests easier to write and maintain. "The DSL is aimed at making it easy to write test cases—that's really what we're trying to achieve."

3. **Protocol Drivers:** Translate high-level DSL commands into actual system interactions, such as UI automation with Selenium or API calls. This layer is the only part of the infrastructure that knows system details. "The protocol driver understands what it needs to do," Dave explains, helping bridge abstraction and execution.

4. **System Under Test:** The actual deployed system being tested in a production-like environment.

### Benefits of Separation of Concerns

This layered separation isolates test logic from system implementation details. It allows:

- Writing tests once and reusing them across different system interfaces or even physical environments.
- Encapsulating complicated setup within the DSL for precise control.

As Dave puts it, "You can write the test cases once and then reuse them in different scenarios through different interfaces... This separation of concerns is enormously useful."

### Implementing the Approach

Dave prefers internal DSLs embedded in programming languages (e.g., Java), gaining the power of programming tools while keeping tests abstract. Nonetheless, external DSLs like Gherkin or SpecFlow also fit well within this framework.

He advises treating the DSL as an independent entity, sharing and reusing it rather than rewriting scenarios repeatedly: "Use the DSL – it's a much more effective way of being able to write these things very quickly and very efficiently."

### Resources and Final Thoughts

Example code demonstrating these ideas is available on GitHub, and viewers can access Dave's free guide to acceptance testing.

In conclusion, this four-layer approach offers a powerful, flexible way to write acceptance tests that remain robust even as the system changes, allowing teams to focus on what really matters—the behavior and value of the system.

> "I haven't yet found an environment where this wasn't a really great way of keeping those test cases focused on what the system needed to do rather than how it did it."
