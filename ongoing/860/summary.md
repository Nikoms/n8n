---
title: "Don’t Do E2E Testing! (en)"
date: 2026-01-26T16:38:13.118+01:00
category: videos
tags: [software testing, end-to-end testing, acceptance testing, contract testing, test automation, continuous delivery, software quality]
excerpt: "Dave Farley discusses why traditional end-to-end testing is problematic and promotes isolated, deterministic acceptance testing with simulated external systems, highlighting contract tests and real-world practices from LMAX."
---

![thumbnail](https://i.ytimg.com/vi/QFCHSEHgqFE/maxresdefault.jpg)
[https://youtu.be/QFCHSEHgqFE?si=C7JIAnX7fj6OBk2w](https://youtu.be/QFCHSEHgqFE?si=C7JIAnX7fj6OBk2w)

<!--- My thoughts -->

## Content

### Understanding the Pitfalls of Traditional End-to-End Testing
Dave Farley explains that traditional end-to-end testing, commonly associated with deploying changes to a staging environment that mirrors production, often leads to slow, expensive, and low-quality outcomes. The common practice involves deploying multiple teams' changes and testing everything manually or automatically in a large integrated system. Because this integration happens infrequently (weeks or months apart), with many changes at once, the tests become complex and fragile, making it hard to pinpoint issues or maintain quality. Additionally, teams lose control over variables and the ability to simulate problematic conditions. As Dave metaphorically puts it, testing such a system is like “eating spaghetti through a letterbox with chopsticks” — complex and controlled neither in predictability nor precision.

> “The bigger and more complex the system, the less thoroughly we can test it because we've lost control of the variables.”

### Principles of Good Testing: Isolation, Determinism, and Clarity
The key to effective testing, according to Dave, is test isolation. A good test is deterministic and atomic — it should precisely set up the system to a known state and yield the same results every time. Tests must be concise, focused on a single outcome, accurate in specifying system behavior, understandable by everyone involved in development, and durable against irrelevant system changes. Tests that probe into private states or rely heavily on external systems tend to be fragile and less maintainable.

> “A good test should be concise, accurate, understandable, and durable.”

### What Does End-to-End Testing Really Mean?
Dave advocates rethinking what end-to-end testing means. Instead of testing the entire complex system including external downstream/upstream systems, treat end-to-end tests as those that cover the entire software system you are building (the releasable unit) under production-like conditions. External systems should be faked or stubbed out with controlled inputs and outputs to maintain test determinism and speed. This allows thorough testing of deployment configuration, infrastructure changes, and new features without depending on real external services.

> “One of the important decisions to make is defining what constitutes our system and what we are responsible for testing.”

### Contract Testing: Validating Interfaces and Enhancing Collaboration
Testing interfaces rigorously via contract tests between your system and collaborating external systems strengthens reliability. Contract tests confirm that both ends adhere to expectations. Sharing these contracts with the teams responsible for external systems allows them to run your tests in their pipelines, catching breaking changes early. This approach, also called user contract testing, helps stabilize interactions across teams and emphasizes controlling interfaces where failures most likely propagate.

> “These sorts of places in code are more important than others because they propagate problems between teams.”

### Building a Sophisticated Test Infrastructure: The LMAX Example
Dave shares how at LMAX Financial Exchange, their acceptance test infrastructure simulated around 25-30 external systems with fakes and stubs. This approach allowed control over every interaction, injecting predefined responses to simulate different scenarios like account approval or rejection. It provided deterministic, fast-running tests often at microsecond speeds, much faster and more reliable than using real systems. Over five years, this approach prevented production incidents caused by integration failures. When upstream systems changed, failing contract tests alerted LMAX immediately, enabling quick adaptation.

> “We never had a production incident caused by failure of our interactions with these external systems.”

### Summary
Dave Farley’s exploration reveals that good end-to-end testing means thoroughly testing the software you control while faking or simulating external dependencies. Tests should be isolated, repeatable, understandable, and durable. Contract testing reinforces interface stability and collaboration between teams. Sophisticated, production-like test rigs enable fast, reliable acceptance testing that is far superior to traditional big-bang staging integration tests.

This modern approach empowers teams to reliably deliver releasable software continuously, avoiding the pitfalls of slow, brittle end-to-end tests that yield little control or insight.

