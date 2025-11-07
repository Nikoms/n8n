---
title: "This Company Tripled Developer Speed By Adopting THIS Practice (en)"
date: 2025-11-07T11:13:18.357+01:00
category: videos
tags: [software development, pair programming, code review, continuous delivery, testing, software quality, productivity, agile, TDD, ATDD, trunk-based development]
excerpt: "A case study on how a leading web company improved software delivery, reducing feature development time by over two-thirds and decreasing bugs through pair programming and process optimization."
---

![thumbnail](https://i.ytimg.com/vi/GVmjNk-gFU4/maxresdefault.jpg)
[https://youtu.be/GVmjNk-gFU4?si=F8Xjf9yis---pBiJ](https://youtu.be/GVmjNk-gFU4?si=F8Xjf9yis---pBiJ)

## My thoughts

Not specified (yet)

## TLDR;
- A well-known web-based company transitioned from a mini-waterfall process with long lead times to using pair programming for feature development.
- Initially, average development time per feature was 151 hours with pull request cycles taking 253 hours.
- Code reviews on large pull requests were ineffective, often yielding fewer comments as change size increased.
- 30% of features started to be developed with pair programming, allowing those features to skip code reviews.
- After 100 days using pair programming, average feature development time dropped from 151 to 44 hours, median from 44 to 22 hours.
- Bug counts decreased and software quality increased with pair programming.
- Pull request cycle time reduced from 253 to 130 hours by eliminating many queues and delays.
- Further improvements are being explored, including trunk-based development, TDD, and acceptance test-driven development.
- Pair programming is shown to yield better quality, fewer bugs, and faster delivery despite initial managerial concerns.
- Emphasizes running all tests faster rather than avoiding tests to reduce risk of bugs.
- Encouragement to try pair programming due to its proven benefits and positive impact on team culture.



## Content

### Introduction: Learning from Real-World Software Improvements
He discusses the value of understanding how successful organizations improve software development, especially when supported by data. A well-known web-based company shared their journey from a slow, waterfall-like process to faster, higher quality outputs.

> "It's always interesting to learn how other organizations approach software development, particularly when they're good at it, and even better when they have data and evidence to show how what they're doing really works."

### Initial Development Process and Challenges
The company's initial process resembled a mini waterfall with releases every couple of weeks managed by Jira and GitHub, using CircleCI and later GitHub Actions. Developers spent on average 151 hours per feature, submitting large pull requests averaging 36 changed files. Two developers reviewed these, followed by QA testing involving manual and automated tests chosen selectively.

The reliance on manual regression tests posed risks of missed bugs due to selective test runs. The entire pull request lifecycle averaged 253 hours with multiple queues causing delays. He critiques test avoidance methods, advocating for running all tests efficiently to reduce risk.

### Insights from Pull Request Review Analysis
Inspired by Dragon Stepanovich's analysis of over 40,000 pull requests, the company analyzed their own repositories and found a similar pattern: larger, more complex pull requests garnered fewer meaningful review comments. Automated tools like Code Rabbit mostly produced spam comments, adding noise rather than value.

> "The more complex the change, the less serious the review and the less value it added."

### Experimenting with Pair Programming
To address these challenges, the team trialed pair programming for at least 30% of features. This approach allowed pair-developed features to skip additional code reviews. Managers initially worried this would reduce throughput and increase bugs, but agreed to monitor closely.

He highlights common apprehensions around pair programming and describes it as an underused but highly effective practice.

### Results of the Pair Programming Experiment
After 100 days, development time per feature dropped dramatically from 151 to 44 hours on average, and median times fell from 44 to 22 hours, indicating maintained or improved productivity despite two developers pairing.

Bug rates decreased, and overall code quality improved, matching findings from academic studies that show paired code tends to be more reliable, readable, and simpler. The pull request cycle time also halved from 253 to 130 hours as many queues and delays were eliminated.

> "Their results were very good indeed... Pair programming is extremely effective as a practice, but is all too often overlooked by nearly everyone."

### Looking Forward: Further Improvements
The company plans to explore trunk-based development, test-driven development (TDD), and acceptance test-driven development (ATDD) to further reduce pull request lifecycle costs and increase quality and throughput.

### Conclusion: Encouraging Pair Programming Adoption
The experiment dispelled fears about pair programming reducing productivity or increasing bugs. Instead, it demonstrated faster feature delivery and better quality with fewer delays.

He encourages managers and developers to try pair programming, underscoring its repeated validation in research and practice.

> "Counterintuitive as it may seem, pair programming is a more productive, higher quality way of working and one that's repeatably backed up by academic research and by practical experience."

### Additional Notes on Testing Philosophy
He advocates for running comprehensive tests efficiently rather than skipping tests to reduce time, emphasizing that testing is best viewed as a way to falsify changes rather than prove them correct.

### Summary
This case study exemplifies how embracing modern practices like pair programming can greatly accelerate delivery timelines while improving software quality, challenging common preconceptions about software development efficiency and effectiveness.




> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/763](https://github.com/Nikoms/n8n/tree/main/ongoing/763)