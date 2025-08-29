---
title: Lesson147 - The Fallacies of Versioning
date: 2025-08-22T17:46:14.566+02:00
category: videos
tags: [software architecture,distributed computing,versioning,microservices,APIs,contract versioning,software development,software engineering]
excerpt: "Mark Richards discusses the ninth fallacy of distributed computing: that versioning is simple. He explores the complexities of versioning microservices, API contracts, and shared libraries, illustrated with a trading app example, and emphasizes the technical and communication challenges involved."
---

![thumbnail](https://i.ytimg.com/vi/pVgCRKkuWzk/maxresdefault.jpg)

## My thoughts

Not specified (yet)

## TLDR;
- The 9th fallacy of distributed computing is that versioning is simple.
- Even basic microservices ecosystems involve multiple artifacts requiring versioning: API endpoints, contracts (e.g., JSON or XML schemas), services, and shared libraries.
- Managing versions across these artifacts can become extremely complex and confusing.
- Example given is a trading app posting buy orders for stock, where the representation of a stock (Apple) can vary (symbol, QSIP, SEDOL).
- Changing contract versions without proper versioning breaks clients relying on the old versions.
- Versioning the API endpoints alone creates duplication; a better approach is versioning at the contract level using request headers and vendor MIME types.
- Implementing versioning logic in services adds complexity, such as conditional handling of different contract versions.
- Supporting multiple versions eventually becomes unsustainable as older versions may be deprecated.
- Communication about version changes and deprecations across teams adds layers of complexity beyond technical challenges.
- Versioning requires careful governance, communication, and strategy—it's not as simple as it seems.



## Content

### Introduction to the Fallacies of Versioning
Mark Richards begins lesson 147 of Software Architecture Monday addressing a new fallacy in distributed computing: "versioning is simple." He references the original eight fallacies of distributed computing coined in the mid-90s by Peter Deutsch and others at Sun Microsystems, emphasizing that these timeless truths still hold. However, Mark and Neil Ford have introduced additional fallacies, with versioning complexity being their ninth.

### Complexity in Microservices Versioning
Mark explains that even in a straightforward microservices ecosystem, versioning is complicated. At minimum, four artifacts require versioning attention: the API Gateway endpoint, strict contracts (such as JSON or XML schemas), different service versions, and multiple shared libraries. These interconnected versions make understanding which versions an endpoint supports very challenging. He illustrates that endpoints may interact with multiple schema versions, services, and library versions, leading to a complex web of dependencies.

### Real-World Example: Stock Trading App
Mark presents a concrete example: a trading application where clients issue a POST request to buy stock. Apple stock can be identified using different schemes: symbol (AAPL), QSIP (037833100), or SEDOL (204-6251). The current JSON schema contract requires all three forms. He shows how clients using one representation work fine until the contract changes to switch from QSIP to SEDOL, breaking clients relying on the prior version.

### The Pitfalls of Versioning Endpoints Versus Contracts
One approach to handle change is to version the API endpoint itself (e.g., v1.0 using QSIP, v1.1 using SEDOL), but Mark argues this leads to duplicate endpoints for the same functionality. Instead, he prefers versioning at the contract level using the "Accept" header with vendor MIME types to specify contract versions. This approach allows multiple clients to coexist with their preferred contract versions without duplicating endpoints.

### Managing Versioning Logic Inside Services
While cleaner, implementing contract versioning demands that services parse headers to identify contract versions. This introduces conditional logic to handle differences per version (e.g., if version one, use QSIP; if version two, use SEDOL). Mark highlights that managing this branching behavior grows increasingly complex and raises the question of how long earlier versions are supported.

### Beyond Technical Challenges: Communication and Governance
Mark emphasizes that versioning complexity extends beyond code. Teams need strategies for communicating version changes, deprecations, and coordinating updates across APIs, contracts, services, and shared libraries. Such governance is challenging to create and maintain, underscoring why versioning is far from simple.

### Conclusion and Upcoming Topics
He concludes by reiterating the ninth fallacy: versioning is not easy. Mark teases an upcoming lesson on the tenth fallacy of distributed computing, encouraging listeners to stay tuned.

"A fallacy is something that we believe to be true but really is not. And that's what versioning is—not simple, even though we often believe it is."

This lesson provides valuable insight for architects, developers, and teams working with distributed systems, highlighting the subtle difficulties and communication challenges inherent in managing versioning effectively.




> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/609](https://github.com/Nikoms/n8n/tree/main/ongoing/609)
