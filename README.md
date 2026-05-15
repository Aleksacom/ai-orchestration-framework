# AI Project Orchestration Framework

> A universal, tool-agnostic workflow framework that makes AI coding assistants pause, plan, and document — built for non-developers and solo builders who want speed AND structure.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Works with: Any AI](https://img.shields.io/badge/Works%20with-Any%20AI-blue)]()
[![No code required](https://img.shields.io/badge/Code%20required-No-green)]()

## The problem

If you've ever asked an AI coding assistant to "add a feature" and watched it change 12 files you didn't expect — this is for you.

AI coding tools are fast. Without structure, fast becomes risky:
- Changes you didn't approve
- Decisions baked in silently
- "Why is this here?" mysteries months later
- No paper trail when something breaks

## What this is

A single prompt you paste into ANY AI coding assistant. The AI then:
1. Asks 12 plain-English questions about your project
2. Recommends a workflow style matching your project (4 presets, from Light to High-Stakes)
3. Creates 5-7 framework files in your project
4. Walks you through git and GitHub setup if needed
5. Suggests a safe first task to practice the workflow
6. Teaches the AI to follow this structure on every future change

Result: every future change goes through `plan → verify → implement → review` before touching your code.

## Who this is for

✓ Non-developers building with AI assistants
✓ Solo developers shipping MVPs
✓ Small teams adopting AI coding tools
✓ Anyone tired of "vibe coding" chaos
✓ Indie hackers using Claude Code, Kimi CLI, Cursor

## How to use it

### Quick start (terminal AI users)

1. Open your AI coding tool (Claude Code, Kimi CLI, Cursor, etc.) in your project folder
2. Copy the entire contents of `setup-prompt.md`
3. Paste it as a single message to your AI
4. Answer the 12 questions
5. Approve the recommended preset
6. The AI creates the framework files

Total time: 15-30 minutes.

### Web AI users (Claude web, ChatGPT, Kimi web, Gemini)

Same flow, but you'll save files and run git commands manually. The AI tells you exactly what to type.


## What you get

After running through the setup:

```
your-project/
├── docs/
│   ├── orchestration/
│   │   ├── playbook.md          ← Your project's workflow guide
│   │   ├── conventions.md        ← Commit format, branch rules
│   │   └── sub-phase-template.md ← Template for new work
│   ├── decisions/
│   │   └── _template.md          ← Decision-doc template
│   └── backlog/
│       └── candidates.md         ← "Ideas for later" list
├── README.md
└── .gitignore                    ← Secrets protected from git
```

Plus a configured AI assistant that knows your project's conventions.

## The four preset profiles

The setup recommends one based on your project:

| Preset | For | Includes |
|---|---|---|
| **Light** | Just-starting solo projects | Single planning step, optional branches, minimal ceremony |
| **Standard** | Growing solo projects | Full 4-step gates, decision docs, branch + merge ceremony |
| **Collaborative** | Small teams (2-5) | All Standard + Pull Requests + mandatory reviewers |
| **High-Stakes** | Production / regulated | All Collaborative + compliance gates + 2+ reviewers required |

You can upgrade or downgrade later as your project evolves.

## Compatible AI tools

✅ **Fully automated** (terminal):
- Claude Code
- Kimi CLI
- Cursor
- Aider

⚠️ **Semi-manual** (web):
- Claude (claude.ai)
- ChatGPT (chat.openai.com)
- Kimi (kimi.com)
- Gemini (gemini.google.com)

Web AIs work fine but require manual file-saving and command execution.

## For Claude Code users — full automation available

If you specifically use Claude Code, there's a companion repo with pre-built 
sub-agents that fully automate the framework:

→ [Claude Code Orchestration Agents](https://github.com/Aleksacom/claude-code-orchestration-agents)

Includes cm-planner, cm-decider, reviewer, conventions-audit, test-author 
sub-agents plus a `/change` slash command. Drops into any project in 15 minutes.

For Kimi CLI, Cursor, ChatGPT, or other tools — use this repo's `setup-prompt.md`.

## Tool-specific implementations

   | AI tool | Repo |
   |---------|------|
   | Kimi CLI | [kimi-orchestration-bootstrap](https://github.com/Aleksacom/kimi-orchestration-bootstrap) |
   | Claude Code | [claude-code-orchestration-agents](https://github.com/Aleksacom/claude-code-orchestration-agents) |

## Why this framework exists

I'm a business analyst in banking-sector IT — not a developer. When AI coding tools made it possible for me to build my own projects, I loved the speed but kept losing track of what was happening. The AI would change things I didn't understand. Decisions would get re-debated because no one wrote them down. Mistakes compounded.

This framework is what I built for myself. The discipline I learned to apply after a few messy starts. Sharing it freely here so others can skip the painful learning curve.

## What this is NOT

- ❌ Not a code generator
- ❌ Not an AI tool itself (bring your own — Claude, Kimi, ChatGPT, etc.)
- ❌ Not magic — it works because YOU follow the discipline, with the AI as enforcer
- ❌ Not appropriate for every project (trivial changes don't need ceremony)

## License

MIT License — free to use, fork, modify, redistribute. See [LICENSE](LICENSE) for details.

## Acknowledgments

Built using AI assistants — the same tools the framework is designed to work with. Lived experience, not just theory.

---

**Star this repo if it helped you.** ⭐

**Found a problem?** [Open an issue](../../issues/new).

**Want updates?** [Watch this repo](../../subscription) for releases.
