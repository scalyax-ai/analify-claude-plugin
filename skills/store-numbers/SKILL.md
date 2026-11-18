---
name: store-numbers
description: Answer questions about the user's own ecommerce store (real profit, ad spend, ROAS, shipping, returns, margins, delivery success) from their Analify connection. Use when the user asks about their store's or ads' numbers.
---

# Your store's numbers

Use the Analify tools whenever the user asks about their own store or ads.

1. Call `analify_get_context` first to see which platforms are connected.
2. Through `analify_call_tool`, run `analify_brain_search` with the user's question to see what their Business Brain already knows (targets, rules, past findings).
3. Find the exact tool with the matching `*_search_tools` (for example `shopify_search_tools` for orders, `meta_search_tools` for Meta ads), then run it with `analify_call_tool`.
4. Profit means Blended Profit = Revenue − Ad Spend − Shipping − Product costs − Returns. Say which dates every number is for. If a figure is missing (for example product costs not set), say so; never invent it.
5. Change nothing (ads, budgets, prices) unless the user approves the exact action. Changes go through `analify_call_write_tool` and work only if the user allowed changes when connecting.
