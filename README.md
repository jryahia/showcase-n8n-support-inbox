# n8n Support Inbox

**One inbox for WhatsApp, email and website chat, where AI drafts replies and a human approves them before sending.**

> **This is a proprietary project. Source code is private. This page showcases the system's architecture and results.**

**Case study page:** [https://jryahia.github.io/showcase-n8n-support-inbox/](https://jryahia.github.io/showcase-n8n-support-inbox/)

![n8n Support Inbox](assets/00-home.png)

## Problem it solves

Support spread across WhatsApp, email and chat means context gets lost and replies are slow. Fully autonomous bots are risky for customer-facing answers. This inbox unifies the channels and keeps a human approval gate on every outbound AI draft. It is built as the webhook backend for a n8n scenario: the automation platform handles triggers, and this service holds the logic and data.

## Architecture

![Architecture](assets/architecture.svg)

1. Messages from all three channels land as conversations in one store.
2. An agent can request an AI-drafted reply; it is saved as pending.
3. A human approves or rejects the draft.
4. Approved drafts are sent back on the original channel.

## Key features

- Single conversation list across channels
- AI drafts with an approve/reject lifecycle
- Channel and status filters
- Unread and pending counters
- Webhook endpoints ready for n8n

## Tech stack

![Python](https://img.shields.io/badge/Python-161b22?style=for-the-badge&labelColor=161b22&color=161b22) ![FastAPI](https://img.shields.io/badge/FastAPI-161b22?style=for-the-badge&labelColor=161b22&color=161b22) ![Webhooks](https://img.shields.io/badge/Webhooks-161b22?style=for-the-badge&labelColor=161b22&color=161b22) ![OpenAI](https://img.shields.io/badge/OpenAI-161b22?style=for-the-badge&labelColor=161b22&color=161b22) ![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-161b22?style=for-the-badge&labelColor=161b22&color=161b22) ![Jinja2](https://img.shields.io/badge/Jinja2-161b22?style=for-the-badge&labelColor=161b22&color=161b22)

## What it does in practice

- Gets the speed of drafted replies while keeping every outbound message human-approved.

## Screenshots

**Unified inbox across channels**

![Unified inbox across channels](assets/00-home.png)

**Conversation with an AI draft awaiting human approval**

![Conversation with an AI draft awaiting human approval](assets/10-conversation.png)

---

Built by [Yahya Jarray](https://github.com/jryahia). Interested in a similar system? [Get in touch](mailto:yahiajarray43@gmail.com).
