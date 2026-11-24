# DICT IT Help Desk Portal: Clickable Demo

A clickable concept demo of the internal IT Help Desk ticketing portal for the IT Division of the Department of Information and Communications Technology (DICT), Papua New Guinea.

This is a **design and workflow reference**, not production code. It runs entirely in the browser with sample data. The production build will be developed on the DTO portal codebase and hosted on DICT's AWS Government Cloud.

## How to run

Open `index.html` in a browser. No build step or server is needed.

## What the demo covers

| Role | What they can do |
| --- | --- |
| Staff | Submit a request with an email code (no password), track progress in My Tickets, comment, confirm a fix or reopen |
| IT Officer | Sign in with password and MFA, work their queue, search tickets, reply or add internal notes, change status and priority, escalate to the IT Manager, use the team workplan |
| IT Manager | Team performance dashboard, all tickets, assign and reassign, handle escalations, export reports (CSV), workplan |
| Executive Manager | Read-only analytics and a TV wall dashboard |

Key behaviours:

- SLA targets count working hours only (Mon to Fri, 8:00 am to 4:00 pm, excluding public holidays).
- On Hold pauses the SLA clock and moves the due time out.
- Staff describe impact and urgency; the portal suggests a priority and IT can change it.
- Resolved tickets close automatically after 3 working days without a reply.
- MFA is required for all IT staff.
- Direct ticket links: `index.html#t-IT-2026-0142`.

## Demo credentials

These work in the demo only.

- Staff email code: `482913`
- IT staff password: `Helpdesk2026!`
- Authenticator code: `482913`

Use **Reset demo** in the top bar to restore the sample data.

## Not in this demo (planned or to confirm)

- Real email notifications and templates
- Attachment storage and malware scanning
- Knowledge base / FAQ
- Linking duplicate tickets to one main incident
- Data retention and records rules
- Categories, SLA targets and the public holiday list are to be confirmed with the IT Division

## Proposed production stack

ECS Fargate, RDS, SES, Amazon Cognito (or department single sign-on), S3 for attachments, and an AWS WAF rule restricting access to the DICT office network. Infrastructure changes require approval under the Government Cloud Team's procedures.

## Files

- `index.html`: the full demo (HTML, CSS and JavaScript in one file)
- `assets/`: DICT emblem and seal, with transparent backgrounds

---

Prepared by Temmah Vanariu, Government Cloud Team, DICT. Sample data only; names and tickets are fictional.
