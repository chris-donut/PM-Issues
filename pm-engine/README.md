# PM Engine v2.3

A scope-constraining PM skill for Claude Code that enforces disciplined product management.

## Features

- **4-Input Gate**: Requires user feedback, product state, success metric, and OKR before work begins
- **5+ Options**: Always enumerates 5+ approaches ranked by conversion probability
- **GitHub/Screenshot Support**: Accepts GitHub links, screenshots, Figma URLs, or file paths as product state
- **OKR Alignment**: Every feature tied to company objectives

## Quick Install (30 seconds)

### Option 1: Symlink (recommended)

```bash
# Clone the repo
git clone https://github.com/chris-donut/PM-Issues.git

# Create symlink to your Claude commands
ln -sf $(pwd)/PM-Issues/pm-engine/pm.md ~/.claude/commands/pm.md
```

### Option 2: Direct copy

```bash
# One-liner
curl -o ~/.claude/commands/pm.md https://raw.githubusercontent.com/chris-donut/PM-Issues/main/pm-engine/pm.md
```

### Option 3: Manual

1. Copy `pm.md` to `~/.claude/commands/pm.md`
2. Done!

## Usage

In any Claude Code session:

```
/pm
```

Claude will request 4 inputs:

| Input | What to provide |
|-------|-----------------|
| User Feedback | Problem description, pain points |
| Product State | GitHub link, screenshot, or file path |
| Success Metric | Quantifiable goal (e.g., "conversion rate") |
| OKR Objective | Which team OKR this supports |

## Example

```
/pm

User: "Onboarding has high drop-off"
Product State: github.com/donut/app/blob/main/src/onboarding/flow.tsx
Success Metric: P(first AI trade suggestion accepted)
OKR: 首屏30秒用户知道能交易什么
```

Claude will:
1. Read the GitHub file
2. Analyze gap between current and desired state
3. Generate 5+ options ranked by P(conversion)
4. Produce executable spec

## Changelog

- **v2.3**: Added 4-input gate (user feedback, product state, success metric, OKR), GitHub/Figma URL support
- **v2.2**: Increased to 5+ options with P(conversion) ranking
- **v2.1**: Initial release with dual-input gate

## License

MIT
