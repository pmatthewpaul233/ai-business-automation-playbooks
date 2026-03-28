# Contributing to AI Business Automation Playbooks

Thank you for your interest in contributing! This project is focused on making AI automation accessible to non-technical business owners.

## What We're Looking For

- New workflow systems for common business use cases
- Improvements to existing setup guides (clarity, accuracy)
- Additional prompt templates and scripts
- Translations or adaptations for specific industries
- Bug fixes in workflow JSON files

## How to Contribute

1. **Fork** this repository
2. **Create a branch**: `git checkout -b feature/your-workflow-name`
3. **Add your contribution** following the folder structure below
4. **Submit a Pull Request** with a clear description of what you've added and why it's useful

## Workflow Submission Format

Each workflow should include:

```
/workflows/your-workflow-name/
  │── overview.md       # What it does, who it's for, outcomes
  │── workflow.json     # Exported workflow (n8n, Make, or GHL)
  │── setup-guide.md    # Step-by-step instructions
```

## Quality Standards

- **Clarity over complexity** — guides should be usable by non-technical people
- **Real-world tested** — ideally something you've deployed in an actual business
- **Tool-agnostic where possible** — note which tools are required vs optional
- **No proprietary credentials** — remove all API keys, tokens, and personal data before submitting

## Questions?

Open an issue with the label `question` and we'll get back to you.
