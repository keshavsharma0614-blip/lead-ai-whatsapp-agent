# Architecture

## Status

Planned

The final architecture will be defined when WhatsApp integration development begins.

## Intended Components

- Webhook endpoint for inbound WhatsApp messages.
- Provider adapter for Twilio or Meta WhatsApp Business APIs.
- AI conversation service for replies, qualification, and handoff routing.
- Lead and conversation storage.
- Business settings for FAQs, availability, scheduling rules, and escalation rules.

## Design Principles

- Verify webhook signatures or tokens before processing.
- Keep provider credentials server-side only.
- Separate message transport from AI response logic.
- Support human handoff for uncertain, sensitive, or high-value conversations.
