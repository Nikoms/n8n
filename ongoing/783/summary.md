---
title: "Technical Neglect - Kevlin Henney - NDC London 2024 (en)"
date: 2025-11-13T20:10:55.874+01:00
category: videos
tags: [technical debt, software maintenance, legacy code, software architecture, technical neglect, software development, metaphors in software, AI in software development, software products, software quality]
excerpt: "Kevin Henny explores the distinction between technical neglect and technical debt, highlighting how unmanaged neglect leads to costly legacy burdens. He advocates for clear metaphors, continuous maintenance, and awareness to better manage software lifecycle complexity."
---

![thumbnail](https://i.ytimg.com/vi/9iLxR1h2208/maxresdefault.jpg)
[https://youtu.be/9iLxR1h2208](https://youtu.be/9iLxR1h2208)

<!--- My thoughts -->

## Content

### Understanding Technical Neglect and Its Impact on Software Development
Kevin Henny opens his talk by introducing the concept of technical neglect, a term many are familiar with in practice yet have not formally named. He stresses the importance of naming in communication and understanding complex problems, particularly in software development architectures older than five years. He explains that software, unlike physical objects, is intangible, making it difficult for humans to grasp issues fully since we naturally understand physical phenomena better. Technical neglect is framed as the subtle absence of care or attention, which is much harder to identify and manage compared to explicit problems.

### The Distinction Between Technical Debt and Neglect
Henny challenges the common attribution of problems to technical debt, clarifying that technical debt is often an effect, not a cause. He explains that not all technical debt is inherently bad—it's a tradeoff, a deliberate borrowing of future time to accelerate present development, much like financial debt. The concern lies with unmanaged technical debt that continuously frustrates progress. The metaphor of a leaky boat aptly illustrates this: developers often focus on bailing water (fixing symptoms) rather than stopping the leak (addressing root causes like neglect).

### Software Degradation and the Nature of Change
Drawing on a 1980 paper by Mya Layman, Henny highlights that software complexity and structural degradation naturally increase over time as systems evolve—despite best practices. Developers tend to focus narrowly, ignoring broader context, leading to inadvertent structural damage. He draws parallels to everyday life where physical maintenance is expected and unavoidable (e.g., cleaning dishes), a mindset often missing from software development where maintenance is misunderstood or undervalued.

### The Power and Pitfalls of Metaphors in Software
Metaphors help explain abstract software concepts by mapping them onto familiar physical experiences. Henny emphasizes that a good metaphor should provide useful correspondences, minimize conflicts, and be familiar to its audience. Terms like "software architecture" or "legacy" are metaphors borrowing from real-world concepts to help reason about intangible systems. However, imperfect metaphors and overuse can cause confusion or misdirection, such as equating technical debt fully with financial debt.

### Legacy Code: Complex, Varied, and Costly
"Legacy" typically has positive meanings but is used negatively in software to denote outdated systems that are difficult to replace and maintain. Henny discusses various interpretations of legacy code, including code that "makes more design decisions than the team," reflecting a loss of control. He cites studies showing that legacy systems constitute around 31% of organizational technology but consume up to 80% of IT budgets for maintenance, severely dragging productivity and growth. He warns that focusing only on new development neglects the underlying legacy burden.

### Challenges with AI and Automated Refactoring
Kevin reviews recent research showing AI-generated code often has low quality and requires extensive fact-checking and corrections. Out-of-the-box large language models fail to reliably improve code without human oversight. He notes that while AI has potential, current practices risk automated production of legacy code, shifting developer roles more towards debugging and repair. The real resolution is not a tool solution but a heightened skill and process understanding around these technologies.

### Rethinking Maintenance and Software Products
Henny critiques common misconceptions labeling software work as "projects" with finite ends rather than ongoing "products." He clarifies that maintenance is not just bug fixes but includes continuous technical work integrated into product lifecycles. This requires recognizing implicit costs and consequences as part of software ownership, rather than viewing development as discrete delivery phases.

### The Cost of Neglect and Failure Demand
He introduces economic concepts of value demand (new feature work) versus failure demand (work caused by incomplete or faulty prior work). Much developer time is spent on failure demand, often due to neglect — the absence of needed attention. His informal observations suggest developers spend only about 5% of their time writing new code, with the majority fighting past neglected issues. This highlights the urgency of addressing neglect as a root cause.

### Housework as a Metaphor for Managing Technical Debt
Building on Ivon Lamb’s idea, Henny proposes that housework is an apt metaphor for technical debt management: continuous cleanup and maintenance prevents overwhelming accumulations. He cites Victorian wisdom that "clearing as you go" reduces extra work later, paralleling the need for integrated technical upkeep to prevent spiraling complexities.

### Final Reflections on Neglect, Awareness, and Habits
Kevin concludes that most software problems arise not from deliberate malice or incompetence but from neglect—an absence of consistent attention to upkeep. Solutions lie in developing awareness, implementing habits that integrate maintenance into daily work, and understanding software as ongoing products with continuous costs. Naming and conceptual clarity around neglect and technical debt are crucial for better management. Ultimately, how developers and organizations spend their time reflects their software’s health and viability.
