---
title: "The Definition Of Insanity - Sam Newman - NDC London 2025 (en)"
date: 2025-09-04T23:19:36.319+02:00
category: videos
tags: [distributed systems,timeouts,retries,idempotency,resilience,robustness,networking,software engineering,microservices]
excerpt: "An in-depth discussion on foundational concepts of building resilient distributed systems: correctly tuning timeouts, implementing safe retries, and ensuring operations are idempotent to avoid errors and system failures.
---

![thumbnail](https://i.ytimg.com/vi/I6SvnCYRm50/maxresdefault.jpg)
[https://youtu.be/I6SvnCYRm50?si=vlVFRbmLuHjWSt59](https://youtu.be/I6SvnCYRm50?si=vlVFRbmLuHjWSt59)

## My thoughts

The video emphasizes the critical importance of being able to change timeouts without modifying code, allowing rapid adjustments in production when issues arise. This flexibility helps maintain system stability by tuning timeout thresholds based on real-time observations and load testing. It also prevents the need for costly redeployments just to tweak timeout settings, making it an essential best practice in building resilient distributed systems.

## TLDR;
- The talk focuses on improving resilience and robustness in distributed systems.
- Three core concepts are discussed: timeouts (knowing when to give up), retries (knowing when to try again), and idempotency (ensuring retries are safe).
- Distributed systems involve multiple computers communicating via networks, with inherent challenges like network delays and unreachable nodes.
- Timeouts prevent systems from waiting indefinitely, conserving computing resources, and meeting user expectations.
- Properly configured timeouts avoid resource exhaustion and system crashes; real-world case study with timeout misconfiguration causing system failure.
- Analyze normal system behavior with histograms to set appropriate timeout thresholds.
- Retries are useful due to transient failures, but must be limited to avoid overloading servers.
- Add jitter to retry delays to avoid retry storms and synchronized retry waves.
- Idempotency ensures repeated operations yield the same result, critical for safely retrying operations like payments.
- Implement idempotency using unique request IDs or server-side fingerprinting, each with advantages and caveats.
- Request IDs require client-server protocol changes, easiest for greenfield development.
- Server-side fingerprinting can retrofit legacy systems but has pitfalls like timestamp changes and repeated identical requests.
- When retrying an operation with the same request ID, the server should return the original response to maintain consistency.
- The common quote about insanity is misleading in distributed systems contexts; retrying the same operation can be essential.
- Use connection libraries like Polly or Resilience4J to implement these patterns effectively.
- Understanding and tuning timeouts, retries, and idempotency are foundational to building robust distributed systems.



## Content

### Introduction to Distributed Systems and Their Challenges
The speaker begins with a reflection on speaking experiences, highlighting a favorite venue, before diving into distributed systems. Distributed systems are defined as environments where two or more computers communicate over networks. These systems are complex due to two primary restrictions: information cannot be sent instantaneously, and sometimes nodes are unreachable. These realities introduce fundamental challenges that developers must embrace rather than expect to eliminate.

### Timeouts: Knowing When to Give Up
Timeouts are defined as thresholds that specify when a system should stop waiting for a response. Waiting indefinitely consumes computing resources and frustrates users. The speaker shares a compelling real-world example from 2008 involving a UK-based vehicle sales application. Misconfigured timeouts and connection pool settings led to system overload and failure, emphasizing the criticality of setting appropriate timeouts.

Effective management includes understanding normal response behavior via histograms rather than averages, as these show response time distributions and outliers (tail latencies). Tail latencies can severely affect user experience and become worse in microservices or parallel call scenarios due to their compounded effects.

### Retries: Knowing When to Try Again
Retries serve to handle transient failures, acknowledging that services may temporarily be unreachable. However, unlimited or poorly timed retries can overload servers. The speaker discusses retry strategies, including exponential backoff and the importance of adding jitter to spread retry attempts randomly, avoiding synchronized retry floods that exacerbate failures.

The talk references a case at Square where hundreds of immediate retries overwhelmed the system. Configurable retry limits and delays are essential, emphasizing that retry policies should be externalized from code for flexibility.

### Idempotency: Knowing When Retrying is Safe
Idempotent operations yield the same result despite multiple identical requests, a crucial property for distributed system reliability. The classic example involves payment processing: a network failure may cause uncertainty about whether a payment succeeded, risking duplicate payments if naive retries occur.

The speaker introduces two primary strategies for idempotency:
- **Request IDs:** Assign a unique identifier per operation so the server can detect duplicates and avoid repeating the operation.
- **Server-side Fingerprinting:** Generate hashes of the request to identify repeated attempts, useful when client modification is not feasible.

While request IDs are straightforward and preferred, they require protocol changes. Server-side fingerprinting has complexities, such as handling changing timestamps or identical repeated operations. The speaker highlights corner cases and advises caution.

Moreover, the server should return the same response when re-responding to a retried request, ensuring client consistency.

### Rethinking the 'Definition of Insanity' Quote
The talk also debunks the famous quote attributed to Einstein about insanity being doing the same thing repeatedly expecting different results, clarifying it was never said by him. In distributed systems, retrying (doing the same thing) can be rational and necessary until conditions change.

### Summary and Best Practices
- Timeouts need careful tuning based on real system behavior and user expectations.
- Retries are valuable but require limits, delays, and jitter to avoid cascading failures.
- Idempotency is the foundation of safe retry logic, implemented via request IDs or fingerprinting.
- Use mature libraries like Polly or Resilience4J to manage retries effectively.
- Monitor latency distributions with histograms to detect anomalies and establish sane timeout values.
- Communication and coordination between client and server teams improve idempotency implementations.

### Closing Remarks
The speaker invites attendees to access slides and upcoming book chapters covering these and related topics like rate limiting, backpressure, and circuit breaking.

This comprehensive talk equips distributed systems developers with foundational principles and practical strategies to build more robust, resilient applications in inherently unreliable networked environments.




> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/657](https://github.com/Nikoms/n8n/tree/main/ongoing/657)