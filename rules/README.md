# Cursor Rules

Drop-in rules for improving AI-generated code quality with [Cursor](https://cursor.com).

## Installation

1. Copy the rule file(s) you want to your project's `.cursor/rules/` directory
2. That's it — Cursor will automatically apply them

```bash
# Example: Install quick-start rules
mkdir -p .cursor/rules
cp rules/quick-start.mdc .cursor/rules/
```

## Available Rules

| Rule | Description | Best For |
|------|-------------|----------|
| [`quick-start.mdc`](quick-start.mdc) | Universal baseline | Any project |

## Rule Details

### quick-start.mdc

The essential rules that work everywhere. Start here.

**Key limits:**
- Max 300 lines per file
- Max 20 lines per function
- Max 3 parameters per function

**Covers:**
- File structure & naming
- Documentation standards
- Error handling patterns
- Testing mindset
- Consistency guidelines


## Customization

Rules use the `.mdc` format with YAML frontmatter:

```yaml
---
description: What this rule does
globs: ["**/*"]        # Which files to apply to
alwaysApply: true      # Apply automatically
---

# Your rules here...
```

To customize, copy a rule and modify the limits/patterns to fit your needs.

## Combining Rules

You can use multiple rules together. Place all desired `.mdc` files in your `.cursor/rules/` directory. Framework-specific rules complement (not replace) the quick-start baseline.

**Recommended combinations:**
- General projects: `quick-start.mdc`
