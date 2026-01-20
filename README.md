# cursor-guardrails

Cursor rules, prompts, and agent configurations for AI-assisted development that doesn't create tech debt.

## Why This Exists

I shipped 38K lines of 100% AI-generated code with zero rules. Ran SonarQube:

- Reliability: D
- 1,008 issues
- 4,500+ line controller
- 800+ line React component

These guardrails exist so you don't end up in the same place.

## Repository Structure

```
cursor-guardrails/
├── rules/                  # Distributable Cursor rules
│   └── quick-start.mdc     # Universal baseline
└── .cursorignore           # Ignore build artifacts, deps, lock files
```

## Quick Start

```bash
# Copy the baseline rules to your project
mkdir -p .cursor/rules
cp rules/quick-start.mdc .cursor/rules/
```

That's it. Cursor will automatically apply them.

## What's Included

### [Rules](rules/)

Drop-in `.mdc` files that constrain AI behavior:

| Rule | Description |
|------|-------------|
| [`quick-start.mdc`](rules/quick-start.mdc) | Universal baseline — works for any project |


### [.cursorignore](.cursorignore)

Prevents Cursor from wasting context on build artifacts, dependencies, and lock files. Copy to your project root.

See [rules/README.md](rules/README.md) for full details.

## Context

- [Post #1: Shipping fast with Cursor](https://www.linkedin.com/posts/alexreshetov_ai-cursor-activity-7416079511567585282-M7hH?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAFE-48BY1KEXKctINfd-90fkbTNhff-DaQ)
- [Post #2: SonarQube results](https://www.linkedin.com/posts/alexreshetov_ai-cursor-activity-7417451668398678017-vwTl?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAFE-48BY1KEXKctINfd-90fkbTNhff-DaQ)

## Contributing

Found a rule that helped you? Open a PR.

## License

MIT
