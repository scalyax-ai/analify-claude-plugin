---
name: brief
description: Morning brief for your store — yesterday's real profit, ads that need attention, delivery problems, and what's missing — from your Analify connection.
disable-model-invocation: true
---

# Morning brief

1. Call `analify_get_context`, then, through `analify_call_tool`, `analify_brain_search` for what the Business Brain already knows (targets, rules, past findings) and `analify_brain_operating_contract`.
2. Yesterday and the last 7 days: Blended Profit (revenue − ad spend − shipping − product costs − returns), ad spend and results per platform, and delivery and return problems if a courier is connected. Find each tool with the matching `*_search_tools` and run it with `analify_call_tool`.
3. Write a short brief: what happened, the one or two things to act on today, and what's missing (for example product costs not set, so profit is incomplete). Never invent a number; say what's missing.
4. Changes (pausing ads, budgets) only after the user approves the exact action.
