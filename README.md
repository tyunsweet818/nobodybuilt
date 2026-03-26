# skills-maker

**Stop building tools nobody uses. Find the ones nobody has built yet.**

skills-maker searches the entire landscape — GitHub, Product Hunt, app stores, Reddit wishlists, trending topics — to find **genuinely unexplored ideas** with viral potential, then generates a complete, publish-ready project blueprint.

Works with any AI coding agent: Claude Code, Codex, Cursor, Gemini CLI, OpenClaw, or anything that supports skill files.

## The Problem

There are millions of tools and repos on GitHub. Most new ones are clones of what already exists. Meanwhile, entire domains have **zero good tools** and massive unmet demand sitting in Reddit threads and unanswered "is there a tool that..." tweets.

This skill finds those gaps for you.

## What It Does

1. **Asks you a few optional questions** (or skip for auto-discovery)
   - Domain interest (cooking? Pokemon? fitness? "surprise me")
   - Target audience (devs, creators, students, parents, "anyone")
   - Platform preference (GitHub repo, Chrome extension, web app, bot, CLI, skill file, "whatever fits")

2. **Actively generates ideas using creative frameworks**
   - Mashup method (combine two unrelated domains — highest hit rate for viral ideas)
   - Annoyance autopsy (find specific frustrations, build the fix)
   - Audience flip (take a dev tool → make it for non-technical users)
   - Format shift (web app → CLI, paid SaaS → open-source single-file alternative)
   - "What if" method (make the impossible sound simple)

3. **Deep-searches the entire ecosystem**
   - GitHub repos, stars, forks, awesome-lists
   - Product Hunt, Chrome Web Store, npm/PyPI
   - Reddit wishlists, X complaints, HN "Show HN" gaps
   - AI tool directories, MCP servers, GPT Store
   - Niche-specific platforms (itch.io, Figma Community, etc.)

4. **Validates demand before recommending anything**
   - Searches for "is there a tool that..." and "I wish someone would build..." posts
   - Checks for manual workarounds (spreadsheets, copy-paste workflows)
   - Looks at adjacent tool popularity as a demand proxy
   - Rates evidence: Strong / Moderate / Weak — drops ideas with no demand signal

5. **Scores ideas on 9 viral factors with calibrated examples**
   - Pain point severity (3x weight)
   - Blue ocean score (3x) — nobody has built it (backed by search evidence)
   - "I need this" factor (3x)
   - Shareability, catchy name, trend alignment, moat
   - Build feasibility — can you ship v1 in a weekend?
   - Each score includes calibration: what a 10, 5, and 1 actually look like

6. **Checks for anti-patterns before recommending**
   - Filters out "dashboard for X", "AI wrapper with no angle", "yet another todo app"
   - Kills ideas that require behavior change, large user bases, or are too broad to be catchy

7. **Generates a complete project blueprint**
   - Name with collision detection (checks GitHub, npm, web for conflicts)
   - Optimized one-liner
   - Full working code (skill file, CLI, extension, or web app)
   - Viral-optimized README
   - 5-step launch strategy with draft posts for Reddit, HN, and X

8. **Supports iteration**
   - "More like this" — 3 more ideas in the same direction
   - "Combine X and Y" — merge two ideas into a hybrid
   - "Same idea, different platform" — redesign for a different form factor
   - "Pivot" — same domain, completely different angle

## Install

Copy the skill file to your agent's skills directory:

```bash
# Claude Code / OpenClaw
cp SKILL.md .claude/skills/skills-maker.md

# Or from anywhere
curl -o .claude/skills/skills-maker.md https://raw.githubusercontent.com/YOUR_USERNAME/skills-maker/main/SKILL.md
```

For other agents, add the SKILL.md content to your agent's system prompt or skills configuration.

## Usage

**Guided mode:**
```
I want to use skills-maker. I'm interested in cooking and meal prep.
```

**Auto-discovery mode:**
```
Use skills-maker. Surprise me — find the most viral unexplored tool idea right now.
```

**Specific niche:**
```
Use skills-maker. I want something for Pokemon fans that would blow up on Twitter.
```

**Platform-specific:**
```
Use skills-maker. Find me a Chrome extension idea that doesn't exist yet.
```

**Iterate after results:**
```
Combine idea 1 and 3. / More like idea 2. / Same idea but as a CLI.
```

## Example Output

The skill researches, validates, scores, and presents ideas like:

| Idea | Blue Ocean | Pain Point | Demand | Total Score |
|------|-----------|------------|--------|-------------|
| **fridge-to-feast** — Snap your fridge, get a week of meals with shopping list | 9/10 | 8/10 | Strong | 168/190 |
| **pokebuild** — Generate competitive Pokemon teams from your catches | 10/10 | 7/10 | Moderate | 155/190 |
| **plant-911** — Describe what's wrong with your plant, get a rescue plan | 9/10 | 8/10 | Strong | 161/190 |

Then generates the complete project — code, README, and launch plan — for whichever you pick.

## How Scoring Works

| Factor | Weight | What it measures |
|--------|--------|-----------------|
| Pain Point | 3x | People actively complain about this |
| Blue Ocean | 3x | Nobody has built it (0 existing = 10) |
| "I Need This" | 3x | Instant reaction: "this doesn't exist?!" |
| Useful in 60s | 2x | Value on first use |
| Catchy Name | 2x | Memorable, creates desire |
| Trend Alignment | 2x | Rides a current wave |
| Shareability | 2x | People would screenshot and post it |
| Moat | 1x | Hard to replicate once built |
| Build Feasibility | 1x | Shippable in a weekend |

## Why This Works

The most successful tools follow the same pattern: **be first in a real category, not 50th in a crowded one.**

The top GitHub repos aren't better code reviewers or yet another todo app. They're the first tool to nail an underserved niche. This skill systematically finds those niches before anyone else does.

## Compatible With

Any AI coding agent that supports skill/instruction files:
- Claude Code
- Codex
- Cursor
- Gemini CLI
- OpenClaw
- Windsurf
- Aider
- Or paste the skill content into any AI chat

## License

MIT
