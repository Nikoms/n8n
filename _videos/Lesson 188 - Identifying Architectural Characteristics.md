---
title: Lesson 188 - Identifying Architectural Characteristics (en)
date: 2025-08-16T12:19:03.580+02:00
category: videos
tags: [software architecture, architectural characteristics, business requirements, system qualities, nonfunctional requirements, scalability, performance, maintainability]
excerpt: Mark Richards discusses how to identify and translate critical architectural characteristics from business needs into system qualities essential for software architecture.
---

![thumbnail](https://i.ytimg.com/vi/j11MWnz2vYQ/maxresdefault.jpg)
[https://youtu.be/j11MWnz2vYQ?si=tJHx3m9DpcNhZYd3](https://youtu.be/j11MWnz2vYQ?si=tJHx3m9DpcNhZYd3)

## My thoughts

The video highlights the critical skill architects need to translate business stakeholder language into architectural characteristics like fault tolerance, availability, and performance. It emphasizes that a single business need often maps to multiple architecture requirements, illustrating this with examples such as user satisfaction translating into performance, security, and testability. This translation process helps ensure alignment between business goals and architectural decisions.
### Highlights

![2025-08-16T13:48:48.662+02:00-AQADscoxG5xPCFF9----Document that can help.jpg](https://github.com/Nikoms/n8n/blob/main/ongoing/369/photos/2025-08-16T13:48:48.662%2B02:00-AQADscoxG5xPCFF9----Document%20that%20can%20help.jpg)

## TLDR;
- Architectural characteristics come from three main sources, especially the business domain.
- Understanding the problem domain helps identify critical characteristics like performance, data integrity, and elasticity.
- Business language often differs from architectural language, requiring architects to translate business needs into architectural qualities.
- User satisfaction translates to multiple architectural characteristics including performance, agility, security, availability, fault tolerance, recoverability, and testability.
- Time to market corresponds architecturally to maintainability, testability, and deployability.
- Architects should document critical characteristics and collaborate with product teams using tools like an architectural characteristics worksheet.
- Validating and getting buy-in on these characteristics is an ongoing communication process between architects and stakeholders.



## Content

### Introduction to Identifying Critical Architectural Characteristics
In this lesson 188 of Software Architecture Monday, Mark Richards guides us through how to identify architectural characteristics that are critical or important to a particular system. He emphasizes that while architectural characteristics can be grouped into categories, determining which are necessary requires further insight. One key takeaway is that most architectural characteristics come from three primary sources, predominantly the business domain.

### Extracting Architectural Characteristics from the Business Domain
Mark illustrates this with an example from a stock trading system where low latency (high performance) and data integrity are essential due to the nature of the business. Additionally, certain requirements like supporting 20,000 to 200,000 concurrent users translate into architectural characteristics such as elasticity, which is the system’s ability to handle fluctuating loads. Through careful listening to the business language, architects can uncover characteristics such as scalability, especially when the business is expanding aggressively.

> "Most architectural characteristics come from simply listening to the business."

### Bridging the Language Gap: Business vs. Architecture
A common challenge architects face is the "Lost in Translation" problem. Business stakeholders and product owners speak in terms like "user satisfaction" and "time to market," whereas architects think in terms of architectural characteristics or system qualities (also called "ilities"). Therefore, a critical skill for architects is to act as a translation engine, converting business needs into architectural language that can be designed for and implemented.

### Translating Business Needs into Architectural Qualities
For example, when the business states "user satisfaction is paramount," it does not translate to a single architectural characteristic like "user satisfaction-ility." Instead, it spans multiple qualities:
- Performance
- Agility (ability to respond quickly to change)
- Security (to protect sensitive data)
- Availability and fault tolerance
- Recoverability
- Testability

These qualities together help ensure the system meets user satisfaction.

Similarly, "time to market" (how fast new features or fixes are released) translates to architectural emphases on:
- Maintainability
- Testability
- Deployability

Maximizing these three helps the organization release updates faster and stay competitive.

> "Our translation engine is one of our superpowers as architects."

### Documenting and Collaborating on Architectural Characteristics
Mark refers back to a worksheet he introduced in a previous episode (available in PowerPoint, Keynote, and PDF). This worksheet helps architects document their identified critical characteristics and provides a communication vehicle to collaborate with the product team. The worksheet fosters:
- Explanation of why certain characteristics were chosen
- Validation through feedback from product owners
- Mutual understanding and buy-in on architectural priorities

This iterative feedback ensures that architects' interpretations align with business needs and reduces misinterpretations.

### Conclusion
Lesson 188 continues the exploration of architectural characteristics emphasizing the practical approaches to identify crucial qualities for a system. Architects must bridge the gap between business goals and architectural requirements using active listening, translation, documentation, and collaboration.

Thank you for following along with Software Architecture Monday. Stay tuned for upcoming lessons that will further enhance your architectural understanding.




> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/369](https://github.com/Nikoms/n8n/tree/main/ongoing/369)