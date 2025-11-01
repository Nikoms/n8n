---
title: "TDD & DDD From the Ground Up Live Coding by Chris Simon (en)"
date: 2025-11-01T15:54:42.438+01:00
category: videos
tags: [test-driven development, domain-driven design, TDD, DDD, software architecture, concurrency, event storming, university registration system, software development practices, business domain modeling]
excerpt: "A comprehensive walkthrough of building a student registration system using test-driven development and domain-driven design, addressing concurrency issues through event storming and deferred room allocation."
---

![thumbnail](https://i.ytimg.com/vi/eWxOisRMcII/maxresdefault.jpg?sqp=-oaymwEmCIAKENAF8quKqQMa8AEB-AH-CYAC0AWKAgwIABABGHIgSigjMA8=&rs=AOn4CLABqSykSY7VyQjDJJUWXEm1wb3UhA)
[https://youtu.be/eWxOisRMcII?si=R69fJeuegIdQdvCn](https://youtu.be/eWxOisRMcII?si=R69fJeuegIdQdvCn)

## My thoughts

Not specified (yet)

## TLDR;
- Presentation about test-driven development (TDD) and domain-driven design (DDD).
- Starts with simple CRUD application for university student registration domain.
- Emphasizes writing small incremental tests and implementing code to pass them.
- Introduces ubiquitous language from domain experts in code naming.
- Demonstrates separating API contract classes from internal application classes.
- Uses vertical slice architecture grouping by domain concept.
- Identifies a race condition issue with concurrent enrollments exceeding room capacity.
- Instead of complex locking mechanisms, uses event storming to clarify business process.
- Discovers better domain model where room allocation happens after enrollments based on popularity.
- Develops a scheduling domain service to allocate courses to rooms optimally.
- Emphasizes encapsulating business logic within domain entities and services.
- Demonstrates refactoring and the value of TDD in maintaining clean code.
- Shares tooling ideas for maintaining a domain glossary for ubiquitous language.
- Concludes with code repository and tool access info.



## Content

### Introduction to Test-Driven Development and Domain-Driven Design
The speaker begins by introducing himself as an Australian recently relocated to France and discusses his passion for two software engineering practices: test-driven development (TDD) and domain-driven design (DDD). He highlights that the talk is unique at the conference because it's not about AI but about foundational software practices that empower technology teams to impact business success.

### Building a Student Registration System
He demonstrates building a university student registration system using live coding. The domain model includes students, courses, and rooms, with a key constraint being that room capacity must not be exceeded when enrolling students. The initial approach assumes a simple CRUD style, gradually transitioning towards domain-driven design as complexity grows.

### Test-Driven Development Fundamentals
The speaker explains the TDD cycle: write a failing test, implement the simplest code to pass the test, refactor, and repeat. He emphasizes small increments for tests and implementation. For instance, the first test verifies registering a student causes a 201 Created response.

### Ubiquitous Language and Code Design
A key DDD principle demonstrated is ubiquitous language - using the same terminology in code as domain experts use in the business. For example, instead of generic controller method names like 'create' or 'post', the code uses 'register new student' to mirror domain language. The speaker also stresses separating API contract classes from internal domain classes to protect consumers from breaking schema changes.

### Incremental Development and Refactoring
Progressing step-by-step, the code includes returning student details, assigning unique IDs, setting location headers, and validating inputs. Refactoring is performed regularly, such as introducing static factory methods to encapsulate object creation.

### Persistence and Testing Strategy
Initially, tests return hard-coded data to shape contracts. Later, JPA repositories are introduced for storing and retrieving entities. The speaker discusses grouping tests by domain concept, vertical slice architecture, and the choice to omit service layers for simplicity when the domain is straightforward.

### Handling Business Rules and Validation
Input validation is implemented, such as ensuring room IDs provided when creating courses exist. This logic is pushed progressively from controllers into domain models for encapsulation. For example, room existence checks and enrollment capacity checks move deeper into the domain layer.

### Encountering a Race Condition
When adding student enrollment business rules, a race condition emerges: concurrent enrollments can exceed room capacity, causing more students to enroll than chairs available. Common technical solutions like pessimistic or optimistic locking are mentioned but the speaker chooses to write failing concurrency tests to confirm the issue.

### Using Domain-Driven Design to Improve the Solution
Rather than complex concurrency controls, the speaker uses event storming - a collaborative workshop involving domain experts - to discover the actual business process and domain requirements. The discovery is that preallocating courses to rooms upfront is unrealistic; instead, course enrolments should happen freely first, then rooms allocated later based on actual popularity.

### Reevaluating and Refactoring the Domain Model
This insight leads to removing concurrency controls and changing the system to defer room allocation. The speaker discusses the importance of making tests go red before removal of code when deleting functionality to safely refactor.

### Developing a Scheduling Domain Service
A new domain service called a scheduler is introduced to allocate courses to rooms after enrollments. Testing at a lower level (unit testing the scheduler directly) enables more complex scenarios while keeping tests efficient and easier to set up.

The scheduling algorithm sorts courses by popularity and rooms by size to assign courses effectively.

### Encapsulation and Protecting Entity State
In the final refinements, setters on entities are made private, ensuring all changes happen through domain-specific methods to protect entity state. This reflects mature DDD practice of encapsulating logic within domain objects.

### Conclusion and Additional Resources
The speaker summarizes starting from small incremental TDD, discovering the race condition, applying DDD techniques to find a better business-aligned solution, the importance of ubiquitous language, and keeping code clean with continual refactoring.

He provides links to the GitHub repository to explore the code and a custom tool called Contextive to document business terminology for use in IDEs and browsers, helping bridge communication between development and business teams.

### Insightful Quote
"Daddy, next time I'm going to clean it up when it's just a little bit messy because cleaning up when it's really messy is just way too hard." - a metaphor connecting his daughter's tidying experience to the importance of continuous refactoring in TDD.




> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/759](https://github.com/Nikoms/n8n/tree/main/ongoing/759)