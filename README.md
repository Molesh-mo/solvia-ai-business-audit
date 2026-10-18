# AI Business Audit: Automated Enquiry Intake with Claude

A free business systems audit on my portfolio site. A visitor answers 7 short questions, and the system logs the enquiry, runs it through Claude to prepare a structured discovery brief, and emails it to me, all without manual work.

**Live site:** https://solvia-system.base44.app (my portfolio and independent practice site)

## The problem
Free audit enquiries need to be captured, understood and followed up quickly, and a form submission alone gives no context for the first conversation.

## The solution
A Make.com automation that turns every audit submission into a logged lead and a ready-made discovery brief.

## How it works
1. Visitor completes the 7-question audit on the website
2. A Make.com webhook receives the answers
3. The enquiry is logged to Google Sheets with a "New" status
4. Claude (Haiku 4.5, via Make's Anthropic module) analyses the answers and produces a structured internal brief: what's known, key information gaps, the main opportunity, discovery questions, and a short client-ready snapshot for manual review
5. An email with the client details and the AI audit is sent to me

## Prompt design
The prompt tells Claude to use only the information provided, never invent facts, clearly separate confirmed information from possibilities, and keep paid-service ideas in a private section. See `audit-prompt.md`.

## Tools used
Base44, Make.com, Webhooks, Google Sheets, Anthropic Claude, Gmail

## Screenshots
![Homepage](IMG_0216.png)
![Audit form](IMG_0218.png)

## Automation blueprint
The exported scenario is in `solvia-audit-scenario-blueprint.json`. Webhook, connection, spreadsheet and email details are replaced with placeholders.

## What I learned
- How to write an AI prompt with strict rules so the output stays grounded in what the client actually said, instead of guessing.
- How to separate internal analysis from a client-ready summary, with a human reviewing before anything is sent.

## What I'd improve next
- Save the AI brief back into the Sheet and score each lead.
- Add an alert if any step fails, and move the AI step into a Python script.

## Built by
Molebogeng Matipwili, AI automation specialist
