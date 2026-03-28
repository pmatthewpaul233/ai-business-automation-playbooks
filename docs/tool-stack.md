# Tool Stack

Complete breakdown of every tool used across these automation systems — what it does, why we use it, and what it costs.

---

## Automation Platforms

### n8n
- **What it does**: Visual workflow automation — connects apps, runs logic, triggers actions
- **Why we use it**: Self-hostable (free), powerful, supports custom code, great for complex workflows
- **Cost**: Free (self-hosted on a $5–10/month VPS) or $20+/month cloud
- **Best for**: Technical users, complex workflows, cost-sensitive setups
- **Get it**: [n8n.io](https://n8n.io)

### Make (formerly Integromat)
- **What it does**: Same as n8n — visual automation builder
- **Why we use it**: Easier UI, great for non-technical users, huge app library
- **Cost**: Free tier (1,000 ops/month), paid from $9/month
- **Best for**: Non-technical users, simpler workflows
- **Get it**: [make.com](https://make.com)

---

## CRM & Marketing Automation

### GoHighLevel (GHL)
- **What it does**: All-in-one CRM, funnel builder, email/SMS marketing, calendar, pipeline management
- **Why we use it**: Replaces 5–10 tools, white-label for agencies, built-in automation
- **Cost**: $97–$297/month
- **Best for**: Agencies, coaches, businesses wanting one platform
- **Get it**: [gohighlevel.com](https://gohighlevel.com)

### Airtable
- **What it does**: Database + spreadsheet hybrid — great for storing leads, content, client data
- **Why we use it**: Free tier, flexible, easy to connect to automations
- **Cost**: Free tier available, paid from $10/user/month
- **Best for**: Lighter-weight CRM needs, content calendars, data storage
- **Get it**: [airtable.com](https://airtable.com)

---

## AI & Language Models

### Claude (Anthropic)
- **What it does**: AI text generation — content, lead qualification, scripts, copy
- **Why we use it**: Best reasoning and instruction-following, excellent for structured outputs
- **Cost**: API usage-based — roughly $0.003/1K tokens (Haiku), $0.015/1K (Sonnet)
- **Models used**:
  - `claude-haiku-4-5` — fast, cheap, great for lead scoring and classification
  - `claude-sonnet-4-6` — best quality for content generation
- **Get it**: [console.anthropic.com](https://console.anthropic.com)

### OpenAI (GPT-4o)
- **What it does**: Same category as Claude — AI text generation
- **Why we use it**: Alternative to Claude, widely integrated, strong for many tasks
- **Cost**: API usage-based
- **Get it**: [platform.openai.com](https://platform.openai.com)

---

## Messaging & Communication

### Twilio
- **What it does**: SMS and WhatsApp API — send and receive messages programmatically
- **Why we use it**: Reliable, well-documented, works globally
- **Cost**: ~$0.005–0.015 per message depending on country
- **Best for**: WhatsApp and SMS automation in n8n/Make workflows
- **Get it**: [twilio.com](https://twilio.com)

### GHL Messaging
- **What it does**: Built-in SMS/WhatsApp within GoHighLevel
- **Why we use it**: No separate tool needed if already on GHL
- **Cost**: Included in GHL subscription (usage costs apply)
- **Best for**: GHL users who want everything in one place

---

## Scheduling & Booking

### Calendly
- **What it does**: Automated scheduling — lets prospects book directly into your calendar
- **Why we use it**: Simple, reliable, free tier available, easy to integrate
- **Cost**: Free tier (1 event type), paid from $8/month
- **Get it**: [calendly.com](https://calendly.com)

---

## Content Scheduling

### Buffer
- **What it does**: Social media scheduling across Instagram, LinkedIn, Twitter/X, Facebook
- **Why we use it**: Simple, clean UI, good API for automation integration
- **Cost**: Free (3 channels), paid from $6/month
- **Get it**: [buffer.com](https://buffer.com)

### Later
- **What it does**: Visual social media planner, strong on Instagram
- **Cost**: Free tier, paid from $16.67/month
- **Get it**: [later.com](https://later.com)

---

## Recommended Minimum Stack (Budget-Conscious)

| Tool | Cost/month | Purpose |
|------|-----------|---------|
| n8n (self-hosted) | ~$5 (VPS) | Automation |
| Airtable | Free | CRM / Data |
| Claude API | ~$5–20 | AI generation |
| Twilio | Pay-per-use | Messaging |
| Calendly | Free | Booking |
| Buffer | Free | Scheduling |
| **Total** | **~$10–25** | Full stack |

---

## Agency Stack (Scale)

| Tool | Cost/month | Purpose |
|------|-----------|---------|
| GoHighLevel | $297 | CRM + Funnels + Messaging |
| n8n Cloud | $50 | Advanced automation |
| Claude API | $50–200 | AI at scale |
| **Total** | **~$400–550** | Multi-client operations |
