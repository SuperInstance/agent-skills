# Agent Skill Specification v0.1

A skill is an installable, self-contained tool that agents (and humans) can drop into any project.

## Required Files

- `CHARTER.md` — Purpose, philosophy, and identity
- `BOOTCAMP.md` — 5-minute onboarding: clone, configure, run
- `package.json` — Dependencies and scripts (or equivalent for non-JS)
- `README.md` — What it does, how to install, how to use

## Required Properties

1. **Installable by clone**: `git clone <url> .skill-name`
2. **Configurable by file**: Edit one config file, no CLI wizardry
3. **Budget-agnostic**: Works with any API budget (including zero/local)
4. **Git-native output**: Results are files, runs are commits
5. **Self-documenting**: README + BOOTCAMP are sufficient to use it
6. **Zero side effects**: Doesn't touch parent project files without explicit config

## Optional but Recommended

- `src/` with typed source code
- `tests/` with passing test suite
- `examples/` with real usage examples
- `config.example.yaml` with documented defaults
- `message-in-a-bottle/` for fleet integration

## Feedback Mechanism

Every skill should have a way to receive feedback:
- GitHub Issues on the skill repo
- Pull requests with improvements
- Usage telemetry (opt-in, git-native — commit counts, run logs)

The skill gets better because agents report what worked and what didn't. This IS the improvement cycle.

## Versioning

Skills follow semver but with a twist:
- **Patch**: Bug fixes, no behavior change
- **Minor**: New features, backward compatible
- **Major**: Breaking changes to config or output format

Agents should pin to major version and accept minor/patch updates.
