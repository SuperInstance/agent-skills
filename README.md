# Agent Skills

**Smart applications any agent can install. Clone, configure, run. No fleet membership required.**

Every skill in this registry is a self-contained application that installs by cloning, gets better with feedback, and works without central authority. No monorepo. No workspace. No API gateways.

---

## The Idea

An agent has a job to do — monitoring a service, spreading information across the fleet, generating dream content for training. Instead of writing that capability from scratch, the agent clones a skill.

```
git clone https://github.com/SuperInstance/agent-skills.git ./skills
```

The skill comes with its own README, its own tests, its own configuration. The agent customizes it, runs it, and — if they choose — contributes improvements back.

---

## Available Skills

| Skill | What It Does |
|-------|-------------|
| **[fleet-murmur](https://github.com/SuperInstance/fleet-murmur)** | Fleet-wide murmur propagation — agents spread signals with controlled entropy |
| **[fleet-spread](https://github.com/SuperInstance/fleet-spread)** | Information dissemination — firehose or drip, topic-filtered |
| **[plato-client](https://github.com/SuperInstance/plato-client)** | PLATO tile client — read, write, subscribe to room updates |
| **[mermaid-engine](https://github.com/SuperInstance/mermaid-engine)** | Generate mermaid diagrams from structured data |
| **[dream-engine](https://github.com/SuperInstance/dream-engine)** | Pseudo-random content generation for synthetic training |
| **[swarm-monitor](https://github.com/SuperInstance/swarm-monitor)** | Fleet health monitoring and alerting |

## How Skills Get Better

Each skill has a `feedback/` directory. When an agent customizes a skill and improves it, the improvement can be contributed back. The skill doesn't have a single maintainer — it has a fleet of users who make it better through use.

---

## How It Fits

- **[agent-skills](https://github.com/SuperInstance/agent-skills)** — installable intelligence (this)
- **[agent-forge](https://github.com/SuperInstance/agent-forge)** — the framework that runs skills
- **[bootstrap-spark](https://github.com/SuperInstance/bootstrap-spark)** — onboarding that discovers installed skills
- **[baton-skill](https://github.com/SuperInstance/baton-skill)** — handoff that preserves skill state

---

## License

MIT
