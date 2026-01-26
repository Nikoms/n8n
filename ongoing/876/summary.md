---
title: "Behavior Driven Development vs Unit Testing (en)"
date: 2026-01-26T16:42:02.250+01:00
category: videos
tags: [BDD, TDD, automated testing, regression testing, software development, specification by example, software quality]
excerpt: "Dave Farley explains how to balance BDD and unit testing to automate regression tests effectively, emphasizing clarity, appropriate tool use, and avoiding over-optimization."
---

![thumbnail](https://i.ytimg.com/vi/YL1q3tDgImM/maxresdefault.jpg)
[https://youtu.be/YL1q3tDgImM?si=mq7jUMSYNJNXrTB0](https://youtu.be/YL1q3tDgImM?si=mq7jUMSYNJNXrTB0)

<!--- My thoughts -->

## Content

### Introduction to Automating Regression Testing
Dave Farley emphasizes the importance of automating all regression testing to establish a more repeatable and reliable route to production. His preferred strategy is a combination of low-level Test-Driven Development (TDD) and user-focused executable specifications, also known as Behavior-Driven Development (BDD) scenarios.

### Understanding the Role of BDD and Unit Tests
Dave discusses how to decide when to use BDD specifications versus low-level unit tests. He explains that the choice depends on the nature of the question each test aims to answer. BDD scenarios are best for capturing user-facing requirements through executable specifications written in the language of the problem domain, focusing on what the system should do rather than how it does it. Conversely, unit tests serve as precise tools to verify specific lines of code, ensuring that the implementation behaves exactly as intended.

### The Tool Metaphor: Tape Measure and Ruler
He uses a metaphor of a tape measure and a ruler to clarify the roles of different tests. A tape measure is used for measuring longer distances quickly but less precisely, analogous to BDD tests measuring user level behaviors. A ruler, on the other hand, is more precise but less convenient for long distances, similar to unit tests. Mixing both tools addresses different measurement needs and provides a balance of coverage and precision.

### Avoiding Over-Optimization and Test Duplication Anxiety
Dave advises not to worry about duplication between BDD and unit tests. Instead of viewing tests as a cost to be minimized, he encourages seeing them as tools to build better software. The focus should be on clarity, understanding, and verifying that features work as intended. Over-optimizing tests for minimal duplication can lead to costly organizational coordination and coupling, which he warns against.

### Priorities in Testing
Dave stresses that the most important optimization is to make tests easy to understand rather than minimizing the number of tests or CPU cycles for execution. The greatest cost in software development lies in coordination and coupling among teams, not test redundancy.

### Writing Tests with a Relaxed Attitude
In conclusion, Dave recommends a relaxed attitude towards testing strategy. He suggests focusing on testing the feature at hand thoroughly and regularly, using BDD for acceptance-level validation and TDD/unit tests for precise verification. This approach leads to reliable software delivery without unnecessary stress over test duplication or perfect optimization.

### Quote to Remember
"Tests are tools that allow us to achieve a better outcome. We're not here to minimize the number of tests, but to build better software."

This episode provides valuable guidance for balancing different testing approaches, emphasizing that testing is about clarity and achieving goals, not simply reducing effort or duplication.
