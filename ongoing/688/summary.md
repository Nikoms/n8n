---
title: "Exposing the not-so-secret practices of the cult of DDD - Chris Klug - NDC London 2025 (en)"
date: 2025-09-17T18:16:03.735+02:00
category: videos
tags: [Domain-Driven Design,DDD,value objects,ubiquitous language,architecture,onion architecture,CQRS,messaging,software design,software development,.NET,.NET Core,entity framework]
excerpt: "A deep dive into Domain-Driven Design concepts including ubiquitous language, value objects, domain events, architecture patterns, and pragmatic advice for applying DDD in real-world software projects."
---

![thumbnail](https://i.ytimg.com/vi/ESPnfFT6iD0/maxresdefault.jpg)
[https://youtu.be/ESPnfFT6iD0?si=CGb1sNiJCeZJD8-J](https://youtu.be/ESPnfFT6iD0?si=CGb1sNiJCeZJD8-J)

<!--- My thoughts -->

## Content

### Introduction to Domain-Driven Design (DDD) and Practicality
Chris Clug introduces the concept of Domain-Driven Design (DDD) and highlights how while DDD offers many valuable practices, it is not always practical for every developer or context, especially consultants. Consultants often lack the time to immerse deeply in a domain to learn ubiquitous language and domain nuances, which DDD requires for full implementation. He clarifies he is not critiquing DDD as bad but stresses it needs to fit the context. DDD works best in a product company where longer-term domain knowledge investment is feasible.

> "DDD is actually really good, I love a lot about DDD, but not everyone should do full DDD because it doesn’t fit everyone."

### Ubiquitous Language and Code Reflecting Domain Language
A core DDD concept is the ubiquitous language—the shared domain language used by developers and domain experts. Translating this into code means naming methods and variables exactly as the domain experts describe them. Chris contrasts a code snippet using terms like `calculateTotalCost` versus a version using the exact domain language like `calculateCostBasedOnClientDiscount` which is more understandable to domain experts.

> "...our code ends up looking something like this... if we show this to a domain expert, they can confirm if it reflects their language and meaning."

### Tactical Patterns: Value Objects
Chris discusses tactical patterns from DDD such as value objects, which aggregate closely related properties (like first name, last name, and age into a single immutable `PersonalDetails` record). These objects provide value equality, immutability, and self-validation, making them robust and simplifying domain models. Value objects ensure that invalid domain states cannot be created.

> "Value objects have value equality, immutability, and they are self-validating." 

He provides examples using C# 9+ record types with validation in constructors, immutable properties with `init`, and rich methods like color mixing for a color value object.

### Entities and Identifiers
DDD distinguishes entities, which are defined by their identity and change over time, from value objects. Chris points out common pitfalls like overusing database IDs as entity identifiers versus using natural domain identifiers (e.g. Swedish personal number for users). He stresses hiding database IDs in the domain model to avoid misuse by developers, while allowing EF Core to use private fields for persistence.

> "...the natural identifier for a Swedish person is the personal number, not the database ID."

### Repositories and Intent-Revealing Methods
Customizing repository interfaces by removing generic suffixes (`IUserRepository`) and adding intent-revealing method names (`UsersLivingIn(city)`) makes domain code more readable and expressive, resembling natural language.

> "Your code becomes like reading a book."

### Architecture: Layered and Onion/Ports & Adapters
Chris explains architectural patterns in DDD, including the relaxed layered architecture (presentation, application, domain, infrastructure) and ports & adapters (onion) architecture focusing on dependency direction inward to domain.
Messaging complicates layering because infrastructure messages must reach application/domain layers. The solution involves placing infrastructure under presentation and dependencies going inward through abstractions.

### Breaking Down Big Domains: Subdomains and Bounded Contexts
Breaking large domains into smaller subdomains (core, supporting, generic) and bounded contexts allows teams to focus on manageable parts. Bounded contexts correspond to independently evolving model parts with their own ubiquitous languages.

> "Defining subdomains and bounded contexts is really complicated and you will fail at it at first... but it's crucial for managing complexity."

### Anti-Corruption Layers
When integrating with other domains or legacy models, anti-corruption layers isolate and translate between different domain models to avoid unwanted coupling and complexity leakage.

### Messaging and Domain Events
DDD embraces asynchronous communication through domain events such as `AccountCreated` or `OrderCompleted`. These events enable decoupled extensions (sending welcome emails, triggering bonuses) adding flexibility.

Chris points out challenges in ensuring consistency between domain state and event publishing, offering the outbox pattern as the practical solution. This stores events in the database within transactions and publishes them reliably, accepting that messaging is generally "at least once" delivery.

### CQRS and Developer Pragmatism
The Command Query Responsibility Segregation (CQRS) pattern fits naturally with DDD for separating writes and reads. Chris discusses pragmatic approaches, including sharing a single database for simplicity and the acceptable trade-offs in duplicating some read code to avoid excessive complexity.

### Final Thoughts
Chris concludes by emphasizing that the highest achievement in DDD is producing domain code that developers not only understand what it does but also why it does it, aligning with domain experts' shared language.

> "The goal is not only can a developer understand what the code does, but also why it does what it does, and can relate the ongoing communication with the domain experts."

### Summary
This talk offers a practical perspective on applying DDD patterns without full dogmatism. It stresses clarity, code aligned with domain language, useful architectural patterns, pragmatic compromises, and the importance of ongoing domain collaboration. Chris's experiences provide actionable insights for developers and consultants navigating complex domains in the Microsoft .NET ecosystem.
