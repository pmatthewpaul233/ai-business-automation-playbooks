# How to Use This Repo

This guide helps you get the most out of these automation playbooks — whether you're implementing for your own business or deploying for clients.

---

## Who This Is For

This repo is built for **systems thinkers** — people who want to move fast, implement real solutions, and not start from scratch every time.

You'll get the most value if you're:
- An agency owner deploying automations for clients
- A coach or consultant building your own acquisition system
- A business operator removing bottlenecks from your sales/marketing process
- A marketer who wants to leverage AI without depending on developers

---

## How the Repo Is Organised

```
/workflows      → Complete automation systems (each with overview, JSON, setup guide)
/templates      → Reusable scripts, copy, and prompts
/docs           → Supporting documentation (use cases, tool stack, this guide)
/assets         → Video walkthroughs and visual resources
```

Start with `/workflows` — pick the system most relevant to your current need.

---

## Step-by-Step: How to Implement a Workflow

### 1. Read the Overview First
Every workflow has an `overview.md` that explains:
- What problem it solves
- Who it's for
- What tools you need
- Expected outcomes

**Don't skip this.** It takes 3 minutes and saves hours of confusion.

### 2. Check Your Tool Stack
Compare the required tools in the overview against what you already have. See [docs/tool-stack.md](tool-stack.md) for setup guides and costs.

### 3. Follow the Setup Guide
Each workflow has a `setup-guide.md` with step-by-step instructions. Follow it in order — each step builds on the previous one.

### 4. Import the Workflow JSON
The `workflow.json` file is a pre-built automation you can import directly into n8n or Make. You'll then connect your own credentials and customise for your context.

### 5. Test Before Going Live
Always run a test with fake data before activating for real leads. Each setup guide includes a testing checklist.

### 6. Customise and Iterate
These are starting points, not finished products. Adapt:
- The AI prompts to match your ICP
- The messaging to match your voice
- The routing logic to match your sales process

---

## How to Choose Which Workflow to Start With

| Your Priority | Start Here |
|--------------|-----------|
| Getting more booked calls | Appointment Booking System |
| Following up with leads faster | Lead Generation System |
| Creating content without spending hours | Content Engine System |
| All of the above | Lead Gen → Content Engine → Booking |

---

## Using the Templates

The `/templates` folder contains copy and scripts you can use independently of the workflows:

- **WhatsApp Sequences** → load into GHL, Twilio, or any messaging tool
- **Ad Copy Examples** → use directly in Meta Ads Manager or adapt for your niche
- **Funnel Scripts** → use for VSLs, opt-in pages, and sales calls

---

## Contributing Your Own Workflows

If you've built something that works and want to share it, see [CONTRIBUTING.md](../CONTRIBUTING.md).

The best contributions are real systems you've deployed — even simple ones. Clarity matters more than complexity.

---

## Getting Help

- Open an **Issue** if something doesn't work or is unclear
- Use the `question` label for general questions
- Use the `bug` label if a workflow JSON has errors
