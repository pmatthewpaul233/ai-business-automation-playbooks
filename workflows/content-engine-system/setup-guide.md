# Setup Guide — Content Engine Automation System

**Total setup time: ~25–35 minutes**

---

## Prerequisites

- [ ] n8n or Make account
- [ ] Airtable account (free tier works)
- [ ] Claude or OpenAI API key
- [ ] Buffer or Later account (optional, for scheduling)

---

## Step 1: Set Up Your Airtable Base

Create a new Airtable base with two tables:

### Table 1: Content Briefs
| Field Name | Type |
|-----------|------|
| Topic | Single line text |
| Target Audience | Single line text |
| Problem | Single line text |
| Tone | Single select (Conversational, Professional, Direct) |
| CTA | Single line text |
| Status | Single select (Pending, Ready to Generate, Done) |

### Table 2: Content Calendar
| Field Name | Type |
|-----------|------|
| Topic | Single line text |
| Hooks | Long text |
| Reel Script | Long text |
| LinkedIn Post | Long text |
| Status | Single select (Draft, Approved, Scheduled, Published) |
| Generated At | Date |
| Publish Date | Date |

---

## Step 2: Import the Workflow

1. Open n8n → New Workflow → Import from JSON
2. Paste `workflow.json` contents
3. Save the workflow

---

## Step 3: Connect Airtable

1. In n8n, go to Credentials → Add New → Airtable
2. Enter your Airtable API key (get it from airtable.com/account)
3. Update both Airtable nodes with your Base ID:
   - Go to your Airtable base → Help → API documentation → copy the Base ID

---

## Step 4: Connect Claude API

1. Get API key from console.anthropic.com
2. In each AI generation node, replace `YOUR_CLAUDE_API_KEY`
3. Alternatively, switch to OpenAI by changing the URL to `api.openai.com/v1/chat/completions` and updating the request format

---

## Step 5: Test It

1. Add a row to your "Content Briefs" table
2. Set Status to "Ready to Generate"
3. Activate the workflow
4. Check "Content Calendar" table — content should appear within 30 seconds

---

## Step 6: Connect Scheduling (Optional)

1. Add a Buffer node after "Save to Content Calendar"
2. Connect your Buffer account
3. Map the content fields to the correct platforms
4. Set your publishing schedule

---

## Customisation Tips

- **Add more platforms**: Duplicate the generation nodes for TikTok scripts, Twitter threads, email newsletters
- **Client management**: Add a "Client" field to both tables to manage multiple clients
- **Approval workflow**: Change Status to "Pending Approval" instead of "Draft" and add a Slack notification to your review channel
- **Batch generation**: Change the trigger to run weekly and generate a full week of content at once
