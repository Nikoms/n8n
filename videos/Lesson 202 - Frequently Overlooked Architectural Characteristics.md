# Lesson 202 - Frequently Overlooked Architectural Characteristics
![thumbnail](https://i.ytimg.com/vi/Ojh8VoKsxqY/maxresdefault.jpg)
[https://youtu.be/Ojh8VoKsxqY?si=APLDsDDs8BnoSHG-](https://youtu.be/Ojh8VoKsxqY?si=APLDsDDs8BnoSHG-)

## My thoughts

The video highlights four frequently overlooked architectural characteristics: feasibility, observability, agility, and modularity. Observability is emphasized as a first-class citizen essential for measuring and understanding system behavior, not just an afterthought. Agility focuses on how quickly a system can evolve, be tested, and deployed, directly impacting time to market. Modularity supports this agility by breaking architecture into manageable, independent components, whether in distributed or monolithic systems.

## TLDR;
- Frequently overlooked architectural characteristics include feasibility, observability, agility, and modularity.
- Feasibility involves considering time, budget, team skill set, and experience constraints before designing solutions.
- Observability is critical for measuring and tracking architectural goals and should be integrated early, not added later.
- Agility refers to the ability to quickly respond to change, involving maintainability, testability, deployability, and evolvability.
- Modularity is key for breaking functionality into manageable pieces and applies to both distributed and monolithic architectures.
- These characteristics are often undervalued by junior architects despite their importance alongside operational characteristics like scalability and responsiveness.



## Content

### Introduction to Overlooked Architectural Characteristics
In this lesson number 202 of Software Architecture Monday, Mark Richards dives into some frequently overlooked architectural characteristics. These qualities—often called nonfunctional requirements or system quality attributes—are crucial but sometimes undervalued by junior architects. Understanding which characteristics matter most depends heavily on the domain and business requirements. For example, a stock trading system demands low latency and strong data integrity. However, beyond the obvious, there are key characteristics often missed in architectural design.

> "There are some undervalued and overlooked architectural characteristics, and I'm hoping this lesson sheds light on at least these four."

### 1. Feasibility
Feasibility tops the list of overlooked characteristics. Mark explains that feasibility entails more than just time and budget constraints; it also encompasses the skills and experience of the development team. Architects must critically assess if a proposed solution is realistically achievable given these constraints.

> "We may come up with the most fantastic solution but fail to question whether it's actually feasible given the time constraints, budget constraints, and the team's skill set and availability."

Ignoring feasibility can lead to architecture that is impractical or impossible to deliver successfully.

### 2. Observability
Observability is another essential but commonly neglected attribute. Mark and Neil Ford identify the fallacy that observability is optional—it's not. Observability allows teams to monitor how architecture performs against its goals over time, supporting architectural fitness functions. Unfortunately, observability is often added late, which undermines its effectiveness.

> "Observability shouldn’t be treated as a last-minute bolt-on but rather a first-class citizen in architecture."

Proper observability is especially vital in today's distributed architectures, enabling timely detection and resolution of issues.

### 3. Agility
Agility here means the ability to respond quickly to change, often expressed as time to market or speed to market. Mark breaks agility down into four critical components:
- **Maintainability:** Ease of locating and modifying code.
- **Testability:** Ability to comprehensively and easily test the system to track bugs.
- **Deployability:** Frequency, risk, and ceremony associated with software deployment.
- **Evolvability:** Ease of evolving architecture to support new features or business lines.

> "As we move faster, we need to track whether we are introducing more bugs or reducing them."

Agility involves measuring the rate of change in both the organization and the system and planning for rapid adaptation. Neglecting agility can seriously affect time to market and product competitiveness.

### 4. Modularity
Modularity is often overlooked but essential. It refers to breaking functionality into chunks that can vary in granularity. While microservices exemplify high modularity with fine-grained single-purpose services, modularity also applies to monolithic architectures:
- The **Modular Monolith** partitions functionality by domain within a monolith.
- The **Microkernel Architecture** achieves modularity through independent plug-in components.

> "Architectural modularity is not only restricted to distributed architectures; monolithic architectures can be modular too."

Good modularity improves manageability, scalability, and evolvability regardless of architectural style.

### Conclusion
Mark highlights these four overlooked characteristics—feasibility, observability, agility, and modularity—as vital for balanced architecture design. While operational attributes like scalability and responsiveness are often top of mind, these qualities deserve equal attention to ensure successful, adaptable systems.

> "Let's not forget these when we get excited about operational characteristics; they matter a lot."

Stay tuned for more lessons in Software Architecture Monday to deepen your understanding of essential architectural practices.
