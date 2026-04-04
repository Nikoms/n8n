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