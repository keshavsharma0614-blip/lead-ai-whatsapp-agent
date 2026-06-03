# User Flow

## Lead Qualification Flow

```text
WhatsApp Message
        ↓
Webhook Received
        ↓
Intent Detection
        ↓
Lead Qualification Questions
        ↓
Qualified?
     /     \
   Yes      No
    ↓        ↓
Store Lead   FAQ / End Conversation
    ↓
Human Handoff Required?
     /      \
   Yes       No
    ↓         ↓
Assign Human Continue Automated Flow
```

## Human Handoff Rules

Escalate when:

* User requests a human.
* Confidence is low.
* Business-specific action is required.
* Sensitive or exceptional situations are detected.
