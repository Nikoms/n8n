# How to Write Acceptance Tests
![thumbnail](https://i.ytimg.com/vi/JDD5EEJgpHU/maxresdefault.jpg)

<!--- My thoughts -->

## Content

### Introduction to Reliable Acceptance Testing
Acceptance tests are essential tools written from the perspective of an external user to validate what a system should do, avoiding any assumptions about how the system internally operates. As Dave Farley explains, "Acceptance tests are always written from the perspective of an external user of the system." However, maintaining these tests especially when the system evolves is challenging due to their fragility when small changes in the system trigger test failures.

### Understanding the Challenge of Fragility
Acceptance tests must reflect actual business behavior and are executed in production-like environments to simulate real scenarios. Yet, Farley highlights a common industry struggle: "These tests are genuinely complex... they can be very fragile if not written well." Even minor system changes can lead to failing tests, which is expected if behavior changes, but often failures happen from incidental issues, undermining trust and adding maintenance overhead.

### The Four-Layer Architecture for Acceptance Testing
To address fragility, Farley advocates for a clear separation of concerns through a four-layer structure:

1. **Test Cases:** These are written purely in the language of the problem domain, describing user stories or requirements such as buying a book with a credit card. Farley notes, "The test case is wholly focused on what the system does and says nothing about how the system should work."

2. **Domain-Specific Language (DSL):** This is an abstraction layer that implements the language of the problem domain and provides reusable methods to express behaviors required by the tests. The DSL handles parameter defaults, input parsing, and aligns test scripts to be repeatable and deterministic. "The DSL is optimized to allow us to write the test cases quickly and efficiently," Farley explains.

3. **Protocol Drivers:** Sitting below the DSL, protocol drivers translate domain-specific commands into actual interactions with the system under test. Whether it's driving a UI with Selenium, calling APIs, or simulating messages, the protocol driver understands system details, bridging the abstract instructions from the DSL to concrete operations. "Protocol drivers ... are the only part of the test infrastructure that know anything about how the system works," says Farley.

4. **System Under Test:** At the base lies the actual deployed system, hosted in a production-like test environment where the acceptance tests finally execute.

This four-layer approach results in test cases resilient to changes, since only the protocol drivers need updates when system internals evolve while test cases and DSL remain stable.

### Practical Example: Buying a Book
Farley illustrates the approach with a user story to buy a book. The test case states: go to the store, search for "Continuous Delivery," add the book to the shopping cart, checkout, pay with a credit card, and confirm ownership of the book. The DSL encapsulates these steps into reusable methods, and protocol drivers handle the real-world interaction details with the system, such as using Selenium to fill form fields or invoke API calls.

### Benefits of Separation of Concerns
This clear abstraction offers immense flexibility. Farley highlights, "You can write the test cases once and then reuse them in different scenarios through different interfaces." You could even imagine the protocol driver controlling a robot in a physical store without changing any test cases, underscoring the decoupling of behavior description from implementation.

### Implementation Styles and Tools
While Farley prefers internal DSLs in programming languages like Java, the principles apply equally to external DSLs such as Gherkin with Cucumber or SpecFlow. The key is to treat the DSL as an independent, reusable component rather than rewriting scenarios or feature steps each time. This fosters efficiency and maintainability.

### Conclusion and Resources
This architecture method has been applied across complex systems successfully and remains a robust approach for maintaining reliable acceptance tests amidst system change. Farley offers example code on GitHub and a free guide on acceptance testing to support practitioners interested in adopting this pattern.

As Farley summarizes, "I haven't yet found an environment where this wasn't a really great way of keeping those test cases focused on what the system needed to do rather than how it did it."

### Further Learning
For those interested in exploring this methodology further, Dave Farley provides a free acceptance testing guide and example implementations available through his GitHub repository linked in the video description.
