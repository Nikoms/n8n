---
title: How to sell a big refactor or rewrite to the business? - Ivett Ördög - NDC Oslo 2025
date: 2025-08-09
category: videos
tags: [refactoring, ndc]
---

![thumbnail](https://i.ytimg.com/vi/wdz90PQ2Ak4/maxresdefault.jpg)
[https://youtu.be/wdz90PQ2Ak4?si=4Gz3VnLq4olwP5r_](https://youtu.be/wdz90PQ2Ak4?si=4Gz3VnLq4olwP5r_)

## My thoughts

When to rewrite?

- Rewrite when it delivers new user value or addresses critical platform issues that prevent progress.
- Prefer incremental rewrites, gradually replacing old components while maintaining functionality, following the "strangling tree" pattern—slowly phasing out legacy code by building around and then replacing it.
- Avoid rewrites that halt feature delivery or create an all-or-nothing situation, as this risks losing market share to competitors.
- Sometimes creating a new product or competing internally (as with Adobe Flash or VS Code examples) is a successful rewrite strategy.

Our highest priority is to satisfy the customer through early and continuous delivery of valuable software.

## TLDR;
- Many developers are unhappy at work, mainly due to poor code quality.  
- Refactoring is essential, especially for AI-generated code.  
- Large rewrites are considered risky but can succeed under certain conditions.  
- Refactoring is small and local, while rewrites involve major re-architectures.  
- The Design Stina Hypothesis describes the trade-off between design investment and development speed.  
- Successful startups often have legacy code because they prioritize fast MVPs.  
- Technical debt often comes from neglect and should be addressed incrementally.  
- Rewrites often fail when approached as “all-or-nothing” without continuous business value.  
- Case studies show successful rewrites through incremental migration or new product development:  
  - Flash migration into a business-oriented product  
  - Gradual replacement of import and workflow systems  
  - Development of VS Code as a lean product for a new market  
  - Partial frontend transition for improved UX  
- Successful strategies: create internal competition or incrementally replace with customer value.  
- Rewrites should not be sold as rewrites, but as feature development.  
- AI assistance helps but does not replace the need for refactoring.  
- Agile principles such as continuous value delivery should guide rewrites.  
- Audience questions confirm that incremental value creation and competitive pressure foster success.  
- Motivation increases through measurable improvements in developer experience (e.g. Shopify).  
- Even without current competition, you should always assume it will come.  

---

## Content  

### Introduction: Why talk about rewrites and refactoring?  
I’m Evette, and I’m excited to talk today about a topic familiar to all developers: large rewrites and refactoring.  

> “Our highest priority is to satisfy the customer through early and continuous delivery of valuable software.” – Agile Manifesto  

This principle should guide us when thinking about how to evolve code and products.  

### The Code Quality Crisis: Why are so many developers unhappy?  
Studies such as those from Stack Overflow show that only about 20% of developers are satisfied, while about a third consider changing jobs. The main reason is poor code quality, which many find frustrating. Especially today, we see AI programs often generate hard-to-maintain code, making refactoring a crucial step to ensure quality.  

> “The more AI-generated code there is, the higher the share of bugs and redundancies.” – Various studies  

### Refactoring versus Rewrite: What’s the difference?  
- **Refactoring** means small, local improvements to code, often done quietly without big effort or announcements.  
- **Rewrite** is the comprehensive recreation of a system without intentional behavior changes, usually risky and costly.  

Rewrites are often viewed negatively—for example, Joski called the Netscape rewrite “the worst strategic mistake.” Yet many developers dream of rewrites, only to quickly learn how complex they are.  

### The Design Stina Hypothesis: Investment and Speed  
Martin Fowler presented the hypothesis that too little design reduces productivity, while too much design slows early progress. Startups prioritize fast MVPs over perfect design, which explains why older systems often have legacy code.  

> “Technical Debt is often really Technical Neglect.” – Kevlin Henney  

This means that much technical debt arises from failing to do the necessary maintenance.  

### Why are rewrites risky?  
Rewrites are risky because they’re often run as “all-or-nothing” projects, during which no real customer value is delivered. This leaves room for competitors to move faster, leading to project failure.  

### Case Studies: Successful rewrites despite risks  
- **Adobe Flash migration:** Instead of rewriting everything, they started with a minimal business product and expanded step by step.  
- **Monolithic workflow systems:** Problematic code was replaced gradually, despite errors and challenges.  
- **Daily data import:** For key customers, a 25-hour process was cut to 5 seconds, then rolled out incrementally.  
- **Platform with external APIs:** New APIs and microservices were introduced gradually alongside refactoring.  
- **VS Code:** Not a replacement for Visual Studio, but a new lean product for a new market, with major success.  
- **Limp Poker frontend:** Old and new frontend components ran in parallel to minimize risks.  

### Insights: Success factors for rewrites  
1. Rewrites must create value, not just refresh internal code.  
2. An incremental approach is crucial—“all-or-nothing” usually fails.  

> “Don’t sell rewrite projects as rewrites—sell features and improvements.”  

### Strategies for successful rewrites  
- **Create internal competition:** e.g., building new products for different markets (Flash, VS Code).  
- **Incremental replacement:** Stepwise replacement of problematic system parts (Strangler Fig Pattern).  

### Further considerations and pitfalls  
The combination of incremental development and customer focus maximizes chances of success. Tools and AI can accelerate progress but do not replace critical evaluation and refactoring.  

> “AI can make developers 30–40% faster, but code quality remains decisive.”  

### Conclusion  
Rewrites are not taboo if carried out strategically, customer-focused, and incrementally. Refactoring remains essential, especially in the era of AI-assisted programming.  

### Outlook and resources  
- Follow my YouTube channel for more technical insights.  
- Sign up for my coaching program to improve presentations and technical communication.  

Questions are always welcome—feel free to reach out!  
