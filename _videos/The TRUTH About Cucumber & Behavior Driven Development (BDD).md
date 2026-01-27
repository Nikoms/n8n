---
title: "The TRUTH About Cucumber & Behavior Driven Development (BDD) (en)"
date: 2026-01-26T16:47:58.027+01:00
category: videos
tags: [BDD, Behavior Driven Development, TDD, Test Driven Development, Software Development, Communication, Software Testing, Cucumber, JBehave, Software Engineering, API Design]
excerpt: "An insightful discussion on BDD emphasizing communication to deliver business value, its origins from TDD, and the evolution of tools like Cucumber."
---

![thumbnail](https://i.ytimg.com/vi/YUkk2lGLxjA/maxresdefault.jpg)
[https://youtu.be/YUkk2lGLxjA?si=pSYbd3fJss65xCOD](https://youtu.be/YUkk2lGLxjA?si=pSYbd3fJss65xCOD)

## My thoughts

The video emphasizes that the real value of BDD lies in communication to get work done, not in the documentation format. It highlights that using plain text feature files, like those in Cucumber, adds unnecessary complexity and layers of indirection between the business discussion and the code. The creator of Cucumber himself points out that while plain text scenarios seem appealing, they are not always practical or the best choice for managing BDD effectively.

## TLDR;
- BDD (Behavior Driven Development) is primarily about communication to get work done, not just about learning or writing plain text files.
- The main purpose of BDD is to focus on the next important feature or behavior that needs to be implemented and to ensure completeness by handling important scenarios first.
- The origins of BDD stem from an effort to teach TDD (Test Driven Development) better without using the term "test" to avoid confusion.
- Writing specifications from the client or consumer perspective ("model client") helps design better APIs.
- The Given-When-Then format was developed to include the context missing in simpler acceptance criteria writing.
- Early BDD tools like JBehave and Cucumber evolved from attempts to create readable and executable specification tests, with debates around technical complexity and process efficiency.
- Plain text feature files and multiple layers of interpretation add indirection that some experienced practitioners find less efficient.





## Content

### The True Purpose of BDD: Communication and Getting Work Done

One of the key misunderstandings about Behavior Driven Development (BDD) is its core purpose. While many associate BDD with learning or writing clear, plain text scenarios, the actual goal is far more practical: it's about communication to get the job done. The speaker emphasizes that software development's primary aim is delivering business value, not learning for its own sake. Learning is a beneficial side effect but should not be mistaken for the primary objective.

He explains BDD as a method that helps teams focus on the "next most important thing" the system doesn’t do yet, prioritizing work according to what matters most. This pragmatic approach involves defining scenarios that cover important cases (e.g., handling scenarios for an ATM like money availability, insufficient funds, or account lockout) in order of importance. Once the critical scenarios are covered and implemented, anything else falls into future work or nice-to-haves.

> "The point of BDD is communication in order to get work done."

### Origins of BDD and Avoiding the Confusion Around Testing

BDD's roots trace back to efforts to teach Test Driven Development (TDD) more effectively. The initial problem was the word "test" itself, which caused confusion, especially between developers and testers. The speaker recounts convincing a team to adopt TDD principles without calling it "testing" by describing code in terms of what it should do, rather than what it should be tested for.

This approach focused on describing a "model client" perspective—writing code as if the perfect API existed for the client or consumer's needs. This mindset encourages designing APIs from the user perspective rather than from the service or server side, leading to clearer, more usable interfaces.

> "Write it as though the thing exists entirely for you."

### The Evolution of Given-When-Then and Scenario Writing

The speaker shares how the common Given-When-Then structure arose to handle missing context in earlier attempts to describe acceptance criteria. Instead of vague "I do this, this happens" descriptions, the structure incorporates context explicitly, providing clear, structured scenarios that aid understanding and testing.

Index cards were used to keep descriptions small and manageable, with examples of different outcomes on the card's back. This method linked business analysis practices to the technical need for precise, shared understanding.

> "We slid it all across a bit. And that's where the given when then columns came from given, you know the that I've got the correct credentials."

### Tooling: JBehave, Cucumber, and the Debate Around Plain Text Feature Files

In the pursuit of practical BDD tools, JBehave was an early Java framework attempting to implement these ideas but struggled to gain traction because it wasn't integrated with standard tools like JUnit. Later, Ruby-based implementations introduced domain-specific languages (DSLs) that allowed writing executable scenarios in code with given-when-then constructs.

Others sought to allow plain-text writing of scenarios parsed by regular expressions, leading to the creation of Cucumber. However, there were criticisms about the complexity and extra layers of parsing introduced, which added indirection between the feature files and the code.

The speaker recalls cautioning against reliance on plain text feature files authored by business analysts due to the risk that those scenarios might not be maintained or prioritised properly, and the processing layers could introduce technical and process overhead.

> "You've now got three and four levels of interaction before you get to the code."

### Final Thoughts

BDD's value, as conveyed by the speaker, lies in fostering shared understanding and seamless communication among stakeholders to deliver business goals effectively. While tooling and syntax are important, they should serve the communication purpose without creating unnecessary complexity. The essence is always about doing the next important thing well and ensuring clarity between development and business teams.





> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/903](https://github.com/Nikoms/n8n/tree/main/ongoing/903)