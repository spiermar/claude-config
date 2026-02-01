Claude Code has a few **built-in** subagents, and then the community has converged on a handful of **“usual suspects”** you’ll see in most issue→PR setups.

## Built-in Claude Code subagents (you’ll see these constantly)
- **Explore** – fast, read-only codebase search / understanding agent (optimized for discovery).  [oai_citation:0‡Claude Docs](https://docs.anthropic.com/en/docs/claude-code/sub-agents)  
- **Plan** – read-only research agent used during *plan mode* to gather context for a plan.  [oai_citation:1‡Claude Docs](https://docs.anthropic.com/en/docs/claude-code/sub-agents)  
- **General-purpose** – used when the task needs both exploration and changes (read + write/edit).  [oai_citation:2‡Claude Docs](https://docs.anthropic.com/en/docs/claude-code/sub-agents)  

## Popular custom subagents people actually use (especially for issue → PR)
These are common because they map cleanly to the software-dev loop:

### Review & quality gatekeepers
- **code-reviewer** (style, correctness, risks)  [oai_citation:3‡Claude Docs](https://docs.anthropic.com/en/docs/claude-code/common-workflows)  
- **security-auditor / security-engineer** (auth, injection, secrets, vuln patterns)  [oai_citation:4‡GitHub](https://github.com/VoltAgent/awesome-claude-code-subagents)  
- **performance-engineer** (hot paths, perf regressions)  [oai_citation:5‡GitHub](https://github.com/VoltAgent/awesome-claude-code-subagents)  
- **qa-expert / test-automator** (test coverage, flaky tests, harness improvements)  [oai_citation:6‡GitHub](https://github.com/VoltAgent/awesome-claude-code-subagents)  
- **accessibility-tester** (a11y checks for UI changes)  [oai_citation:7‡GitHub](https://github.com/VoltAgent/awesome-claude-code-subagents)  

### Debugging & “make CI green”
- **debugger** (root-cause + fix strategy)  [oai_citation:8‡Claude Docs](https://docs.anthropic.com/en/docs/claude-code/common-workflows)  
- **error-detective** (log/trace analysis, weird failures)  [oai_citation:9‡GitHub](https://github.com/VoltAgent/awesome-claude-code-subagents)  
- **devops-incident-responder / incident-responder** (when the “issue” is an outage / broken pipeline)  [oai_citation:10‡GitHub](https://github.com/VoltAgent/awesome-claude-code-subagents)  

### Builders (implementation specialists)
- **frontend-developer / backend-developer / fullstack-developer**  [oai_citation:11‡GitHub](https://github.com/VoltAgent/awesome-claude-code-subagents)  
- **api-designer** (REST/GraphQL shape, breaking-change avoidance)  [oai_citation:12‡GitHub](https://github.com/VoltAgent/awesome-claude-code-subagents)  
- **refactoring-specialist / legacy-modernizer** (safe migrations, mechanical refactors)  [oai_citation:13‡GitHub](https://github.com/VoltAgent/awesome-claude-code-subagents)  

### DevEx / docs (keeps PRs reviewable)
- **documentation-engineer / api-documenter** (update docs alongside code)  [oai_citation:14‡GitHub](https://github.com/VoltAgent/awesome-claude-code-subagents)  
- **git-workflow-manager** (branching, PR hygiene, commit structure)  [oai_citation:15‡GitHub](https://github.com/VoltAgent/awesome-claude-code-subagents)  

## Where people grab “popular packs”
A lot of folks use a community catalog like **VoltAgent’s “awesome-claude-code-subagents”** (100+ agents; includes things like `code-reviewer`, `debugger`, `security-auditor`, `test-automator`, etc.).  [oai_citation:16‡GitHub](https://github.com/VoltAgent/awesome-claude-code-subagents)

## My recommended “issue → PR” lineup (minimal, high leverage)
If you want a tight orchestrated flow without overcomplicating it:
1) **Explore** (built-in) → find relevant files  
2) **Plan** (built-in, plan mode) → produce a concrete change plan  
3) **test-automator** → add/adjust tests + run locally  
4) **debugger** → only if tests fail  
5) **code-reviewer** + **security-auditor** → final pass before opening PR
