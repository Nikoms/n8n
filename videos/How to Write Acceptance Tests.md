# How to Write Acceptance Tests
![thumbnail](https://i.ytimg.com/vi/JDD5EEJgpHU/maxresdefault.jpg)

## My thoughts

The video explains that the key to creating robust acceptance tests lies in using a Domain Specific Language (DSL) that focuses on what the system should do rather than how it works. By organizing tests through a layered architecture—test cases in domain language, the DSL for expressing behaviors, protocol drivers that translate to system interactions, and the system under test itself—you can write tests that remain stable despite system changes. This approach allows the same test scenarios to be reused across different interfaces or test types, whether end-to-end or unit tests.

## TLDR;
- Acceptance tests focus on what the system should do, not how it works.
- Fragility in acceptance tests arises when small system changes break tests.
- A four-layer approach separates concerns to make tests robust and maintainable.
- The four layers are: Test Cases (problem domain language), DSL (domain-specific language), Protocol Drivers (interface translation), and System Under Test.
- DSL provides reusable, abstracted behaviors to write test cases efficiently.
- Protocol Drivers translate abstract actions into real system interactions, isolating system-specific details.
- This separation enables reuse of tests across different interfaces and scenarios.
- Internal DSLs (e.g., in Java) are preferred but external DSLs like Gherkin can also be used.
- Example used: Buying a book from Amazon demonstrating this layered, abstract testing approach.
- The method helps keep acceptance tests stable and focused despite system evolution.
- A free guide and GitHub examples are available to learn more.



## Content

### Acceptance Testing: Writing Robust, Maintainable Tests in a Changing System

Acceptance tests verify that a system behaves as expected from an external user's perspective, focusing solely on what the system should do rather than how it operates internally. However, keeping these tests running reliably while the system evolves is challenging due to test fragility when small changes cause failures. In this article, we explore a powerful four-layer approach that helps write acceptance tests that remain stable amid system changes.

### The Acceptance Testing Challenge

Acceptance tests evaluate a system end-to-end, simulating real user scenarios in production-like environments. They are often business-facing and support programming efforts, using executable specifications typically written before the code. Yet, despite their benefits, these tests tend to be complex and brittle. A small modification to the system's internal workings can make acceptance tests fail — not because the business behavior broke, but because the tests are tightly coupled to technical details.

Dave Farley highlights this core issue: acceptance tests must separate *what* the system should do from *how* it does it. This separation of concerns is essential to combating test fragility and maintaining reliable acceptance tests.

> "The only part of our test infrastructure that understands the details of how the system works should be isolated — everything else should focus on the problem domain."

### The Four-Layer Architecture for Acceptance Tests

Farley's preferred solution is a structured four-layer architecture:

1. **Test Cases (User-Level Specifications)**: Written in the language of the problem domain, these scenarios describe *what* the system must do, such as "buying a book from a store." They contain no technical details about system internals — only business-oriented steps.

2. **DSL (Domain-Specific Language)**: This layer implements an internal DSL designed to capture reusable behaviors and abstract the detailed interactions. It allows specification of optional parameters and default values, making test writing faster and more flexible.

3. **Protocol Drivers**: The protocol driver layer translates the abstract domain language into concrete interactions with the system under test. Depending on the system, this might involve driving user interfaces with tools like Selenium, calling APIs, or sending messages. It is the only layer with knowledge about how the system works internally.

4. **System Under Test**: The actual software system deployed in a production-like test environment, which is exercised by the tests.

This architecture cleanly separates concerns, isolating system knowledge in the protocol drivers and keeping test cases concise, readable, and stable.

### Practical Example: Buying a Book from Amazon

To illustrate, consider the acceptance test for purchasing a book on Amazon:
- The test case steps through actions like going to the store, searching for "Continuous Delivery," adding the book to the basket, checking out, and paying with a credit card.
- The DSL encodes these steps in reusable methods that can handle variations and optional arguments.
- The protocol driver uses Selenium (or other tools depending on the interface) to execute real UI interactions or API calls behind the scenes.

> "This test case would be equally true of any bookstore, even a real-world physical store, demonstrating the power of abstraction and reuse."

This approach ensures the tests remain valid even if Amazon's UI changes or the system evolves, as only the protocol driver needs updates.

### Benefits of the Four-Layer Approach

- **Maintainability**: Changes in system implementation only affect protocol drivers, not the test cases.
- **Reusability**: The same high-level test cases can operate across multiple interfaces or environments.
- **Clarity**: Test cases express business requirements clearly without technical noise.
- **Efficiency**: The DSL allows writing tests quickly with optional parameterization.

Farley notes he has successfully used this method in complex systems for years without encountering scenarios where it is ineffective.

### Tools and Implementation Notes

While Farley prefers internal DSLs implemented in programming languages like Java, external DSLs like Gherkin used in Cucumber or SpecFlow can also fit well into this architecture. The key is treating the DSL as a reusable, abstracted layer that encapsulates system behaviors separately from test definitions.

### Additional Resources

Farley provides a free guide to acceptance testing and shares example code on GitHub illustrating this four-layer design pattern (link in the video description). These resources offer practical help for adopting this approach in your own projects.

> "Don’t write your scenarios from scratch every time. Use the DSL as a shared, powerful tool to drive effective acceptance testing."

### Conclusion

Acceptance testing is a vital practice to verify business requirements end-to-end, but test fragility has hindered its wide success. By embracing a four-layer separation of concerns — clear test cases, a robust DSL, smart protocol drivers, and the system under test — teams can build resilient and maintainable acceptance tests that evolve gracefully alongside their systems.
