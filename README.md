<p align="center">
  <img src="assets/banner.svg" alt="nobodybuilt — find what nobody has built yet" width="100%"/>
</p>

<p align="center">
  <a href="https://github.com/KeWang0622/nobodybuilt/stargazers"><img src="https://img.shields.io/github/stars/KeWang0622/nobodybuilt?style=for-the-badge&color=ff6b6b&labelColor=1a1a2e" alt="Stars"></a>
  <a href="https://github.com/KeWang0622/nobodybuilt/network/members"><img src="https://img.shields.io/github/forks/KeWang0622/nobodybuilt?style=for-the-badge&color=ffa502&labelColor=1a1a2e" alt="Forks"></a>
  <a href="LICENSE"><img src="https://img.shields.io/github/license/KeWang0622/nobodybuilt?style=for-the-badge&color=ff4757&labelColor=1a1a2e" alt="License"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Claude_Code-supported-blue?style=flat-square&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIxMCIgZmlsbD0id2hpdGUiLz48L3N2Zz4=" alt="Claude Code"/>
  <img src="https://img.shields.io/badge/Cursor-supported-blue?style=flat-square" alt="Cursor"/>
  <img src="https://img.shields.io/badge/Codex_CLI-supported-blue?style=flat-square" alt="Codex"/>
  <img src="https://img.shields.io/badge/Gemini_CLI-supported-blue?style=flat-square" alt="Gemini CLI"/>
  <img src="https://img.shields.io/badge/OpenClaw-supported-blue?style=flat-square" alt="OpenClaw"/>
  <img src="https://img.shields.io/badge/Windsurf-supported-blue?style=flat-square" alt="Windsurf"/>
  <img src="https://img.shields.io/badge/Aider-supported-blue?style=flat-square" alt="Aider"/>
</p>

<h3 align="center">Stop building the 50th todo app. Find the tool <i>nobody</i> has built yet.</h3>

---

**nobodybuilt** is an AI agent skill that searches GitHub, Product Hunt, Reddit, npm, app stores, and AI tool directories to find **genuinely unexplored ideas** with viral potential — then generates a complete, publish-ready project with code, README, and launch strategy.

> **"I can't believe nobody built this yet."** That's the reaction you want. This skill finds those ideas systematically.

## Quick Start

```bash
# Claude Code / OpenClaw — one command, done
cp SKILL.md ~/.claude/skills/nobodybuilt.md

# Or curl it directly
curl -sL https://raw.githubusercontent.com/KeWang0622/nobodybuilt/main/SKILL.md \
  -o ~/.claude/skills/nobodybuilt.md
```

For other agents (Cursor, Codex, Gemini CLI, Windsurf, Aider), paste the SKILL.md content into your agent's skills or system prompt configuration.

## Usage

```
# Guided — tell it what excites you
Use nobodybuilt. I'm into cooking and meal prep.

# Auto-discovery — let it surprise you
Use nobodybuilt. Surprise me with the most viral unexplored idea right now.

# Niche-specific
Use nobodybuilt. Find a tool for Pokemon fans that would blow up on Twitter.

# Platform-specific
Use nobodybuilt. Find me a Chrome extension idea that doesn't exist yet.

# Iterate on results
Combine idea 1 and 3.  /  More like idea 2.  /  Same idea but as a CLI.
```

## How It Works

Most "idea generators" just brainstorm. **nobodybuilt** validates.

```
You say "cooking"
        │
        ▼
┌─────────────────────────────────────────────────────────────┐
│  PHASE 1: Creative Ideation                                 │
│  5 frameworks: Mashup, Annoyance Autopsy, What-If,          │
│  Audience Flip, Format Shift → 15-20 raw ideas              │
└──────────────────────────┬──────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│  PHASE 2: Deep Research                                     │
│  GitHub, Product Hunt, Reddit, npm, Chrome Web Store,       │
│  AI directories, niche platforms → map what exists           │
└──────────────────────────┬──────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│  PHASE 3: Validate & Score                                  │
│  Demand validation (Reddit wishlists, manual workarounds)   │
│  Anti-pattern filter (kills "dashboard for X", AI wrappers) │
│  9-factor scoring with calibrated examples → Top 3          │
└──────────────────────────┬──────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│  PHASE 4: Build the Winner                                  │
│  Name (collision-checked) + code + viral README +           │
│  launch strategy with draft posts for Reddit, HN, X         │
└─────────────────────────────────────────────────────────────┘
```

## What You Get

| Output | Details |
|--------|---------|
| **3 scored ideas** | Ranked by 9 viral factors (190-point scale), with search evidence proving the gap |
| **Validated name** | Collision-checked against GitHub, npm, and web — confirmed available |
| **Complete code** | Working v1 — SKILL.md, CLI, extension, or web app. Not stubs. Runnable. |
| **Viral README** | Hook-first, one-command install, 3 usage examples, "why this exists" |
| **Launch strategy** | Draft posts for Reddit/HN/X, directory submissions, timing advice |

## Scoring System

Every idea is scored on 9 weighted factors. Each score has calibrated benchmarks — no guessing.

| Factor | Weight | 10 = | 1 = |
|--------|--------|------|-----|
| **Pain Point** | 3x | Reddit threads with 500+ upvotes about this problem | "Nice to have" nobody complains about |
| **Blue Ocean** | 3x | Zero results on GitHub, PH, any directory | Multiple well-maintained tools with active communities |
| **"I Need This"** | 3x | You stop researching to think "wait, I want this" | You have to explain why anyone would want it |
| **Instant Value** | 2x | `npx tool` and it works. No config, no signup. | Needs accounts, API keys, database setup |
| **Catchy Name** | 2x | The name IS the pitch ("Shazam", "Tinder") | Generic ("my-tool", "utils") |
| **Trend Alignment** | 2x | Enabled by something launched this month | Could've been built 5 years ago |
| **Shareability** | 2x | Output so good people MUST screenshot it | Correct but boring output nobody shares |
| **Moat** | 1x | Network effects, unique dataset, "standard" status | Pure code anyone could clone in a weekend |
| **Feasibility** | 1x | Single file, no deps, 2-hour build | Needs infra, multiple services, complex integrations |

**Max score: 190.** Top 3 presented with evidence.

## Anti-Patterns Filter

Ideas get killed before you see them if they match these traps:

| Anti-Pattern | Why It Dies |
|-------------|-------------|
| "Dashboard for X" | No wow moment, requires integration, competes with everything |
| "AI wrapper, no angle" | Everyone has this idea. Must add unique data/workflow/output. |
| "Yet another todo app" | 10,000+ exist. Need genuinely novel angle. |
| "Requires behavior change" | Tools needing new daily habits almost always fail |
| "Needs large user base" | Network effects impossible to bootstrap solo |
| "Too broad to be catchy" | "Productivity toolkit" = nothing. "Git history to resume" = shareable. |

## Example Output

```
### 1. fridge-to-feast
> Snap your fridge, get a week of meals with a grocery list

Scores: Pain 8 x Blue Ocean 9 x Need 9 x Instant 7 x Name 8 x Trend 8 x Share 9 x Moat 5 x Build 6 = 168/190

The insight: Meal planning apps exist. Recipe apps exist. But nothing takes
a fridge photo → generates a WEEK of meals → outputs a shopping list grouped
by store aisle. The closest tools require manual ingredient input.

Evidence: Searched GitHub for "fridge meal planner", "fridge to recipe",
"photo grocery list" — found 3 repos, all abandoned (last commit 2+ years ago).
Reddit r/mealprep has weekly "I wish there was an app that..." threads.

The share moment: Side-by-side of messy fridge photo → beautiful weekly meal
calendar with nutritional breakdown. Screenshot-bait.
```

Then it generates the complete project: SKILL.md, README, code, and a launch plan with draft Reddit/HN/X posts.

## Creative Ideation Methods

Not just gap-searching — active idea generation using 5 proven frameworks:

| Method | How It Works | Example |
|--------|-------------|---------|
| **Mashup** | Combine two unrelated domains | Duolingo = language + gaming |
| **Annoyance Autopsy** | List 10 specific frustrations, build the fix | "I hate manually copying recipe ingredients to my shopping list" |
| **"What If"** | "What if [impossible thing] was [simple input]?" | "What if you could mass-unfollow inactive Twitter accounts in one click?" |
| **Audience Flip** | Developer tool → make it for non-devs | GitHub contribution graph → but for gym workouts |
| **Format Shift** | Web app → CLI / paid SaaS → open source single-file | Canva → but as a CLI for developers |

## Iteration

Don't like the results? Keep going:

- **"More like this"** — 3 more ideas in the same direction
- **"Combine 1 and 3"** — Merge ideas into a hybrid
- **"Same idea, different platform"** — CLI to extension, skill to web app
- **"Pivot"** — Same domain, completely different angle
- **"Go deeper"** — Second research pass with refined queries

<details>
<summary><b>Full Feature List</b></summary>

### Research Sources
- GitHub repos, stars, forks, awesome-lists, topics
- Product Hunt launches and traction data
- Chrome Web Store and extension marketplaces
- npm, PyPI, crates.io packages
- Reddit wishlists, X complaints, HN gaps
- AI tool directories (ClawHub, skills.sh, GPT Store, FutureTools)
- Niche platforms (itch.io, Figma Community, Splice, etc.)

### Ideation Techniques
- Mashup method (cross-domain combination)
- Annoyance Autopsy (frustration-first ideation)
- "What If" method (impossibility framing)
- Audience Flip (re-target existing tools)
- Format Shift (platform/format translation)
- Cross-pollination scan (adjacent domain analysis)

### Validation
- Demand signals (Reddit/X/HN "I wish..." searches)
- Manual workaround detection
- Adjacent tool popularity as demand proxy
- Search volume inference
- Collision detection (GitHub, npm, web)

### Output Formats
- AI agent skills (SKILL.md)
- CLI tools (Node.js, Python, Rust)
- Browser extensions
- Web apps
- Discord/Slack/Telegram bots
- Any platform that fits the idea best

### Launch Strategy
- Draft posts for Reddit, HN, X (platform-specific framing)
- Money screenshot specification
- Awesome-list and directory submission targets
- Timing optimization
- Follow-up content plan (blog, video, thread)

</details>

## Why This Exists

There are millions of repos on GitHub. Most are clones. Meanwhile, entire domains have **zero good tools** and massive unmet demand sitting in Reddit threads and unanswered tweets.

The most successful tools follow the same pattern: **be first in a real category, not 50th in a crowded one.** This skill systematically finds those categories before anyone else does.

## Compatible With

Any AI coding agent that supports skill/instruction files:

| Agent | Install Method |
|-------|---------------|
| **Claude Code** | `cp SKILL.md ~/.claude/skills/nobodybuilt.md` |
| **OpenClaw** | `cp SKILL.md ~/.claude/skills/nobodybuilt.md` |
| **Cursor** | Add to `.cursor/rules/` or paste into system prompt |
| **Codex CLI** | Add to agent instructions |
| **Gemini CLI** | Add to agent instructions |
| **Windsurf** | Add to Cascade rules |
| **Aider** | Add to `.aider/prompts/` |
| **Any AI chat** | Paste SKILL.md content as system prompt |

## Star History

<p align="center">
  <a href="https://star-history.com/#KeWang0622/nobodybuilt&Date">
    <img src="https://api.star-history.com/svg?repos=KeWang0622/nobodybuilt&type=Date" alt="Star History Chart" width="600"/>
  </a>
</p>

## Contributing

Found an idea that nobodybuilt helped you discover? Open a PR to add it to the [Hall of Fame](https://github.com/KeWang0622/nobodybuilt/issues/1)!

Ideas for improving the skill itself are welcome — open an issue or PR.

## License

[MIT](LICENSE) — do whatever you want with it.

---

<p align="center">
  <b>If this helped you find something worth building, <a href="https://github.com/KeWang0622/nobodybuilt">star the repo</a></b> so others can find it too.
</p>
