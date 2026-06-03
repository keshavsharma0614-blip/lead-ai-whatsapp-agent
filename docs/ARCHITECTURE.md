# Architecture

## Status

Prototype / In Development

This document describes the intended architecture. It must be updated when implementation files are added.

## System Context

Lead.AI WhatsApp Agent supports this product role: WhatsApp AI assistant for business leads and customer support.

Business problem: Businesses miss WhatsApp leads and manually answer repetitive questions.

## Core Layers

- **Experience layer:** user-facing screens, widgets, reports, dashboards, or documentation flows.
- **API/workflow layer:** input validation, business rules, routing, integrations, and orchestration.
- **AI layer:** prompts, scoring, summaries, explanations, recommendations, or decision support.
- **Data layer:** product records, configuration, outputs, audit records, and analytics events.
- **Security layer:** authentication, authorization, secret management, privacy, logging, and abuse controls.

## Planned Components

- WhatsApp message handling
- Lead qualification
- FAQ responses
- Booking intent detection
- Business hours handling
- Escalation to human
- CRM-ready lead storage
- Twilio integration placeholder

### Lead Qualification Flow

The MVP workflow is expected to:

1. Receive inbound WhatsApp messages through a webhook.
2. Detect intent and collect qualification details.
3. Determine whether the lead meets business-defined qualification criteria.
4. Route qualified leads for follow-up.
5. Escalate conversations to a human when handoff rules are triggered.

### Human Handoff Rules

Human escalation should occur when:

* A user explicitly requests a human.
* Confidence in the AI response is low.
* A business-specific decision is required.
* The conversation falls outside supported workflows.


## Data And Integration Notes

- Store only the data required for the workflow.
- Keep provider-specific code behind clear adapters.
- Document data retention and deletion expectations before production use.
- Avoid storing private customer data in logs or public examples.

## Architecture Principles

- Keep the MVP small and testable.
- Separate UI, backend, AI, and integration concerns.
- Validate inputs before persistence or AI processing.
- Make important AI outputs reviewable and explainable.
