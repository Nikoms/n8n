---
title: "TECHNICAL STORIES DON'T WORK (en)"
date: 2026-01-26T16:38:33.275+01:00
category: videos
tags: [software development,technical stories,agile,software quality,technical debt,user stories,essential complexity,accidental complexity,prioritization,continuous delivery]
excerpt: "Dave Farley discusses why separating software development into user stories and technical stories harms project success, advocating instead for developers to own technical decisions and integrate all work around user needs to maintain quality and speed."
---

![thumbnail](https://i.ytimg.com/vi/vSuJqMRG1WM/maxresdefault.jpg)
[https://youtu.be/vSuJqMRG1WM?si=VqJxJj-6Mho9g1je](https://youtu.be/vSuJqMRG1WM?si=VqJxJj-6Mho9g1je)

## My thoughts

Not specified (yet)

## TLDR;
- Software development work splits into solving user problems (essential complexity) and technical system work (accidental complexity).
- Technical stories are often deprioritized, harming system quality and maintainability.
- Separating user stories and technical stories for prioritization is a bad idea; it leads to poor quality software.
- Developers should take responsibility for technical decisions and complexities instead of deferring them.
- User stories represent user needs and should guide all development work.
- Technical tasks should be integrated with user stories or justified by clear user value.
- Continuous small improvements (Boy Scout rule) and prioritizing technical debt in terms understandable by business aides maintain system health.
- High quality and fast development are not in conflict; small incremental changes improve speed and quality simultaneously.
- Collaborative prioritization between technical and business roles is essential to balance value and system integrity.



## Content

### Understanding the Dual Nature of Software Development
Software development involves two distinct types of work: addressing the essential complexity—the actual user problems the software aims to solve—and handling the accidental complexity, which consists of the technical intricacies needed to make the system function effectively. Dave Farley clarifies that while technical work is vital, it is often overlooked or underprioritized when separated into so-called "technical stories."

> "There are clearly two important Dimensions to writing software: the problem that we're solving and the technicalities of solving it."

### The Pitfalls of Technical Stories
A common practice in Agile teams is to split work into user stories and technical stories. However, this division frequently results in technical tasks being pushed aside since prioritization usually favors user stories that bring visible user value. Dave argues this is detrimental.

> "If we split our stories into user stories and Technical stories then surely we must now prioritize the user stories... This results in low quality systems that are hard or almost impossible to maintain."

This approach relegates critical technical work, leading to brittle, complex codebases where even minor changes become risky and slow.

### Responsibility for Technical Complexity
Technical complexity should not be seen as a task for someone else. Developers, as experts, must take responsibility for managing accidental complexities and technical decision-making rather than deferring them to non-technical managers.

> "Technical stories are a cop-out—they mean the teams are either abdicating responsibility or non-qualified people are trying to exert control."

The best strategy is to eliminate the concept of separate technical stories and fold all work into user stories fueled by user needs, with the technical teams responsible for the technical decisions.

### Redefining User Stories and Prioritization
User stories are not mere development tasks; they represent user needs or goals. Development involves many steps addressing both essential and accidental complexities to realize these goals.

> "A user's story is meant to express a user need—a small increment in function that will be of some use to a user from their perspective."

By focusing on real user needs behind technical tasks, such as performance or resilience improvements, teams can prioritize work effectively alongside traditional features.

### Balancing Quality and Speed
Contrary to outdated beliefs, quality and speed are not trade-offs. Research cited by Dave from the DORA group reveals maintaining high quality enables faster progress and more focus on new features.

> "If you want to go fast you must have high quality and if you want high quality you need to move fast and make progress in small steps."

Continuous practices like test automation, refactoring, and maintaining code health should be standard work, not optional technical stories.

### Managing Technical Debt and Legacy Systems
For legacy codebases, it may be necessary to surface some technical stories temporarily to stabilize the system. However, the "Boy Scout rule"—leaving the code better after each commit—helps incrementally improve code health.

> "Aim to make the parts of the code where you are working a habitable space and keep a list of tidying tasks for those areas."

Prioritizing technical debt items using business metrics like decreased developer productivity can help make a compelling case for their importance to non-technical stakeholders.

### Conclusion
Dave Farley's insights caution against segregating and deprioritizing technical work in software development. Instead, he encourages developers to embrace full ownership of both user-facing and technical concerns. By integrating technical work into the user story framework and collaborating closely with business roles, teams can build maintainable, high-quality software while delivering real user value continuously.

> "Inside every technical story there's user value struggling to escape—we just need to think of a way of letting it out."

This holistic approach promotes balanced prioritization, sustainable development, and ultimately more successful software projects.




> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/862](https://github.com/Nikoms/n8n/tree/main/ongoing/862)