---
layout: posts
title: 'Hidden risk in Notion 3.0 AI agents: Web search tool abuse for data exfiltration'
date: '2025-09-20 03:56:11 '
excerpt: 'Notion 3.0''s shiny new AI agents promise to handle everything from doc creation to multi-step workflows across your workspace, but they''re packing a sneaky vulnerability that could let attackers siphon off sensitive data. The real issue is '
seo_title: 'Hidden risk in Notion 3.0 AI agents: Web search tool abuse for data exfiltration'
seo_description: Notion 3.0's shiny new AI agents promise to handle everything from doc creation to multi-step workflows across your workspace, but they're packing a sneaky
categories:
- Security
- Azure
- AI_Automation
tags:
- Security
- Azure
- AI_Automation
permalink: /blog/hidden-risk-in-notion-30-ai-agents-web-search-tool-abuse-for-data-exfiltration/
---

Notion 3.0's shiny new AI agents promise to handle everything from doc creation to multi-step workflows across your workspace, but they're packing a sneaky vulnerability that could let attackers siphon off sensitive data. The real issue is how these agents combine LLM smarts, tool access, and persistent memory to bypass traditional access controls, turning a simple web search feature into a backdoor for exfiltration—think embedding a malicious prompt in a PDF to trick the agent into shipping your private Notion page contents to a shady server. In a demo, even a top-tier model like Claude Sonnet 4.0 got duped into constructing and firing off queries that leak confidential info, highlighting how MCP integrations with tools like GitHub or Gmail amplify the risks. Small businesses and MSPs should watch out, as this expanded threat surface means your routine AI automations could unwittingly expose customer data, so double-check agent permissions and scrutinize any incoming files before letting bots loose.

**Source:** [https://www.codeintegrity.ai/blog/notion](https://www.codeintegrity.ai/blog/notion)
