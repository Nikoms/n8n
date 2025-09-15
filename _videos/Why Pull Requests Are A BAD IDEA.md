---
title: "Why Pull Requests Are A BAD IDEA (en)"
date: 2025-09-15T11:13:31.320+02:00
category: videos
tags: [software development, continuous integration, pull requests, code review, pair programming, continuous delivery, devops, software quality]
excerpt: "Dave Farley discusses the challenges of software development, emphasizing continuous integration principles, the inefficiencies of pull requests, and advocating pair programming as a superior approach for fast, high-quality code review.
---

![thumbnail](https://i.ytimg.com/vi/ASOSEiJCyEM/maxresdefault.jpg)
[https://youtu.be/ASOSEiJCyEM?si=639d9l8F0THk5jmC](https://youtu.be/ASOSEiJCyEM?si=639d9l8F0THk5jmC)

## My thoughts

The video explains that while code reviews are important, pull requests often slow down the feedback loop essential for effective continuous integration and continuous delivery. Instead, it advocates for pair programming as an integrated, real-time code review that maintains fast, high-quality feedback without the delays caused by asynchronous pull requests. This approach supports the data-backed need for frequent integration and avoids the inefficiencies and frustrations commonly associated with pull request reviews. https://www.researchgate.net/publication/27295641_The_Case_for_Collaborative_Programming

## TLDR;
- Software is complicated and requires cautious, careful development.
- Continuous Integration (CI) with trunk-based development improves quality and speed based on large-scale data.
- Pull requests often hinder fast feedback necessary for effective CI.
- Code reviews are important but pull requests slow down the process due to waiting times and asynchronous communication.
- Pair programming integrates code review into the development process, providing fast, high-quality feedback.
- Pair programming improves productivity and reduces defects despite common misconceptions.
- Teams should experiment with pair programming for a short period to evaluate its benefits.



## Content

### Software Complexity and the Importance of Caution
Dave Farley begins by emphasizing that software is inherently complicated, requiring more care rather than rushing through the development process. He suggests that the common haste in software practices is akin to "running with scissors," advocating for greater caution.

### The Role and Evidence of Continuous Integration
He highlights the concept of Continuous Integration (CI) as a critical practice where changes are integrated and tested frequently alongside others'. Farley references the State of DevOps report from the DORA group at Google, citing robust data from tens of thousands of respondents demonstrating that teams practicing daily CI produce higher quality software faster and with better stability. He stresses that contrary opinions must bring comparable evidence to challenge these findings.

### Critique of Pull Requests and Code Reviews
While affirming the importance of code reviews, Farley critiques pull requests as a common barrier to achieving effective CI. Pull requests introduce delays in feedback loops due to asynchronous reviews and waiting times, often extending from minutes to days or weeks. This delay conflicts with the core requirement of CI: fast, multiple-time-per-day feedback.

He explains that pull requests originally served as gatekeeping tools in open-source projects where not everyone has commit access. However, this model is inefficient for collaborative team environments where trust among teammates should enable direct, fast code integration.

### The Problems with Pull Request-Driven Workflows
Pull requests often suffer from slow, one-way communication, lacking real-time discussion that could clarify intentions and teach improvements. Consequently, they create indeterminate states of changes that slow down the release pipeline, conflicting with continuous delivery goals.

### Solutions: Pair Programming as Integrated Code Review
Farley advocates for pair programming, where two developers work together simultaneously, providing immediate code review and feedback. This approach removes the bottleneck of asynchronous pull requests and speeds up error detection and resolution.

He acknowledges that pair programming is sometimes disliked due to perceived inefficiency or discomfort but presents evidence that pairs work nearly twice as fast and with fewer defects than solo developers. Furthermore, many people prefer pair programming once they experience it.

### Encouragement to Try Pair Programming
To overcome resistance, Farley suggests that teams try pair programming for a couple of weeks and then review the experience collectively. This trial can help dispel misconceptions and reveal the productivity and quality benefits of pairing.

### Final Thoughts
Overall, Farley stresses that the data-backed benefits of frequent integration, fast feedback, and collaborative review outweigh the challenges posed by traditional pull request workflows. Embracing pair programming and rethinking code review processes are practical steps toward building better software faster.





> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/680](https://github.com/Nikoms/n8n/tree/main/ongoing/680)