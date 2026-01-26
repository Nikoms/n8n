---
title: "When Behaviour Driven Development Goes WRONG! (en)"
date: 2026-01-26T16:35:50.109+01:00
category: videos
tags: [BDD, Behavior-Driven Development, software development, software testing, automated testing, domain-driven design, executable specifications, software quality, collaboration, test automation]
excerpt: "Dave Farley explains how BDD enhances software development by focusing on clear behavior specifications, common pitfalls to avoid, and best practices for driving high-quality development."
---

![thumbnail](https://i.ytimg.com/vi/YAZr3LsCzn0/maxresdefault.jpg)
[https://youtu.be/YAZr3LsCzn0?si=PjMs0Snlro9xh-0G](https://youtu.be/YAZr3LsCzn0?si=PjMs0Snlro9xh-0G)

## My thoughts

Not specified (yet)

## TLDR;
- BDD (Behavior-Driven Development) centers around separating system specifications from implementation.
- It emphasizes describing what the system should do, not how it does it.
- Collaboration and using a domain-specific language to express requirements consistently are key.
- Common mistakes include confusing UI interactions with behavior, long and complex scenarios, lack of reuse in specifications, and scenario overload.
- BDD specifications should be concise, reusable, behavior-focused, and guide development without prescribing implementation.
- Effective BDD works best combined with other automated testing forms and focuses on user-desired behaviors.
- Dave Farley advocates a four-layer approach: test cases, DSL layer, protocol drivers, and system under test.
- Avoid using BDD scenarios to test every input; unit tests are better for detailed checks.
- BDD helps improve software quality when done correctly but requires avoiding common pitfalls.



## Content

### The Core Philosophy of BDD
Dave Farley starts by emphasizing that Behavior-Driven Development (BDD) is fundamentally about separating the specification of a system's behavior from its implementation. The goal is to describe what the system should do without prescribing how it accomplishes those behaviors. This approach fosters collaboration with domain experts and stakeholders to clearly articulate user needs. Using a consistent domain-specific language helps create clear, executable specifications that guide development efforts and reduce the risk of missing the mark.

> "Our job as software developers is not typing code, it's solving problems with software."

### Common Mistakes in BDD and Their Impact
Farley identifies five common pitfalls teams encounter with BDD:

1. **Confusing UI Interactions with Behavior:** Many BDD tests mistakenly specify user interface actions rather than the underlying user goals or system behaviors. For example, specifying entering a username and password focuses on an implementation detail rather than the broader behavior of user authorization. Instead, a better specification would be something like "Scott can access his accounts," which leaves room for different authentication methods. This focus allows the team to innovate in how behaviors are achieved.

2. **Long-Running, Complex Scenarios:** Some teams write scenarios that read more like tests with excessive detail, making them brittle and obscuring the core requirement. BDD scenarios should focus on one clear outcome, acting as executable specifications rather than exhaustive acceptance tests.

3. **Lack of Reuse in Scenarios:** Repeating steps and rewriting specifications without reuse wastes effort and indicates a lack of domain thinking. Reuse reflects deep understanding of the problem domain and avoids coding by remote control, where detailed instructions marginalize developers' problem-solving abilities.

4. **Scenario Overload:** Relying solely on BDD for all automated testing or having QA write scenarios separately often leads to covering every possible case unnecessarily. BDD specifications should prioritize defining the desired behaviors rather than exhaustive input coverage.

5. **Coding by Remote Control:** When senior or non-technical people specify every development step, it limits developers' ability to understand and solve problems effectively. This approach results in simple or overly complex implementations and loses important context about the problem being solved.

### Best Practices for Effective BDD
Farley's preferred approach involves several key practices:

- Write specifications that say nothing about the how, only the what.
- Develop a domain-specific language (DSL) to express user needs consistently.
- Use a four-layer structure in test code: test cases focused on system needs, a DSL layer defining language and utilities, protocol drivers that connect the language to the system, and the system under test.
- Combine BDD executable specifications with unit tests to cover detailed logic efficiently.
- Use BDD specifications to drive development from an external user's perspective, ideally in production-like test environments.

> "BDD makes the need to establish a language that describes the problems that we aim to fix more obvious."

### Conclusion
BDD is a powerful tool that can significantly enhance software quality and team alignment when applied correctly. By focusing on behavior rather than implementation, encouraging collaboration through a ubiquitous language, and avoiding common traps like scenario bloat and coding by remote control, teams can harness BDD to deliver software that truly meets user needs. However, success requires mindful application and integration with other testing strategies.

For further learning, Farley references talks and resources by John Ferguson Smart and tools like SpecFlow, encouraging continuous education on BDD best practices.




> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/856](https://github.com/Nikoms/n8n/tree/main/ongoing/856)