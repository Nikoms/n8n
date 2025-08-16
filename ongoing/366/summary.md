---
title: Lesson 188 - Identifying Architectural Characteristics ()
date: 2025-08-16T12:15:30.517+02:00
category: videos
tags: []
excerpt: 
---

![thumbnail](https://i.ytimg.com/vi/j11MWnz2vYQ/maxresdefault.jpg)
[https://youtu.be/j11MWnz2vYQ?si=tJHx3m9DpcNhZYd3](https://youtu.be/j11MWnz2vYQ?si=tJHx3m9DpcNhZYd3)

<!--- My thoughts -->

## Content

### Identifying Critical Architectural Characteristics in Software Architecture

In lesson 188 of Software Architecture Monday, Mark Richards explores how software architects can identify which architectural characteristics are critical for their systems. Understanding these characteristics is a foundational skill for architects to better align system design with business needs.

### Sources of Architectural Characteristics

Architectural characteristics generally arise from three key sources:
1. **Business Domain:** The nature of the business problem often dictates crucial characteristics. For example, a stock trading system naturally demands low latency and high data integrity.
2. **Requirements:** These often specify quantitative demands like supporting 20,000 to 200,000 customers, reflecting elasticity in managing load.
3. **Listening to the Business:** Conversations with business stakeholders often reveal needs such as aggressive expansion, implying scalability requirements.

Richards emphasizes that a great deal can be discovered simply by carefully listening to business stakeholders and understanding their priorities.

> "Most architectural characteristics come from simply listening to the business."

### The Lost in Translation Problem

A common challenge architects face is the language gap between business stakeholders and technical teams. While business users talk in terms like "user satisfaction" and "time to market," architects think in terms of architectural qualities or system "ilities" (non-functional requirements).

Mark introduces the concept of using the architect's brain as a "translation engine" to interpret business language into meaningful architectural characteristics. This skill helps bridge communication gaps and ensures alignment.

> "One of the skills of a software architect in identifying important architectural characteristics is to use our brain as a translation engine."

### Translating Business Priorities into Architectural Characteristics

Mark provides two examples illustrating this translation:

**User Satisfaction:**
- Contrary to the simplistic notion of "user satisfactability," this priority unfolds into multiple characteristics including performance, agility, security, availability, fault tolerance, recoverability, and testability.
- No single characteristic alone guarantees satisfaction; it's a combination that supports the overall user experience.

**Time to Market:**
- Often described as "speed to market," this requires maximizing maintainability, testability, and deployability from an architectural perspective to quickly deliver features and fixes.

### Documenting and Collaborating on Architectural Characteristics

Mark revisits a tool introduced in lesson 112: the Architectural Characteristics Worksheet. This worksheet is available for download and facilitates recording the architect's hypotheses about critical attributes.

More importantly, it serves as a collaborative artifact for dialogue between architects and product teams. This interaction validates and refines the identified characteristics to ensure the architecture truly aligns with business priorities.

> "This worksheet is a vehicle for collaboration between architects and product teams, enabling better understanding and buy-in."

### Conclusion

Recognizing and articulating critical architectural characteristics is a crucial step in delivering systems that meet business expectations. Leveraging business insights, translating them effectively, and collaborating with stakeholders through tools like worksheets empowers architects to build better systems.

Mark encourages viewers to apply these insights as homework and stay tuned for further lessons in Software Architecture Monday.

