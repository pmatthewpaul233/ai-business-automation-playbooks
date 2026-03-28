# Appointment Booking Automation System

## What It Does

Turns cold leads into booked calls automatically. A prospect enters a funnel, gets scored by AI based on fit, and — if qualified — receives a personalised booking link. Non-qualified leads go into a nurture sequence. Zero manual scheduling required.

## Workflow Flow

```
Funnel Page / Lead Magnet Opt-in
        ↓
   Lead Captured (Webhook)
        ↓
   AI Lead Scoring (fit, budget, urgency)
        ↓
   Score ≥ 7 → Booking Link Sent (Calendly / GHL Calendar)
   Score < 7 → Nurture Sequence Triggered
        ↓
   Booking Confirmed → CRM Updated + Sales Notified
        ↓
   Pre-call Reminder Sequence (24h, 1h before)
        ↓
   Post-call Follow-up (automated)
```

## Outcomes

- 📅 **Automated booking** — qualified leads book themselves without back-and-forth
- 🎯 **Better-fit calls** — AI filters out poor-fit prospects before they reach your calendar
- ⏰ **Reduced no-shows** — automated reminders improve show rates
- 💰 **Higher close rates** — pre-call prep sequence warms leads before the call

## Ideal For

- Coaches and consultants selling high-ticket offers
- Agencies doing strategy calls or onboarding calls
- SaaS companies booking product demos
- Service businesses doing consultations

## Tools Required

| Tool | Purpose | Free Tier? |
|------|---------|-----------|
| n8n or Make | Workflow automation | Yes |
| Calendly or GHL Calendar | Booking management | Calendly free tier |
| GoHighLevel | CRM + follow-up sequences | Paid |
| OpenAI / Claude | Lead scoring | Usage-based |
| Twilio / GHL | SMS/WhatsApp reminders | Pay per message |

## Real-World Impact

Deployed for coaching clients. Booking rate from qualified leads improved significantly. No-show rate dropped from ~40% to ~15% with the pre-call reminder sequence.

## Setup Time

~30–40 minutes following the [setup guide](setup-guide.md).
