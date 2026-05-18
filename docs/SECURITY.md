# Security

## Status

Planned

Security controls must be reviewed again when WhatsApp integration code is added.

## Requirements

- Do not commit provider tokens, webhook secrets, `.env` files, or customer exports.
- Verify webhook tokens or signatures before processing messages.
- Keep WhatsApp and Twilio credentials server-side only.
- Avoid logging message content unless there is a documented privacy reason.
- Scope conversations and leads by authenticated organization.
- Add human handoff for sensitive, uncertain, or high-impact conversations.

## Reporting

Report security concerns privately to the maintainer before public disclosure.
