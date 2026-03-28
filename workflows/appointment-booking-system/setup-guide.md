# Setup Guide — Appointment Booking Automation System

**Total setup time: ~30–40 minutes**

---

## Prerequisites

- [ ] n8n or Make account
- [ ] Calendly (free) or GoHighLevel Calendar
- [ ] GoHighLevel account (for CRM) or Airtable
- [ ] Claude or OpenAI API key
- [ ] Twilio or GHL for WhatsApp/SMS

---

## Step 1: Set Up Your Booking Calendar

### Calendly (Free):
1. Create account at calendly.com
2. Set up a 30-minute "Strategy Call" event type
3. Connect your Google or Outlook calendar
4. Copy your booking link (e.g., `calendly.com/yourname/strategy-call`)
5. In the workflow, replace `YOUR_CALENDLY_LINK` with this URL

### GoHighLevel Calendar:
1. Go to GHL → Calendars → Create Calendar
2. Set availability and call duration
3. Copy the calendar booking link

---

## Step 2: Connect Your Funnel

1. In the workflow, click the **"Funnel Lead Capture"** webhook node
2. Copy the webhook URL
3. Paste it into your funnel tool (ClickFunnels, GHL funnel, Webflow, etc.)
4. Map these fields in your form:
   - `name` → First name
   - `email` → Email address
   - `phone` → Phone number (include country code)
   - Any other qualifying fields (business type, revenue, goals)

---

## Step 3: Configure AI Scoring

The AI scorer evaluates leads based on the data submitted in your form. To improve accuracy:

1. Open the **"AI Lead Scoring"** node
2. Customise the prompt to reflect your ideal client:

```
Score this lead 1-10 for booking a [YOUR OFFER] call.
My ideal client: [describe your ICP - industry, revenue, pain point]
Red flags (score low): [e.g., "no budget", "just starting out", "competitor"]
Green flags (score high): [e.g., "established business", "specific pain point", "ready to invest"]
```

3. Adjust the routing threshold in "Qualify Lead" node (default: 7/10)

---

## Step 4: Set Up WhatsApp/SMS Booking Message

Replace in the **"Send Booking Link"** node:
- `YOUR_ACCOUNT_SID` — Twilio Account SID
- `YOUR_TWILIO_NUMBER` — WhatsApp-enabled number
- `YOUR_CALENDLY_LINK` — Your booking page URL

Customise the message to match your voice:
```
"Hey {name}! Loved what you shared. You're exactly who I work with.
Here's my calendar — pick a time and let's talk: {booking_link}

P.S. Spots this week are limited."
```

---

## Step 5: Pre-Call Reminder Sequence

Add these nodes after the booking confirmation webhook (set up in Calendly):

1. **Booking confirmed webhook** → triggers when someone books
2. **Wait node** → set to 24 hours before call time
3. **WhatsApp reminder** → "Hey {name}, just a reminder — we're talking tomorrow at {time}. Looking forward to it!"
4. **Wait node** → set to 1 hour before call time
5. **Final reminder** → "We're on in 1 hour! Here's the Zoom link: {link}"

---

## Step 6: Test End-to-End

1. Activate the workflow
2. Submit a test form with high-quality fake data
3. Verify booking link is sent via WhatsApp
4. Check CRM for contact with correct tags
5. Verify Slack notification fires
6. Submit another test with low-quality data — verify it goes to nurture instead

---

## Troubleshooting

| Issue | Fix |
|-------|-----|
| AI scoring always returns same score | Check that form fields are correctly mapped in the JSON payload |
| Booking link not sent | Verify Twilio WhatsApp sandbox is active |
| Low-score leads not going to nurture | Check the If node threshold value |
| CRM not updating | Verify GHL API key and permissions |
