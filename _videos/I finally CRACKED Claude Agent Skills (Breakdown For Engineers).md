---
title: "I finally CRACKED Claude Agent Skills (Breakdown For Engineers) (en)"
date: 2026-01-06T10:10:37.088+01:00
category: videos
tags: [cloud code, agent skills, MCP servers, sub agents, custom slash commands, agentic coding, prompt engineering, AI workflows, software engineering]
excerpt: "An in-depth exploration of Cloud Code's agent skills and related features clarifying their distinct roles, use cases, and how to effectively leverage them in AI-driven engineering workflows."
---

![thumbnail](https://i.ytimg.com/vi/kFpLzCVLA20/maxresdefault.jpg)
[https://youtu.be/kFpLzCVLA20?si=eICgZgfNcVcL-mfz](https://youtu.be/kFpLzCVLA20?si=eICgZgfNcVcL-mfz)

## My thoughts

Not specified (yet)

## TLDR;
- Agent skills allow autonomous application of custom expertise to repeat workflows, triggered by agents, and provide efficient context use and modularity.
- MCP servers connect agents to external tools and data sources; they are distinct from skills.
- Sub agents enable isolated, parallel workflows with separate context windows but lose context persistence.
- Custom slash commands are manually invoked, reusable prompt shortcuts; mastering prompt engineering is crucial.
- Skills support composability by using MCP servers, sub agents, and slash commands; they have a dedicated directory structure.
- Use cases:
  - Automatic PDF data extraction: Skill
  - Connecting to Jira or fetching weather data: MCP server
  - Parallel workflows (e.g., fixing tests): Sub agent
  - Simple one-step tasks (e.g., get commit messages, UI component creation): Custom slash command
- It is recommended to start with custom slash commands (prompts), then scale to sub agents for parallelism, and use skills for complex, reusable, modular solutions.
- Hooks add deterministic automation during lifecycle events.
- Plugins help package and share cloud code extensions.
- Output styles format agent outputs, enhancing usability.
- Pros of skills: agent-invoked, context protection, modular, composable, promote autonomy.
- Cons of skills: cannot nest sub agents or prompts inside skills fully; reliability and chaining of multiple skills need further testing; innovation is incremental.
- The prompt is the fundamental primitive; all agent coding builds atop context, model, prompt, and tools.
- The creator rates skills 8/10, sees them as a powerful compositional layer rather than a replacement for other features.



## Content

### Understanding Agent Skills and Related Cloud Code Features

Agent skills, sub agents, MCP servers, and custom slash commands may seem overlapping but serve distinct purposes in cloud code engineering. Agent skills are designed to apply custom expertise autonomously to repetitive workflows triggered by agents. They offer efficient usage of context through progressive disclosure and follow a dedicated modular directory structure. This modularity allows for building repeatable solutions that agents can invoke.

### Differentiating Key Features

MCP servers connect agents with external tools and data sources, which is fundamentally different from agent skills. Sub agents isolate workloads into separate context windows enabling parallelization but lose context persistence. Custom slash commands are manual prompt shortcuts that developers invoke, acting as the primitive building block closest to raw prompt engineering.

### When to Use What: Use Case Breakdown

- **Skills:** Best for automatic behaviors such as extracting text from PDFs or managing complex workflows that require reusable, modular solutions.
- **MCP Servers:** Ideal for external integrations like connecting to Jira or fetching real-time weather data.
- **Sub Agents:** Perfect for isolated, parallelizable workflows that don't require context persistence like scalable debugging or security audits.
- **Custom Slash Commands:** Suitable for simple, one-off tasks like getting commit messages or creating UI components.

For example, creating git work trees can be approached in multiple ways: a prompt (custom slash command) for simple creation, a sub agent for parallel tree creation, and a skill for managing multiple such work trees with reusable, automated operations.

### Composability and Hierarchies

Skills can compose many MCP servers, sub agents, and custom slash commands, placing them at the top of the compositional hierarchy. Custom slash commands (prompts) are fundamental primitives; mastering prompt engineering is essential for agentic coding success. The integration and composition between these features allow for flexible, scalable agent workflows.

### Additional Cloud Code Features

Hooks provide deterministic automations that trigger at specific lifecycle events, balancing autonomy with control. Plugins offer a way to package and distribute sets of functionalities, making it easier to share cloud code extensions. Output styles format the agent’s outputs in usable forms like text-to-speech or summaries, enhancing user interaction.

### Pros and Cons of Agent Skills

**Pros:**
- Agent-invoked autonomy enhances delegation.
- Protects context with progressive disclosure.
- Clear, modular directory structure for repeatable solutions.
- Composability with other features.
- Encourages agentic approaches where the agent chooses the right skill.

**Cons:**
- Cannot fully nest sub agents or embed prompts inside skills.
- Uncertain reliability when chaining multiple skills in production.
- Incremental innovation; skills largely concatenate prompt engineering and modularity rather than create fundamentally new capabilities.

### Conclusion: The Fundamental Role of Prompts

At the core, every agent system revolves around four components: context, model, prompt, and tools. Prompts remain the fundamental unit of knowledge work and agent coding. Developers are recommended to start with custom slash commands (prompts) to build foundational skills before scaling with sub agents and skills for more complex, parallelized, and modular solutions.

The new agent skills feature is a powerful addition to Cloud Code, earning an 8 out of 10 from the creator, who emphasizes its role as a compositional layer rather than a replacement for existing features. This nuanced understanding and careful use of these tools will help engineers master agentic coding and build sophisticated, reliable AI-driven workflows.

"If you master the fundamentals, you'll master the compositional units, you'll master the features, and then you'll master the tools."

This codebase and example skills are available publicly, encouraging developers to explore and customize their agent skill workflows, pushing the boundaries of autonomous agent engineering.

Stay focused and keep building.




> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/833](https://github.com/Nikoms/n8n/tree/main/ongoing/833)