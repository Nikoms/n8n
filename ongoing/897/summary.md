---
title: "TDD or BDD When It Comes To Automated Testing? (en)"
date: 2026-01-26T16:47:08.032+01:00
category: videos
tags: [software testing, automated testing, test driven development, behavior driven development, continuous delivery, software quality, test automation strategy]
excerpt: "Dave Farley discusses practical approaches to automated testing, emphasizing the value of behavior driven development for legacy systems and test driven development for new projects, aiming to reduce manual regression testing and improve software delivery."
---

![thumbnail](https://i.ytimg.com/vi/Z9fGG1k6P40/maxresdefault.jpg)
[https://youtu.be/Z9fGG1k6P40?si=8JSbp6N8VPAoAZfR](https://youtu.be/Z9fGG1k6P40?si=8JSbp6N8VPAoAZfR)

<!--- My thoughts -->

## Content

### Preface
Dave Farley highlights a consensus among developers: most prefer working with well-automated tests. Even those reluctant to automate testing would want rapid feedback instead of waiting weeks or months due to manual regression testing delays. The crux of the matter is not the choice to automate tests, but how to do so effectively.

### Starting with Automated Testing: The Challenge
Dave notes that while he champions Test Driven Development (TDD) for its benefits in producing clean designs and isolated tests, retrofitting TDD onto legacy systems can be disruptive and complex due to existing code shape. This makes TDD best suited for new projects where it can be integrated from day one.

### Behavior Driven Development (BDD) as a Practical Entry Point
For existing codebases, Dave recommends Behavior Driven Development (also called acceptance test driven development) as a more accessible route. BDD focuses on automating the behaviors of the system in business language rather than technical implementation details, making it easier to retrofit and apply even to legacy or complex systems.

### Building a Domain-Specific Language (DSL) for Testing
A key step is developing a DSL tailored to describe system behaviors clearly and simply. This DSL should express what the system does rather than how it does it. Test cases scripted through this DSL map business scenarios and support fast, maintainable test writing.
Dave stresses:
> "...does my system express what it does in a way that I could replace the entire system with different technology without needing to change the tests?" 

Achieving this abstraction results in tests resilient to implementation changes, thus reducing breakages.

### Controlling Test Environments and Flaky Tests
Dave highlights that flaky tests often arise from uncontrolled test environment variables. Manual testers can compensate with subjective judgment, but automation demands more control for repeatability and reliability. Creating deterministic system states through controlled setups, version-controlled infrastructure, and test environments is essential.

### The Value Proposition and Practicality
He makes an optimistic but pragmatic claim:
> "Once you have the barebones of an acceptance testing DSL in place, the work of only a few days for most systems then for approximately the same amount of time it takes you to do the manual testing once or twice, you can replace manual testing with automated tests."

This transition yields much faster feedback cycles and greater stability and confidence in releases.

### Recommendations and Closing
- Start new projects with full continuous delivery, TDD, BDD, and deployment automation.
- For existing projects, begin with BDD and acceptance tests focused on releasability criteria.
- Grow your DSL steadily by learning from current release processes and focusing on user outcomes instead of UI clicks or implementation details.
- Use a layered architecture to maintain test abstraction.
- Incorporate infrastructure as code to automate system setup and maintain stable, repeatable test environments.

Dave encourages developers to learn TDD to improve individual skills but advises teams to adopt BDD first for quicker organizational impact. He also provides free tutorials on refactoring, TDD, and automated testing approaches for those interested.

The video reminds viewers that the goal is practical, good-enough automated testing that replaces the need for expensive manual regression testing, enabling quicker, more objective, and repeatable software releases.

---
Thank you for joining this detailed exploration from Dave Farley on automated testing strategies, practical tips, and mindset shifts essential for modern software delivery.
