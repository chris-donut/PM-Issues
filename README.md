# PM Issues

Product management tools and workflows for the Donut team.

## PM Engine v2.3

A Claude Code skill that enforces disciplined product management with:
- **4-Input Gate**: User feedback, product state, success metric, OKR
- **5+ Options**: Ranked by P(conversion)
- **GitHub/Screenshot Support**: Paste links or drag screenshots

### Quick Install

```bash
# One-liner install
curl -o ~/.claude/commands/pm.md https://raw.githubusercontent.com/chris-donut/PM-Issues/main/pm-engine/pm.md

# Or symlink (for auto-updates)
git clone https://github.com/chris-donut/PM-Issues.git
ln -sf $(pwd)/PM-Issues/pm-engine/pm.md ~/.claude/commands/pm.md
```

### Usage

```
/pm
```

Then provide:
1. **User Feedback**: What problem are we solving?
2. **Product State**: GitHub link, screenshot, or file path
3. **Success Metric**: What metric defines success?
4. **OKR Objective**: Which team objective does this support?

See [pm-engine/README.md](./pm-engine/README.md) for full documentation.

## Repository Contents

```
PM-Issues/
├── README.md
├── PM_ENGINE_v2.1.md      # Original prompt (archived)
├── pm-engine/
│   ├── pm.md              # Claude Code skill (latest)
│   └── README.md          # Installation & usage docs
└── ...
```

## Contributing

Open issues or PRs for PM workflow improvements.
