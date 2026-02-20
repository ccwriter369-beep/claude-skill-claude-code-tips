---
name: claude-code-tips
description: |
  Optimizes Claude Code usage through expert context engineering, keyboard shortcuts, and rule management. Use this to streamline pair programming and minimize token bloat. Use when user says: "optimize my claude workflow", "set up a new project rules", "how to manage context window", "improve my validation loop".
source: "/tmp/yt-clean-transcript.txt"
extracted: "2026-02-20"
---

# Claude Code Productivity And Workflow Optimization

## Core Rules

- Run Claude from the project root directory to ensure proper context zipping and rule application.
- Initialize new projects with `/init` to create a foundational CLAUDE.md based on codebase analysis.
- Maintain a robust validation loop in CLAUDE.md (build/test commands) to enable agentic self-improvement.
- Prioritize CLAUDE.md rules from top to bottom (most important to least important).
- Keep CLAUDE.md focused and concise, ideally under 300 lines, to prevent context dilution.
- Use Plan Mode exclusively for starting new features to verify architectural assumptions before execution.
- Audit context usage regularly with `/context` to identify and remove token-heavy MCPs or bloat.
- Ask Claude to update CLAUDE.md rules automatically when it makes a mistake you have to fix manually.
- Use Git as the primary safety net and for generating summaries rather than relying on rewind features.
- Use model switching via `/models` to balance performance needs with token costs.

## When to Apply

- When starting a new project or onboarding a new codebase to Claude Code.
- When implementing complex features that require architectural verification.
- When experiencing model regression or frequent context-related errors.
- When token usage or costs need to be audited and optimized.

## Anti-Patterns

- Don't run Claude in subdirectories, as it may miss root-level context and rules.
- Avoid bloating CLAUDE.md with archaic patterns or excessive detail that confuses the AI.
- Don't ignore the context window; avoid long sessions without clearing or compacting context.
- Avoid over-relying on MCPs that consume high token counts for simple tasks.
- Don't manually edit CLAUDE.md for recurring errors; let Claude update the rules to ensure precise compliance.

## Workflow

1. Initialize the project using `/init` to establish the architecture and baseline rules.
2. Configure the validation loop in CLAUDE.md with specific build and test commands.
3. Toggle to Plan Mode (Shift+Tab) to outline the approach and verify assumptions.
4. Execute implementation in Edit Mode, using interrupts (Esc) if the model goes off track.
5. Audit context usage with `/context` and clear or compact as needed for new tasks.
6. Update CLAUDE.md rules immediately after identifying a 'never do this' pattern.
7. Finalize work by using Git for commits and Claude for generating test plans and summaries.

## Examples

- Initializing a Next.js project using `/init` to capture the Next.js 15 architecture and requirements.
- Switching to Plan Mode to double-check Swift UI implementation details before writing code.
- Using `/context` to discover that a specific Xcode MCP is blowing up the token count.
- Adding a specific 'always use this pattern' rule to CLAUDE.md after a manual correction.
