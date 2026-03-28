# Setup Guide — Lead Generation Automation System

**Total setup time: ~20–30 minutes**

---

## Prerequisites

Before you start, make sure you have:

- [ ] n8n account (cloud or self-hosted) OR Make account
- [ ] GoHighLevel or Airtable account (for CRM)
- [ ] Twilio account with WhatsApp sandbox enabled (or GHL messaging)
- [ ] OpenAI or Claude API key (for lead qualification)

---

## Step 1: Import the Workflow

### In n8n:
1. Open your n8n dashboard
2. Click **"New Workflow"** → **"Import from JSON"**
3. Paste the contents of `workflow.json`
4. Click **Save**

### In Make:
1. Create a new Scenario
2. Click the three dots → **"Import Blueprint"**
3. Upload `workflow.json`

---

## Step 2: Connect Your Webhook

1. Click on the **"Lead Form Webhook"** node
2. Copy the webhook URL provided by n8n
3. Paste this URL into your landing page form (Typeform, GHL form, Webflow, etc.)
4. Set the form method to **POST**

---

## Step 3: Connect Your CRM

### GoHighLevel:
1. Go to GHL → Settings → API Keys → Create a new key
2. In the workflow, find the **"Create CRM Contact"** node
3. Replace `YOUR_GHL_API_KEY` with your key

### Airtable (alternative):
1. Get your Airtable API key from airtable.com/account
2. Update the node to use Airtable's API endpoint instead

---

## Step 4: Set Up WhatsApp Messaging

### Option A — Twilio:
1. Create a Twilio account at twilio.com
2. Enable WhatsApp Sandbox under Messaging → Try it Out → Send a WhatsApp message
3. Replace in the workflow:
   - `YOUR_ACCOUNT_SID` → your Twilio Account SID
   - `YOUR_AUTH_TOKEN` → your Twilio Auth Token
   - `YOUR_TWILIO_NUMBER` → your WhatsApp-enabled Twilio number

### Option B — GoHighLevel:
1. Enable GHL messaging in Settings → Phone Numbers
2. Replace the WhatsApp node with GHL's SMS/messaging action

---

## Step 5: Configure AI Qualification

1. Get a Claude API key at console.anthropic.com
2. In the **"AI Lead Qualification"** node, replace `YOUR_CLAUDE_API_KEY`
3. Adjust the qualification prompt if needed (e.g., add your specific ICP criteria)

---

## Step 6: Set Up Sales Notifications

1. Connect your Slack workspace to n8n (or replace with email/SMS notification)
2. Update the `#hot-leads` channel name to match your Slack setup
3. Alternatively, use GHL pipeline stages to route qualified leads

---

## Step 7: Test the Workflow

1. Activate the workflow in n8n
2. Submit a test form with fake lead data
3. Verify:
   - [ ] CRM contact created
   - [ ] WhatsApp message sent
   - [ ] AI qualification score returned
   - [ ] Correct routing (hot lead notification OR nurture tag)

---

## Customisation Tips

- **Change qualification threshold**: In the "Route by Score" node, adjust `7` to a higher or lower number
- **Add more follow-up days**: Duplicate the WhatsApp node and add a Wait node before it (set to 24h, 48h)
- **Add email follow-up**: Add an email node running parallel to WhatsApp
- **Industry-specific prompts**: Edit the AI qualification prompt to reflect your ideal client profile

---

## Troubleshooting

| Issue | Fix |
|-------|-----|
| Webhook not receiving data | Check form is submitting to correct URL with POST method |
| WhatsApp not sending | Verify Twilio sandbox is active and number is opted in |
| AI node failing | Check API key and that you have credits available |
| CRM not creating contacts | Verify API key permissions include contact creation |
