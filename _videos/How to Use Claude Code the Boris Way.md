---
title: "How to Use Claude Code the Boris Way (en)"
date: 2026-04-04T23:02:29.806+02:00
category: videos
tags: [Claude Code,Anthropic,AI best practices,Context management,Plan mode,Verification,Claude MD,Skills,Parallel sessions,AI workflows,Software development,Automation,AI tools]
excerpt: "Comprehensive overview of Anthropic's Claude Code official best practices drawn from the documentation and developer Boris's real-world workflow, emphasizing context management, planning, verification, and workflow automation."
---

![thumbnail](https://i.ytimg.com/vi/1aCp9OT8rvw/maxresdefault.jpg)
[https://youtu.be/1aCp9OT8rvw?is=89qK4OEN8JBoSz8E](https://youtu.be/1aCp9OT8rvw?is=89qK4OEN8JBoSz8E)

## My thoughts

Not specified (yet)

## TLDR;
- Claude's context window is a critical, limited resource that must be managed carefully to avoid performance degradation.
- Use slash clear between unrelated tasks and sub agents for focused exploration to preserve context.
- Plan mode (explore, plan, implement, commit) improves output quality, especially for complex tasks; skip planning only for minor changes.
- Verification is essential: provide test cases, visual verification, or root cause analysis to have Claude validate its work.
- Keep Claude MD concise and focused (under 500 lines), updating it after every correction to compound improvements.
- Use parallel sessions and Git work trees to avoid context pollution and improve workflow efficiency.
- Employ skills for reusable domain knowledge and workflows; commit them to Git for cross-project reuse.
- The interview technique helps refine and clarify specs by having Claude ask questions before implementation.
- Avoid common pitfalls like the kitchen sink session, repeated corrections without resetting context, and overly long Claude MD files.
- Use tools like slashinit, post tool use hooks, and permission controls to automate and secure workflows.
- Accept that 10-20% of sessions may fail, and use efficient session management techniques to mitigate wasted effort.

These best practices come from Anthropic's official documentation and Boris, the creator of Claude Code, reflecting real-world workflow strategies used by the Claude Code team.



## Content

### Introduction
Anthropic recently updated their Claude Code documentation to include official best practices. Boris, the creator of Claude Code, alongside his team, shared practical insights and workflows that they use daily. This blog post provides a comprehensive breakdown of these recommendations with concrete tips for improving your own Claude Code workflows.

### Context Management: The Most Important Resource
At the core of Claude Code's best practices is context management. Claude's context window holds conversation history, file contents, commands, loaded skills, and more. When this window fills, Claude begins forgetting earlier instructions and makes more mistakes. Anthropic stresses managing this scarce resource carefully.

Boris implements this by running 5 to 10 parallel sessions, each focused on a single task. He uses slash clear between unrelated tasks and sub agents to offload deep exploration, preserving the cleanliness of main sessions. Tracking context usage through `/st status` keeps this limitation visible. Boris likens AI to a schedulable capacity rather than a single conversational tool.

### The Four-Phase Workflow: Explore, Plan, Implement, Commit
Anthropic prescribes a four-phase workflow:
1. **Explore in Plan Mode:** Enter plan mode (shift tab tab) to safely read files and ask questions without making changes.
2. **Plan:** Have Claude generate a detailed implementation plan. Review, refine, and iterate on it.
3. **Implement:** Exit plan mode and let Claude execute the approved plan with existing context.
4. **Commit:** Finalize and commit changes.

For simple fixes described in one sentence, planning may be skipped. Boris insists on always starting complex tasks in plan mode and iterating until the plan is solid before switching to auto-accept mode to prevent wasted corrections.

### Verification: The Highest Leverage Practice
Anthropic emphasizes making Claude verify its work as the most impactful quality booster. Without verification, constant manual feedback is required.

Three verification strategies include:
- Including test cases
- Visual verification (Boris uses the Claudin Chrome extension for UI testing)
- Root cause fixes

Boris insists on verification for every shipping change, embracing the "go fix it" pattern where Claude autonomously iterates until correct.

### Providing Precise Context and Prompting Techniques
Precise instructions reduce corrections. Claude Code best practices recommend scoping tasks, referencing sources, and describing symptoms clearly. Context can be given via direct file references, pasted images, URLs, or by piping data.

Advanced prompting includes:
- Writing detailed specs to reduce ambiguity
- Using voice dictation for quicker, more detailed prompts
- Having Claude act as a reviewer for changes

### Managing Claude MD: The Living Document
Claude MD contains bash commands, code style rules, testing instructions, repository etiquette, and architectural decisions unique to the project. It should exclude info Claude can infer or that changes frequently.

The key insight is to keep Claude MD under 500 lines and prune ruthlessly. Boris and his team update it multiple times weekly, tagging Claude during code review to improve guidelines automatically. Boris's golden rule: end every correction prompt with "update your Claude MD" to transform mistakes into permanent learning.

### Compound Engineering with Skills and Sub Agents
Skills are modular domain knowledge or workflows loaded on demand to reduce context bloat. Reusable skills are committed to Git and shared across projects. Boris's team also builds learning-focused skills, like spaced repetition for knowledge reinforcement.

Sub agents handle focused exploration or verification tasks, each with distinct responsibilities (e.g., code simplifier, verify app). They run in separate context windows, preserving the main session's focus.

### The Interview Technique for Complex Feature Specs
Using the new "ask user question" tool in Claude Code, the interview technique involves Claude interviewing the user to surface unconsidered details about UI, UX, edge cases, and trade-offs. This leads to more complete specs before implementation.

### Common Pitfalls and How to Avoid Them
Anthropic identifies frequent failure patterns:
- **Kitchen Sink Sessions:** Mixing unrelated tasks fills context with irrelevant info; fix by using slash clear or forking sessions.
- **Repeated Corrections:** After two failed corrections, reset context and improve the prompt.
- **Overly Long Claude MD:** Leads to ignored rules; fix by pruning.
- **Trust Then Verify Gap:** Provide verification or don’t ship.
- **Infinite Exploration:** Scope investigations narrowly or use sub agents.

Boris admits discarding 10-20% of sessions and advocates parallel sessions and quick abandonment to mitigate wasted effort.

### Session and Workflow Management Tips
- Use `/escape` to stop Claude mid-action and `/rewind` to restore earlier states.
- Aggressively manage context with `/clear` and controlled compaction.
- Use CLI tools like GitHub, AWS, and G-Cloud to enable external services with no rate limits.
- Use `/slashinit` to auto-detect codebase features.
- Emphasize critical rules in Claude MD files.
- Use child directories with their own Claude MD for modular context loading.
- Employ post tool use hooks for automatic formatting.
- Avoid unsafe permission settings in production; prefer pre-approvals and sandboxing for security.
- Always use the latest model (e.g., Opus 4.5) to reduce correction costs.

### Conclusion
The core messages from Anthropic and Boris are:
- Manage the context window carefully.
- Always provide verification criteria.
- Use a disciplined workflow of explore, plan, implement, and commit.
- Be specific in prompts and keep Claude MD concise and updated.
- Use sub agents and parallel sessions to avoid context pollution and dead ends.
- Automate repetitive workflows with skills and commands.
- Accept some session failures and manage sessions proactively.

These best practices, backed by those who built Claude Code, provide a powerful framework for leveraging Claude Code efficiently and effectively.

Applying these strategies will help optimize your workflows, reduce mistakes, and compound value over time.




> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/917](https://github.com/Nikoms/n8n/tree/main/ongoing/917)