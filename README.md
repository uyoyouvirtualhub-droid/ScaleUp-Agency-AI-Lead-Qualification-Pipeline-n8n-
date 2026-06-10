# ScaleUp Agency — AI Lead Scoring & Sales Pipeline

A multi-channel lead qualification system that automatically 
scores incoming leads using AI and routes them to the 
appropriate sales action — without any manual triage.

## Problem It Solves
The agency was receiving leads from multiple sources and 
spending hours manually qualifying, sorting, and following 
up. Hot leads were being treated the same as cold ones, 
causing lost revenue.

## Tools Used
- n8n (workflow automation)
- OpenAI API (lead scoring)
- Webhook (lead capture trigger)
- Switch node (routing by score)
- Slack (hot lead alerts)
- Gmail (automated follow-up emails)
- Calendly (auto booking for hot leads)
- Google Sheets (lead log)
- Telegram (team notifications)

## How It Works
1. Lead submits via webhook (website form or CRM)
2. OpenAI scores the lead based on budget, intent, 
   and fit criteria — returns a score and reasoning
3. Switch node routes by score tier:
   - Hot lead → Slack alert + Calendly booking link sent
   - Warm lead → Gmail nurture sequence triggered
   - Cold lead → Google Sheets log + Telegram notification
4. All leads are logged to Google Sheets regardless of tier

## Key Concepts Demonstrated
- AI-powered lead scoring with OpenAI
- Multi-branch Switch node routing
- Slack Block Kit notifications
- Cross-node data referencing with $('NodeName').item.json
- Full CRM-style pipeline in n8n
