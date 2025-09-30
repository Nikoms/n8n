---
title: "Lesson 157 - Incorporating ADRs Into Existing Systems (en)"
date: 2025-09-30T12:46:46.580+02:00
category: videos
tags: [architecture decision records, ADRs, software architecture, legacy systems, architectural documentation, microservices, software engineering, architecture management]
excerpt: "Mark Richards explains how to incorporate Architecture Decision Records (ADRs) into existing software systems, helping architects document decisions and foster architectural clarity even in mature projects."
---

![thumbnail](https://i.ytimg.com/vi/7qsEgEfqDDk/maxresdefault.jpg)
[https://youtu.be/7qsEgEfqDDk?si=NiUh1mzjgD81u__e](https://youtu.be/7qsEgEfqDDk?si=NiUh1mzjgD81u__e)

<!--- My thoughts -->

## Content

### Introduction to Architecture Decision Records (ADRs)
Architecture Decision Records (ADRs) are concise text documents that capture important architectural choices made during a project's lifecycle. Mark Richards revisits ADRs in lesson 157 of Software Architecture Monday, focusing on the challenges and opportunities of integrating ADRs into existing software systems.

He reminds viewers that ADRs typically include sections such as a title, status (e.g., proposed, accepted, superseded), context explaining the reasoning, alternatives considered, the final decision, and the consequences including trade-offs. This structure provides a blueprint for comprehensively capturing architectural decisions.

As Mark emphasizes, ADRs are not restricted to new systems; they can and should be brought into established architectures to improve transparency and guide future changes. This lesson builds on his prior discussions about ADRs in earlier lessons (55 and 141) and architecture stories in lesson 106.

### Applying ADRs to Existing Systems
Mark addresses a common question among architects: is it worthwhile to start using ADRs in a mature system? His answer is a resounding yes. Despite decisions already being made—often without documentation or with personnel turnover—starting to create ADRs is valuable.

The approach involves reviewing the system to identify major decisions that lack clear rationale and documenting them. For example, Mark examines a student testing system used for standardized tests across schools, a system in place for about five years. This system contains multiple microservices such as sign-in service, fraud detection service, test taker service, auto grader, and various databases.

### Investigating Architectural Decisions: Questions to Ask
Mark encourages architects to question the current design and identify areas suitable for ADRs:
- Why does each microservice have its own separate database instead of using domain-based or a shared database?
- Why are test questions and answers stored in separate databases despite their close relationship?
- Why is fraud detection in a separate service instead of being integrated into the sign-in service?
- Why is the messaging queue sharded in a particular way, and why multiple queues exist?

Such questions open the door for documenting decisions and potentially revisiting them.

### The Three Core Steps to Incorporating ADRs
1. **Find the rationale:** Seek out the reasons behind each architectural choice, ideally talking to the decision makers. Often, this knowledge is lost due to staff changes, so the system’s history is reconstructed.
2. **Analyze and hypothesize:** If the rationale is unclear, propose logical reasons (e.g., security concerns might have led to separating questions and answers to restrict answer key access).
3. **Document and validate:** Write an ADR capturing the current understanding or alternative ideas, and invite feedback or challenges. New ADRs can justify architectural changes or preserve important legacy decisions.

### Benefits: Building a Brain Trust and Enabling Change
Creating ADRs for a legacy system forms a documented Brain Trust—an institutional memory of why things are done a certain way. This documentation supports better decision-making over time.

For example, Mark illustrates a recent architectural change: moving from inline auto grading to a post-grading model with a background service. Writing an ADR for this change records the trade-offs and implications, helping teams understand and justify modifications.

### Final Thoughts
Mark’s lesson underscores that ADRs are useful regardless of a system’s age. By carefully reviewing existing architectures, questioning decisions, seeking reasons, and systematically documenting them, software architects can transform legacy systems into maintainable, transparent, and evolve-ready platforms.

He invites viewers to follow future Software Architecture Monday lessons for more insights.

