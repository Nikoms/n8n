---
title: "How to Improve Developer Productivity • Jez Humble • YOW! 2020 (en)"
date: 2025-10-18T21:40:28.038+02:00
category: videos
tags: [developer productivity, software delivery performance, continuous delivery, devops, lean management, software architecture, psychological safety, agile, cloud computing, remote work, COVID-19]
excerpt: "Dre Humble explores effective developer productivity measurement, continuous delivery, culture's impact, and how modern practices improve software delivery and organizational success."
---

![thumbnail](https://i.ytimg.com/vi/5_rrQND3lpQ/maxresdefault.jpg)
[https://youtu.be/5_rrQND3lpQ?si=CISwrakt0AM2ACdy](https://youtu.be/5_rrQND3lpQ?si=CISwrakt0AM2ACdy)

<!--- My thoughts -->

## Content

### Misconceptions in Measuring Developer Productivity
Dre Humble, a Site Reliability Engineer at Google, begins by highlighting common flawed approaches to measuring software developer productivity. Traditional metrics such as lines of code, velocity, and utilization are critiqued.

- **Lines of Code:** Counting lines of code incentivizes excessive code writing and maintenance burden rather than focusing on outcomes. A smaller, well-structured codebase is preferred over a large, complex one. For example, an engineer once deleted 10,000 lines of code while simplifying an early Mac program, improving the solution remarkably.

- **Velocity:** Used in Agile teams, velocity measures story points completed per iteration. However, it is not designed to compare teams and can lead to gaming the system, discouraging collaboration and distorting capacity management.

- **Utilization:** Measuring how busy team members are often undermines the need for slack capacity essential to deal with technical debt, unexpected events, and maintain long-term speed and quality.

### Measuring Software Delivery Performance
Effective measurement focuses on outcomes at the system level rather than individual output. Humble identifies four critical metrics from the DORA (DevOps Research and Assessment) program:

1. **Deploy Frequency:** How often deployments happen.
2. **Lead Time for Changes:** Time from code commit to production deployment.
3. **Change Failure Rate:** Percentage of deployments causing failures.
4. **Time to Restore Service:** Time to remediate incidents.

These metrics correlate strongly with organizational performance, profitability, customer satisfaction, and mission success. Elite performers excel by deploying multiple times per day, restoring services quickly, and maintaining low failure rates.

### Continuous Delivery and Architectural Considerations
Continuous delivery aims to make releases "boring"—safely automated, low-risk, and repeatable at any time. Key practices include trunk-based development, continuous integration, automated testing, and observability.

The deployment pipeline tests changes rapidly to catch issues early, reducing defects and improving quality. This approach integrates security testing, ensuring faster vulnerability remediation.

Architecture and team independence are crucial:

- Teams should be able to make large-scale changes, deploy on demand, and test independently without cross-team dependencies.
- Zero-downtime deployments during business hours are achievable and critical for agility.

Cloud adoption furthers these capabilities when implemented with characteristics such as on-demand self-service, broad network access, rapid elasticity, and pay-per-use models. Simply migrating to cloud infrastructure without process changes does not improve outcomes.

### Lean Management and Product Development Practices
Lean practices support productivity through:

- Limiting work in process and using visual management tools.
- Lightweight change approval facilitated by techniques like pair programming.
- Incremental delivery in small batches.
- Incorporation of customer feedback and team experimentation to innovate.

These practices enhance software delivery performance and reduce burnout.

### Building a Performance-Oriented Culture
Culture strongly influences productivity and innovation. Drawing on sociological research, Humble highlights the spectrum from pathological (blame-focused, punitive) to generative cultures that encourage cooperation, responsibility sharing, and embrace of novelty.

Psychological safety—the ability of team members to take risks and be vulnerable without fear of punishment—is paramount. Google research confirms this is the biggest factor in high-performing teams.

Leaders must model trust, encourage learning from failure, and resist scapegoating to foster such environments.

### Rethinking Individual Productivity
While productivity critics often discourage measuring individuals, Humble's research explores the feeling of productivity—focusing on deep work with minimal distractions. Key drivers include:

- Psychological safety.
- Usable, effective tooling and robust internal and external search.
- Reduced technical debt via maintainable code, manageable dependencies, and effective monitoring.

Increased individual productivity leads to better work recovery, less burnout, and better stress coping mechanisms. Experience level was surprisingly not a significant productivity factor.

### Insights on COVID-19 and Remote Work
Recent GitHub research analyzing system data reveals that developer activity remained stable or increased during the pandemic and remote work transition. This underscores the importance of flexible tools and processes to sustain productivity under disruption.

### Summary
Dre Humble's talk consolidates years of research showing that improving developer productivity requires valid metrics focused on outcomes, continuous delivery practices, effective culture, and enabling environments rather than simplistic output measurements. Investments in architecture, process, culture, and tooling collectively improve software delivery performance, organizational success, and developer well-being.

More detailed research, practical guidance, and resources can be found at cloud.google.com/devops.
