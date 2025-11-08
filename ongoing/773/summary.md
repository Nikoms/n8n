---
title: "Application Architecture for Real World Continuous Delivery  by  Christopher Batey (en)"
date: 2025-11-08T12:29:16.697+01:00
category: videos
tags: [continuous delivery, application architecture, devops, kubernetes, microservices, testing, observability, configuration management, deployment strategies, stateless applications]
excerpt: "This talk explores application architecture for continuous delivery, focusing on interfaces, disposability, stateless design, testing strategies, observability, configuration, and infrastructure decoupling to achieve fast, reliable, and secure deployments."
---

![thumbnail](https://i.ytimg.com/vi/mSO6x2QdBI8/maxresdefault.jpg?sqp=-oaymwEmCIAKENAF8quKqQMa8AEB-AH-CYAC0AWKAgwIABABGHIgSigjMA8=&rs=AOn4CLDqwDqv4k9LQb-omsqSBFcltg2yPw)
[https://youtu.be/mSO6x2QdBI8?si=5F1O9OoGPKmnNIVy](https://youtu.be/mSO6x2QdBI8?si=5F1O9OoGPKmnNIVy)

<!--- My thoughts -->

## Content

### Introduction to Continuous Delivery and Application Architecture
He introduces continuous delivery (CD) as the capability to deploy changes rapidly, securely, and reliably into production, focusing primarily on applications owned and developed by teams. He broadens the perspective on what constitutes changes, including data pipelines, infrastructure, and third-party products but confines today's focus on applications. Drawing from two decades of experience, he notes the importance of enabling frequent deployments with auditability and traceability.

### Defining Systems and Applications
A full system serves business needs and includes client applications, global load balancers, content delivery networks, and one or more applications developers build. The focal point is application architecture within this larger system — the public interfaces the application exposes, backing services, hosting methods (serverless, containers, VMs), and observability.

### Public Interfaces and Versioning
He stresses the importance of carefully defining public interfaces such as HTTP APIs, gRPC messages, or event streams. Internal backing services like databases and caches are not considered interfaces unless accessed directly by other services. Preventing accidental exposure of internal implementation details (e.g., direct database queries by other teams) is key. Successful continuous delivery requires these interfaces to be backward and forward compatible, with clear versioning and deprecation strategies to avoid coordinated releases.

### Disposability and Hosting Environment
Historically, applications like mainframes ran for years without restarts, but modern environments require disposability. Applications must support rolling deployments and autoscaling, meaning multiple versions run concurrently and nodes can be drained and replaced automatically. He highlights three crucial architectural needs:
1. Health checks: implement both liveness and readiness probes to ensure instances only serve requests when fully ready.
2. Graceful shutdown: handle termination signals (e.g., SIGTERM), stop accepting new requests, complete ongoing work, flush metrics, close connections, and exit cleanly without dropping requests.
3. Fast startup: ensure applications become ready quickly to maintain smooth rolling updates.

### Statelessness and Load Balancing
Being stateless means not storing session or user data on the instance itself, allowing any request to be routed to any instance without stickiness (session affinity). State must be externalized to caches or databases. He reviews common load balancing methods (round robin, heuristics, sticky sessions, weighted distributions for canaries) and explains why avoiding sticky sessions supports disposability and scalability.

### Delivery Unit Encapsulation
All code, tests (unit, functional, performance, synthetic), monitoring dashboards, alerts, and configuration must be encapsulated in a single repository—referred to as the Deployable Immutable Versioned Artifact (DIVA). This tight bundling guarantees coordinated deployments and simplifies continuous delivery pipelines. Tests should be versioned and promoted alongside application code.

### Testing Strategies for Continuous Delivery
The emphasis is on stubbed functional testing, which tests the application in isolation with real backing services but stubbed collaborators. Stubs can be primed to simulate failure scenarios (timeouts, errors) to verify the application's resilience features such as timeouts and circuit breakers. Testing graceful shutdown through simulated slow dependencies is possible via stubs. Tests must be loosely coupled and runnable within minutes to provide fast feedback.

### Observability Architecture
Observability components (metrics, logs, dashboards, alerts) are integral parts of application architecture. The application exposes logs via standard output and metrics on endpoints without coupling to any particular provider. Dashboards and alert definitions are checked into the repository and deployed along with the application. If enterprise providers lack API-driven configuration, self-hosted solutions can be deployed with the application and export key metrics upward. He categorizes metrics into technical, delivery, and business metrics, emphasizing the importance of business metrics for canary deployment decision-making.

### Configuration Management
He strongly recommends minimizing configuration, ideally eliminating unnecessary configurable options. Environment-specific configuration should be limited and versioned with the application. Sensitive data must be secured, preferably using workload identity or secrets management systems. He advocates for having a well-defined, small set of environments to avoid configuration drift and maintain confidence in promotion activities. Database schema is treated as code and versioned within the application repository with established migration tools (Flyway, Atlas).

### Designing for Reduced Blast Radius
He highlights considerations for high availability, especially in multi-region deployments. Questions to ask include support for concurrent multi-version deployments, whether user sessions can transition between versions seamlessly, and whether persistence mechanisms allow active-active scenarios. Misguided multi-region deployments can paradoxically reduce availability if dependencies on transactional databases span regions.

### Decoupling from Infrastructure
Independent application architecture shields developers from the variability and complexity of cloud and infrastructure changes. He provides case studies where applications deployed seamlessly across cloud providers or infrastructure upgrades due to adherence to principles like network communication to backing services, observability externalization, and avoiding hard coupling to infrastructure implementations. This decoupling supports infrastructure agility and developer productivity.

### Conclusions and Resources
He encourages reading the 12 Factor App methodology and original continuous delivery literature. He plans to release a tool for evaluating continuous delivery readiness of architectures. For further discussion, attendees are invited to connect with him on social platforms.
