---
title: "Domain Driven Design with BDD (en)"
date: 2026-01-26T16:41:42.015+01:00
category: videos
tags: [BDD, behavior driven development, domain driven design, ubiquitous language, software development, acceptance testing, executable specifications, software testing, agile]
excerpt: "Dave Farley explains how BDD goes beyond tools and tests to unify development teams around a shared language, creating executable specs that focus on behavior and improve software alignment with business goals."
---

![thumbnail](https://i.ytimg.com/vi/Ju50D11EIoE/maxresdefault.jpg)
[https://youtu.be/Ju50D11EIoE?si=-MoVigtFyowFswXo](https://youtu.be/Ju50D11EIoE?si=-MoVigtFyowFswXo)

## My thoughts

Not specified (yet)

## TLDR;
- BDD (Behavior Driven Development) is more than just tools like Gherkin, Cucumber, or SpecFlow; it is a methodology that connects the whole development process.
- BDD promotes the use of a ubiquitous language, a shared problem domain language across business, development, and testing teams to improve communication and reduce misunderstandings.
- The practice focuses on describing system behavior from the perspective of users, emphasizing "what" the system should do rather than "how".
- BDD specifications are executable and durable, changing only when business goals change, enabling more flexible and maintainable testing.
- A layered model separates test cases, domain-specific language (DSL), protocol drivers, and the system under test, supporting reuse and adaptability to different test implementations.
- BDD helps build better aligned, more changeable software, and supports complex problem domains effectively.



## Content

### Understanding Behavior Driven Development (BDD) and Its Broader Implications
BDD is often mistakenly reduced to a few elements—like the Gherkin language or tools such as Cucumber and SpecFlow—or the idea of the "three amigos" discussing business ideas. However, Dave Farley argues that BDD's true power lies in how it connects different parts of the development process, acting as "the grease in the wheels" that enables great teams to do great work.

### The Role of Ubiquitous Language in BDD
At the heart of both domain-driven design and BDD is the concept of a ubiquitous language—a consistent language agreed upon by all team members to describe the problem domain. Dave references Eric Evans’s book *Domain Driven Design* to emphasize that our code should be executable models reflecting the problem domain, not technical jargon or implementation details. By using a definitive and unambiguous language, teams reduce misunderstandings, fostering accurate communication between business and technical stakeholders. This language becomes a foundation for writing specifications and implementing software with clarity and purpose.

As Dave puts it: "The idea is that over time we agree on the words that we're going to use... We want our ubiquitous language to be definitive, accurate, and ideally lacking in ambiguity."

### A Behavioral Focus: Writing Stories and Scenarios the BDD Way
BDD encourages a focus on behavior from the user or consumer perspective. This means writing user stories that define *what* the system should do—never *how*. For example, a good story might be "As a traveler, I'd like to book a room at my destination," without specifying UI details or implementation specifics.

Each story is complemented by examples or scenarios—acceptance criteria described succinctly in the ubiquitous language that demonstrate how the user benefits. These become executable specifications, confirming that the system fulfills the desired behavior.

Dave stresses that "If your user stories say things like add a button or make this text blue, you're doing it wrong."

### Executable Specifications and Loose Coupling
One of the key strengths of BDD is that these executable specifications are loosely coupled to the system implementation. The specification's validity depends on business goals, not technical details, enabling evolution without frequent rewrites of tests or scenarios.

Dave introduces a four-layer model supporting this:
- **Test cases**: Executable specifications written in ubiquitous language.
- **Domain-Specific Language (DSL)**: Defines the ubiquitous language, making it sharable and reusable.
- **Protocol drivers**: Translate DSL concepts into actual system interactions.
- **System under test**: The real running software.

This separation allows reuse and flexibility. For instance, whether booking a room via a web interface or a function call, only the protocol drivers change; the DSL and specifications remain intact. Dave explains, "I can't imagine a way of creating test cases that are more loosely coupled to the system."

### Practical Example: Booking a Room on Airbnb
Using a simple example, Dave illustrates creating a story for a traveler booking a room, writing executable specifications that remain agnostic of UI or system implementation. This clarity makes it easier to maintain and evolve the system while ensuring alignment with user goals.

### BDD for Complex Domains
Though the example is simple, Dave mentions he has applied this approach to highly complex fields such as financial trading, medical devices, and genetic analysis. BDD’s strength grows as problem domains increase in complexity, helping teams maintain clarity and ensure software correctness.

### Conclusion: Benefits of Behavioral Focus and Ubiquitous Language
BDD is a powerful methodology for bridging communication across roles, focusing on true user behavior, and enabling more maintainable and adaptable software development. By rooting software in the language of the business, it helps teams develop solutions that better meet real needs and handle change gracefully.

Dave Farley concludes: "The approach to BDD style acceptance testing... helps us structure, organize, and capture our ubiquitous language, improves communication, better focuses our development on the problem, and makes testing those systems an awful lot easier."




> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/871](https://github.com/Nikoms/n8n/tree/main/ongoing/871)