# 📦 Agent Skills — Installable Intelligence

Smart applications that any agent (or human) can drop into a project, customize, and improve through use.

## The Idea

Every tool in this registry is a **git-agent skill** — a self-contained application that:

1. **Installs by cloning** — `git clone` into your project, configure, run
2. **Gets better with feedback** — the agent creator's feedback improves the skill for everyone
3. **Works standalone** — no fleet membership required, no central authority
4. **Composes freely** — pipe murmur output into spreader, spreader into dream-engine

## Available Skills

| Skill | What It Does | Install |
|-------|-------------|---------|
| 🫧 **murmur** | All-night thinking agent. Point at a topic, let it think. Budget-agnostic. | `git clone https://github.com/SuperInstance/murmur-agent.git .murmur` |
| 🌊 **spreader** | One idea, many perspectives. Fans out across specialist views with synthesis. | `git clone https://github.com/SuperInstance/spreader-agent.git .spreader` |
| 🛶 **dream-engine** | Overnight content generation. Schedule narratives while your computer sleeps. | `git clone https://github.com/SuperInstance/dream-engine.git .dream-engine` |
| ✨ **luciddreamer** | Autonomous 30-min content cycle. Compounding knowledge graph, forever stream. | `git clone https://github.com/SuperInstance/luciddreamer-ai.git .luciddreamer` |

## How Skills Work

```
Your Project
├── .murmur/          ← Think about a topic overnight
├── .spreader/        ← Spread an idea across perspectives
├── .dream-engine/    ← Generate scheduled content
└── .luciddreamer/    ← Autonomous content stream
```

Each skill is independent. Install one or all. They don't fight.

## The Feedback Loop

```
Agent uses skill → discovers rough edges → feedback to skill repo
    → skill improves → every agent benefits
```

This is the key insight: **the agent creator's feedback IS the product improvement cycle.** Not bug reports from users — actual usage feedback from agents who push the tools to their limits.

## Building a New Skill

1. Create a repo with `CHARTER.md` (purpose) and `BOOTCAMP.md` (how to use)
2. Build the core engine — no external dependencies that aren't optional
3. Make it budget-agnostic: works with any API budget or local hardware
4. Git-native output: every result is a file, every run is a commit
5. Add to this registry with a one-line install command

## Design Principles

- **Tolerant of silence**: If the API is down, wait. If the budget is empty, pause. Never die angry.
- **Whatever it gets done is great**: 10 calls/day or 10,000 — both produce value.
- **The repo IS the interface**: No dashboards. Files and git commits.
- **Fork-first**: Every fork is independent. No central authority.
- **Composable**: Output of one skill is input to another.

## Composability Examples

```bash
# Think about a topic, then spread the insights
cd .murmur && npm run think -- --topic "event-driven architecture"
cd ../.spreader && npm run spread -- --idea "$(cat ../.murmur/murmur-output/SUMMARY.md)"

# Dream about whatever murmur found
cd .dream-engine && configure with murmur-output as context

# Let luciddreamer run forever, spreading the best insights every 30 min
# (pipe luciddreamer output into spreader for analysis)
```

## For Agent Builders

If you're building agents (human or AI), these skills are your toolkit:
- **Murmur** for deep research and exploration
- **Spreader** for decision-making and perspective-gathering
- **Dream-engine** for scheduled content production
- **Luciddreamer** for autonomous, compounding knowledge streams

Each one is a git-agent that lives in your project and works while you do other things.

## License

All skills are MIT licensed unless otherwise noted in their individual repos.
