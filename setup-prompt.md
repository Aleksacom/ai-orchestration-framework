# Universal Project Orchestration Framework — Setup Prompt

## What this prompt does

- Asks 12 plain-English questions about your project (one section at a time, not all at once)
- Recommends a workflow style that fits your project — pick from 4 presets ranging from Light to High-Stakes
- Creates 5–7 small framework files in your project that hold decisions, conventions, and templates
- Walks you through git and GitHub setup if you don't already have them
- Suggests a safe first task so you can practice the workflow before doing real work
- Teaches your AI assistant to follow this structure on every future change

## How it helps you

- The AI always shows you its plan BEFORE making changes — no surprises, no "wait, what did it just do?"
- Important decisions get written down in plain English, so future-you can read the reasoning months later
- Every change goes through git, which means mistakes are easy to undo
- You stay in control — the AI pauses for your approval at key moments
- Works whether you're solo or with a team, beginner or experienced
- Works with any AI tool: Claude Code, Kimi CLI, Cursor, ChatGPT, Claude web, Kimi web, Gemini

## Why this matters

- AI assistants can change many files in seconds — without structure, that speed becomes risk
- The "why did we do this?" question shows up later (when you've forgotten, or someone new joins). A written paper trail saves hours of guessing.
- Small projects grow. Today's habits shape how messy or clean your project feels in 6 months.
- Mistakes are recoverable when changes are tracked, reversible, and reasoned-about
- This framework codifies practices experienced developers learn the hard way — so you don't have to

---

**Paste this entire document into your AI coding assistant. The assistant will read it, ask you a few questions about your project, then set up a structured workflow for managing changes.**

**You do NOT need to be a developer to use this.** The prompt is written in plain English. The AI will guide you step by step.

---

## Before you start: where do you actually run this?

**If you've never used an AI coding tool before, start here.** This section explains the practical setup. Skip it if you already know.

### Two ways to run this prompt

**Option 1: Terminal AI tool (recommended)**
- You install a small app on your computer that lets you talk to an AI in a "terminal" (a text-based window).
- The AI can read your files, create new ones, run commands, and do real work on your computer.
- Examples: **Claude Code**, **Kimi CLI**, **Cursor**, **Aider**.
- Best for: setting up the framework, then doing real project work with it.

**Option 2: Web AI (works but more manual)**
- You use an AI chatbot in your browser (no install needed).
- The AI can read what you paste and tell you what to do, but it can't directly touch your files.
- Examples: **Claude** (claude.ai), **ChatGPT** (chat.openai.com), **Kimi** (kimi.com), **Gemini** (gemini.google.com).
- Best for: planning, learning, asking questions. Works for setup too but you'll be saving files and running commands manually.

**Beginner-friendly path:** if you're new to terminals, use a terminal AI tool, but pair it with a friendly terminal app (recommended below). It's not as scary as it looks.

### What is a "terminal" anyway?

A terminal (also called "command line" or "shell") is a text-based way to control your computer. Instead of clicking icons, you type commands. It looks intimidating at first because old terminals were ugly green-on-black text, but modern terminals are clean, friendly, and even have AI built in.

**You only need to type a few simple commands to use this framework. The AI does the rest.**

### Recommended terminal apps (free, beginner-friendly)

**Warp (best for non-developers)** — modern terminal with AI built in. Looks clean. Helps you when you don't know what to type. Works on Mac, Windows, and Linux.
- Download: warp.dev
- Why this one: feels less like "scary developer tool" and more like "modern app." Has its own AI helper if you get stuck.

**Other options if you prefer:**
- **Mac users:** the built-in "Terminal" app (Applications → Utilities → Terminal) works fine
- **Windows users:** "Windows Terminal" (free from Microsoft Store) or just "Command Prompt" / "PowerShell" (already installed)
- **Linux users:** you already know

For this guide, instructions assume Warp, but they work in any terminal.

### How to set up your AI tool (one-time, ~10 minutes)

This is the part that intimidates non-developers most. It's actually quick.

**Step 1: Install a terminal.** Download Warp from warp.dev. Install it like any other app.

**Step 2: Install an AI coding tool.** Pick ONE based on what you already use:

- **If you have a Claude account:** install Claude Code. Open Warp. Type this and press Enter:
  ```
  curl -fsSL https://claude.ai/install.sh | sh
  ```
  Or visit claude.ai/code for current install instructions.

- **If you want to use Kimi:** install Kimi CLI. Open Warp. Type:
  ```
  npm install -g @kimi/cli
  ```
  (You may need to install Node.js first from nodejs.org if you don't have it. The terminal will tell you if it's missing.)

- **If you want to use Cursor:** download from cursor.com. Cursor is a code editor with AI built in — it's not a terminal tool, but it works similarly. You'd paste the prompt into Cursor's AI chat panel instead of a terminal.

**Step 3: Find your project folder.** Wherever your project lives on your computer. If you don't have one yet, just create a folder (e.g., on your Desktop call it `my-project`).

**Step 4: Navigate to that folder in the terminal.** In Warp, type:
  ```
  cd ~/Desktop/my-project
  ```
  (Replace with your actual folder name and location. `cd` means "change directory" — it's how you move around folders in a terminal.)

  If you don't know the path: in Warp, you can drag the folder from Finder/Explorer into the terminal window and it auto-fills the path.

**Step 5: Start your AI tool.** Type its name:
  - Claude Code: `claude`
  - Kimi CLI: `kimi`
  - The tool starts a chat session right in the terminal.

**Step 6: Paste this entire prompt.** Copy everything in this document, paste it into your AI tool's chat (in the terminal). Press Enter.

The AI takes over from there.

### What does "paste this prompt" actually mean?

When this guide says "paste this prompt," it means:

1. Open this document (`universal-orchestration-setup-prompt.md`)
2. Select all the text (`Cmd+A` on Mac, `Ctrl+A` on Windows)
3. Copy it (`Cmd+C` / `Ctrl+C`)
4. Click into your AI tool's chat input (terminal or web)
5. Paste it (`Cmd+V` / `Ctrl+V`)
6. Press Enter (or send)

The AI reads the entire prompt as one big message, understands it, then starts asking you the questions in Section 1 below.

### If you get stuck

- **In Warp:** there's a built-in AI helper. Press `Cmd+I` (Mac) or `Ctrl+I` (Windows) and ask in plain English: "How do I navigate to my Desktop folder?" — Warp will tell you.
- **General terminal help:** any of the web AI tools (Claude, ChatGPT, Kimi) will explain terminal commands if you ask: "I'm using Warp on a Mac, how do I go to my Documents folder?"
- **If something goes wrong:** terminals are very hard to permanently break. Worst case, close the terminal window and start over. The framework files (if any were created) are still on your computer.

### Web AI path (if you don't want to install anything)

If installing a terminal AI tool feels like too much right now, you can use the framework with a web AI. It's more manual but works.

1. Open Claude, ChatGPT, Kimi, or Gemini in your browser
2. Paste this entire document into the chat
3. Answer the questions the AI asks
4. The AI will give you the CONTENT of each framework file to save manually
5. You'll need to:
   - Create the files yourself (open a text editor like VS Code, Notepad, or TextEdit)
   - Save them in the right folders within your project
   - If using git: type the git commands the AI tells you in a terminal (yes, you'll still need a terminal eventually for git, but the AI tells you exactly what to type)

**Honest take:** the terminal AI path is genuinely easier once you've spent the 15 minutes to set it up. The web AI path keeps the "no install" appeal but adds 30-60 minutes of manual file-management work. Choose based on your patience for setup vs your patience for manual steps.

---

## What is this?

A workflow framework that makes building any project (app, website, tool, automation) more reliable and less stressful — especially when you're working with an AI assistant.

**The problem this solves:** When you ask an AI to build or change something in your project, it sometimes:
- Skips important decisions silently
- Mixes "planning what to do" with "doing it"
- Forgets context between sessions
- Makes changes you didn't intend
- Loses track of why something was done a particular way

**The solution:** A small set of habits the AI follows every time it changes something:
- **Plan before doing** — the AI tells you what it's about to do and gets your approval first
- **Verify before changing** — the AI checks the actual state of your project before making changes
- **Show its work** — every command the AI runs is visible to you
- **Write down decisions** — the AI keeps a short note explaining each significant choice, so you (or someone else) can read it later
- **Backup-friendly** — every change goes through git (a backup system for code), so nothing is ever truly lost

You can use this for any kind of project: an app, a website, a script, a content generator, a data pipeline, anything.

---

## Glossary (plain English)

Don't worry if you don't know these yet. The AI will explain them in context as it goes.

- **Project** — Any folder on your computer containing the work you're building (could be code, documents, configurations, anything).
- **Git** — A free tool that tracks every change you make to files in your project. Like "undo history" but for entire folders. Most coding projects use git.
- **Repository (repo)** — Another word for "project folder being tracked by git."
- **GitHub** — A free website where you can store a copy of your project in the cloud. Backup + sharing + collaboration in one place. Owned by Microsoft.
- **Branch** — A workspace within your project where you can try changes without affecting the main version. When you're happy, you merge the branch back to "main."
- **Commit** — Saving a snapshot of your project at a moment in time. Each commit has a short message explaining what changed.
- **Push** — Uploading your saved changes from your computer to GitHub.
- **Pull** — Downloading the latest changes from GitHub to your computer.
- **Merge** — Combining a branch back into the main version of your project.
- **AI assistant / coding assistant** — A tool like Claude Code, Kimi CLI, Cursor, or ChatGPT that helps you write code or set up projects by understanding natural-language instructions.
- **Sub-phase** — One self-contained chunk of work (e.g., "add a contact form" or "fix the login bug"). The framework treats each sub-phase as one unit with planning, work, and review steps.
- **Gate** — A pause point during a sub-phase where the AI stops and asks for your approval before continuing.
- **Decision doc** — A short note (saved as a file in your project) that records a significant choice and why you made it. Like keeping a journal of important decisions.
- **Convention** — A rule the project agrees to follow (e.g., "all commit messages start with `feat:` or `fix:`"). Conventions make the project easier to navigate over time.

---

## How this works

When you paste this entire document to your AI assistant:

1. The AI reads it and understands the framework.
2. The AI asks you 5–10 questions about your project (or you can pick a preset).
3. The AI proposes a setup tailored to your project.
4. You approve or adjust the proposal.
5. The AI creates ~5 small framework files in your project.
6. You commit those files (the AI helps you do this).
7. Every future change you ask the AI to make follows the framework.

**Total setup time:** 15–30 minutes the first time. After that, the framework runs in the background — you barely notice it.

---

## Instructions for the AI assistant (READ THIS CAREFULLY)

**You are setting up a project orchestration framework. Your job is:**

1. **Read this entire document first.** Don't skim. The framework details matter.

2. **Ask the user the Discovery Questions below.** Ask one section at a time, not all at once — wait for their answers before moving to the next section. Be friendly and explain WHY each question matters in plain English.

3. **Recommend a preset profile** based on their answers (see Preset Profiles section). Show them the preset and explain what it includes. Let them adjust if they want.

4. **Handle git/GitHub setup if needed.** Some users won't have git installed or won't have a GitHub account. Walk them through it patiently using the Git/GitHub Setup section.

5. **Create the framework files** following the File Generation Spec section. Customize each file's content based on the user's project context.

6. **Commit the files via the user's git** (you can run the commands; explain what each one does).

7. **Suggest a first low-risk sub-phase** they can try to test the framework (see First Sub-Phase Suggestion section).

**Important rules for you, the AI:**

- **Announce every command you're about to run BEFORE running it.** Tell the user what the command does in plain English. If they say no or aren't sure, don't run it.
- **One question at a time, not bulk Q&A.** Wait for each answer.
- **Plain English. No jargon without explaining it.** The user is not a developer.
- **If the user seems confused or stuck, slow down.** Re-explain. Offer simpler options.
- **Don't overwrite existing files without confirming.** If a file already exists in their project at a path you're about to write, surface it and ask.
- **NEVER commit secrets** (API keys, passwords, personal data). Add a `.gitignore` entry if there's risk.

---

## Discovery Questions

Ask these one section at a time. Wait for answers before moving on.

### Section 1 — About the project (3 questions)

**Q1.** In 1–2 sentences in plain English, what are you building? (Example: "A daily email that sends me a summary of crypto prices" or "A website for my photography business")

**Q2.** What stage is the project in?
- (a) Just an idea, nothing built yet
- (b) Started but very early (a few files, maybe a few hours of work)
- (c) Partway built (some features working, some not)
- (d) Mostly built (just adding features or fixing things)

**Q3.** Who is working on the project?
- (a) Just me (solo)
- (b) Me plus 1 friend / collaborator
- (c) A small team (3–5 people)
- (d) A larger team (5+)

### Section 2 — What's at stake (2 questions)

**Q4.** What kind of project is this?
- (a) Learning / playing / personal experiment — no real consequences if it breaks
- (b) Personal tool — only I use it, but I'd be annoyed if data got lost
- (c) Real users — other people will use this; their experience matters
- (d) High-stakes — handles payments, health data, legal data, or other sensitive info

**Q5.** Where will the project run?
- (a) Just on my computer
- (b) Online (website, app, server)
- (c) Both — I work on it locally, but it eventually runs online
- (d) Not sure yet

### Section 3 — Technical context (2–3 questions)

**Q6.** What technology does the project use? (Pick the closest match — it's OK if you're not sure)
- (a) I'm not coding — this is for documents, content, or planning
- (b) Python (data, scripts, automation, AI tools)
- (c) JavaScript / TypeScript (websites, apps, browser tools)
- (d) Web technology (HTML/CSS/JavaScript for websites)
- (e) Mixed — multiple languages
- (f) Something else (please specify)
- (g) Not sure — the AI assistant is choosing for me

**Q7.** Which AI tool are you using to build this project?
- (a) Claude Code (terminal-based, by Anthropic)
- (b) Kimi CLI (terminal-based, by Moonshot)
- (c) Cursor (code editor with AI built in)
- (d) ChatGPT or Claude on the web
- (e) Something else
- (f) Not sure / multiple

**Q8.** (Conditional — only ask if Q7 = e or f) Can you tell me a bit about how that tool works? Does it have access to your files? Can it run commands?

### Section 4 — Git and GitHub (2–3 questions)

**Q9.** Do you have a GitHub account?
- (a) Yes, and I use it regularly
- (b) Yes, but I rarely use it
- (c) No, but I've heard of it
- (d) No, I don't know what it is

**Q10.** Is your project folder already set up with git?
- (a) Yes, and I use git regularly
- (b) Yes, but I'm not sure how to use it well
- (c) No
- (d) Not sure

**Q11.** (Optional — only ask if useful) Do you want this project backed up online (GitHub) or kept just on your computer?

### Section 5 — Final context (1 question)

**Q12.** Anything else important about this project I should know? Examples:
- "It has rules I want to follow (e.g., all decisions should be reviewed by my co-founder)"
- "I'm replacing an older system with this one"
- "I need to be able to demo it next month"
- "I'll be the only one maintaining it long-term"

(Or just "nothing else" — that's fine too.)

---

## Preset Profiles

After Discovery Questions, recommend one of these presets. Explain it in plain English. Let the user adjust.

### Preset 1 — Light (Just Starting)
**Match this when:** Q2 = (a) or (b), Q4 = (a) or (b), Q3 = (a)

**What's included:**
- Single planning step before each sub-phase (no separate prep + planning gates)
- Decision docs only for "real decisions" (not routine work)
- Direct commit to main acceptable for first ~10 commits while you find your footing
- Branch + merge optional — use it if it feels natural, skip if not
- No convention audits

**Why this works:** When you're just starting, heavy ceremony slows you down. The Light preset gives you structure without overhead. You can upgrade later.

**Example sub-phase flow:**
1. You: "Add a contact form to the homepage"
2. AI: "Here's my plan: [outlines what files to change, what the form will do]. Approve?"
3. You: "Yes, but make the form simpler"
4. AI: "Updated plan: [revised]. Approve?"
5. You: "Yes, proceed"
6. AI: [makes the changes, shows you each command]
7. You: "Looks good"
8. AI: [commits the work]

### Preset 2 — Standard (Growing Project)
**Match this when:** Q2 = (b) or (c), Q4 = (b) or (c), Q3 = (a) or (b)

**What's included:**
- Full 4-step planning gates (plan → verify → implement → review)
- Decision docs for all substantive choices
- Branch + merge ceremony for every change
- Convention rules (commit format, file structure)
- Backlog file for tracking deferred ideas

**Why this works:** As your project grows, untracked decisions become "why is this here?" questions later. The Standard preset captures decisions as you make them, so future-you doesn't have to reconstruct.

**Example sub-phase flow:**
1. You: "Add user authentication"
2. AI: "Plan: [files, approach, decisions to ratify with you]. Decisions for you: should we use email/password or social login?"
3. You: "Email/password"
4. AI: "Verifying current state: [checks the project, confirms what's there]. Ready to proceed?"
5. You: "Go"
6. AI: [creates a git branch, makes changes, shows commands]
7. AI: "Pre-merge review: [tests pass, no issues, here's the diff]. Approve merge?"
8. You: "Yes"
9. AI: [merges the branch into main, pushes to GitHub if applicable]

### Preset 3 — Collaborative (Small Team)
**Match this when:** Q3 = (b), (c), or (d)

**What's included:**
- Full planning gates
- All work goes through Pull Requests (PRs) on GitHub
- At least one teammate reviews each change
- Decision docs are mandatory
- Backlog is shared across the team
- Conventions enforced strictly

**Why this works:** With a team, the "what did you change and why" question comes up daily. The Collaborative preset makes that conversation easy by capturing context in files everyone can read.

### Preset 4 — High-Stakes (Production / Regulated)
**Match this when:** Q4 = (d), OR Q2 = (d) with Q5 = (b) or (c)

**What's included:**
- Full planning gates plus an extra "compliance check" gate at the end
- All decisions get decision docs WITH compliance notes (e.g., "does this affect data privacy?")
- Pull Requests with mandatory minimum 2 reviewers
- Audit trail in PR descriptions
- Security review at planning gate for any external dependency
- No direct commits to main, ever

**Why this works:** When real money or sensitive data is involved, "I think I remember why we did this" isn't good enough. The High-Stakes preset gives you a paper trail strong enough to defend in front of an auditor, lawyer, or angry customer.

---

## Git/GitHub Setup (only if needed)

If the user has git and GitHub set up, skip this section.

If they don't:

### Path A — User has nothing, project doesn't exist yet
Walk them through:
1. Install git (explain what it is, give them the link for their OS: git-scm.com/downloads)
2. Create a GitHub account if needed (github.com/signup)
3. Configure git with their name + email (one-time setup commands)
4. Create the project folder
5. Initialize git in the folder (`git init`)
6. (Optional) Create a GitHub repo and link the local folder to it

### Path B — User has git but no GitHub
Walk them through:
1. Create a GitHub account (github.com/signup)
2. Create a new repository on github.com (call it the project name)
3. Connect the local folder to the GitHub repo (`git remote add origin <url>`)
4. Push the existing work up (`git push -u origin main`)

### Path C — User has GitHub but no git locally
Walk them through:
1. Install git
2. Clone their existing GitHub repo to their computer (`git clone <url>`)
3. Continue from there

### Path D — Has both, just needs setup in this specific folder
Walk them through:
1. Open terminal in the project folder
2. Initialize git (`git init`)
3. Create the GitHub repo (or link an existing one)
4. Push existing work

**For all paths:** Make sure the user has a `.gitignore` file before any commits. Add common secrets to it:
```
# Environment variables and secrets
.env
.env.local
*.key
*.pem
secrets/
node_modules/
__pycache__/
.DS_Store
```

Explain in plain English: ".gitignore tells git which files NOT to track. We want secrets and passwords NEVER to end up on GitHub by accident."

---

## File Generation Spec

After preset is chosen, create these files in the project (paths relative to project root):

### File 1: `docs/orchestration/playbook.md`
**Purpose:** The framework concepts and workflow. Other files reference this.
**Contents:** Explains what gates are, when to pause, how planning/verifying/implementing/reviewing works, what auto-resolve vs escalate means, how branches and merges flow. Tailored to the preset chosen.
**Length:** ~300–500 lines depending on preset (Light is shorter; High-Stakes is longer).

### File 2: `docs/orchestration/conventions.md`
**Purpose:** The rules the AI follows when working on this project.
**Contents:**
- Commit message format (e.g., `type(scope): subject`, max 72 characters)
- Branch naming format (e.g., `feat/short-description`)
- Decision-doc filename format
- Backlog entry format
- Tripwire rules (announce all commands before running)
- Any user-specific conventions from Q12

### File 3: `docs/orchestration/sub-phase-template.md`
**Purpose:** A fill-in-the-blank template the user (or AI) uses to start any new sub-phase.
**Contents:** A markdown template with sections for goal, scope, branch name, expected pauses, etc.

### File 4: `docs/decisions/_template.md`
**Purpose:** Template for decision docs. Each substantive decision becomes a copy of this template.
**Contents:**
```markdown
---
decision-id: [date]-[slug]
date: YYYY-MM-DD
status: active
applies-to: [sub-phase or area]
approved-by: [name]
---

# [Decision title in plain English]

## Why we needed to decide
[1–3 sentences in plain English]

## Options we considered
- Option A: [...]
- Option B: [...]
- (etc.)

## What we chose
Option X — [name]

## Why
[2–5 sentences in plain English]

## What this means going forward
- [Impact 1]
- [Impact 2]

## If we want to change this later
[What would prompt revisiting this decision]
```

### File 5: `docs/backlog/candidates.md`
**Purpose:** A list of "ideas for later" — things we considered but decided not to do now.
**Contents:** Initialized empty with structure for Active, Deferred, and Done sections plus an entry-format template.

### File 6: `README.md` (only if not already present)
**Purpose:** Project overview readable by anyone who finds the project.
**Contents:** Project name, what it does in 1–2 sentences, who it's for, link to the orchestration playbook.

### File 7: `.gitignore` (only if not already present, or extend if exists)
**Purpose:** Prevents secrets from being committed.
**Contents:** Standard ignores for the user's tech stack + secrets entries.

---

## First Sub-Phase Suggestion

After framework setup is done, suggest a low-risk first sub-phase the user can try. The goal is to practice the workflow on something safe before doing real work.

**Good first sub-phases (pick one matching the project type):**

- "Add a `CHANGELOG.md` file documenting what's been built so far"
- "Add a `CONTRIBUTING.md` file explaining how someone new could help"
- "Create a basic project status page or README update"
- "Add example configuration files (`.env.example`) so future-you remembers what variables are needed"
- "Document the decisions already baked into the project — migrate them into individual decision docs"

The point isn't the work itself — it's experiencing one full sub-phase end-to-end (plan → verify → implement → review → merge) on something low-stakes.

After the practice sub-phase succeeds, the user can apply the framework to real work.

---

## What this framework is NOT for

Some changes don't need the full ceremony. Use direct commits for:

- **Typo fixes** in documentation or comments
- **Renaming a single variable** for clarity
- **Bumping a dependency version** (assuming tests pass)
- **Reformatting code** (no logic change)
- **Adding a comment** explaining existing code

Rule of thumb: if a change took less than 5 minutes and you're sure it can't break anything, just commit it directly. Save the framework for changes that involve real decisions or could affect other parts of the project.

---

## Recovery Patterns

What to do when things go sideways. The AI should mention this section to the user once setup is complete so they know help is available.

### "I made a mistake on a branch — how do I undo it?"
- `git checkout main` — go back to the main version, your mistake is on the branch
- `git branch -D bad-branch-name` — delete the branch entirely if you want to start over
- The mistake never reached `main`, so the main version is safe.

### "I committed something I shouldn't have (secrets, sensitive data)"
- Stop what you're doing. Do NOT push to GitHub if you haven't yet.
- Tell the AI assistant immediately. There are specific git commands to remove the commit from history.
- If it's already on GitHub: assume the secret is compromised. Rotate the API key / password / token immediately. Then clean up history.

### "I'm lost in a sub-phase and don't know what to do next"
- Ask the AI: "Where are we in this sub-phase? What's the next step?"
- The AI should remind you which gate you're at (plan, verify, implement, review) and what's needed next.

### "The AI did something I didn't approve"
- Stop the AI immediately.
- Ask: "Show me every command you just ran and what file it changed."
- Decide what to keep and what to undo.
- This is exactly what the tripwire discipline is supposed to prevent — surface it as a process failure.

### "I want to delete this project and start over"
- The project folder lives on your computer. You can delete it.
- If you pushed to GitHub, you can delete the repo there too.
- Nothing the framework created is irreversible.

### "I think the framework is too heavy — can I downgrade?"
- Yes. Tell the AI: "Switch this project from [current preset] to [lighter preset]." The AI should update the playbook and conventions accordingly.

### "I think the framework isn't strong enough — can I upgrade?"
- Yes. Same conversation, just upgrade direction.

---

## Privacy and Security Reminders

The AI should walk the user through these once during setup. Non-developers especially benefit from these explicitly.

1. **Never commit secrets to git.** API keys, passwords, tokens, personal info — none of it goes in git. Use `.env` files and add them to `.gitignore`.

2. **Be careful what you push to public repos.** A public GitHub repo can be read by anyone in the world. Default to private repos for personal projects.

3. **Decision docs can contain sensitive context.** If you record decisions involving customer info or business plans, consider whether the repo should be private.

4. **AI assistants can see everything in your project folder.** Don't put secrets in plain text files you ask the AI to read.

5. **Removing a secret from a current commit doesn't remove it from history.** Once a secret is in git history, it's there until you rewrite history (which is risky). Better to never commit it in the first place.

---

## Cost Considerations (for paid AI tools)

Some AI tools charge per use. Help the user understand rough costs:

- **Each sub-phase** typically uses ~5,000–50,000 tokens of conversation, depending on complexity.
- **At Claude Sonnet pricing** (~$3 per million input tokens, $15 per million output as of 2026), a typical sub-phase costs ~$0.02–$0.50.
- **At Claude Opus pricing** (~$15 input, $75 output), a typical sub-phase costs ~$0.10–$2.50.
- **A full project with 20–30 sub-phases** might total $1–$30 in AI costs across the project's life.
- **Free tools** (some Kimi tiers, some ChatGPT tiers) don't charge per use but may have daily limits.

**Recommendation:** Start with the cheaper model (Sonnet equivalent) for routine work. Only use the more expensive model (Opus equivalent) for genuinely complex decisions — architecture questions, debugging hard problems, designing core systems.

---

## When to update or evolve the framework

This is a living framework. After using it for a few sub-phases, the user might notice:

- "I keep being asked to ratify the same kind of decision — can it just auto-resolve?"
- "There's a pattern in the conventions that doesn't fit my project."
- "I want to add a new gate for [specific check]."

These adjustments are healthy. Update `docs/orchestration/playbook.md` and `conventions.md` to reflect the project's evolved needs. Treat the framework update itself as a sub-phase (plan → implement → commit).

---

## For the AI: end-state checklist

Before you're done with framework setup, confirm:

- [ ] Discovery Questions answered, preset chosen
- [ ] Git is initialized in the project folder
- [ ] `.gitignore` exists with appropriate entries
- [ ] All 5–7 framework files created and committed
- [ ] First commit message follows the conventions chosen
- [ ] If GitHub is in use: project pushed to remote successfully
- [ ] User shown a sample sub-phase invocation (paste-able next time they want to do something)
- [ ] User given the recovery patterns reference
- [ ] User encouraged to try the first sub-phase suggestion

**Once all confirmed, tell the user:** "Setup complete. You can now start any new piece of work by saying 'I want to [thing]' — I'll respond with a plan, you approve, and we'll go through the gates together. Try the practice sub-phase whenever you're ready."

---

## Final note for the user

This framework is meant to reduce stress, not add it. If at any point it feels like overhead instead of help, tell the AI: "This is getting in the way — can we simplify?" The AI will adjust.

The discipline matters most for:
- Decisions you'll need to remember later
- Changes that could break other things
- Work where you're collaborating with others (now or in the future)

It matters less for:
- Quick experiments
- Throwaway scripts
- Personal notes / drafts

Pick your battles. The framework works best when it's helping you, not policing you.

---

*End of universal orchestration framework setup prompt.*

*AI: now begin at Section 1, Question 1 of Discovery Questions. Ask one section at a time, wait for answers.*
