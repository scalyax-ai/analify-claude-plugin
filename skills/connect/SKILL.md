---
name: connect
description: Connect Claude to your Analify workspace — sign in, check which platforms (Shopify, Meta, TikTok, Google Ads, Snapchat, couriers) are connected, and show what's still missing.
disable-model-invocation: true
---

# Connect Analify

1. **Sign in.** Call `analify_brain_session_start` with this session's id.
   - If the Analify tools aren't available or ask for authentication: tell the user to run `/mcp`, choose **analify** → **Authenticate**, sign in, pick their workspace, and tick **Allow changes** if Claude should be able to save to the Business Brain (Claude still asks before changing any ad or price). Then run `/analify:connect` again. Stop here.
2. **Say which workspace it is.** Name the organization the session returned, so the user can confirm it's the right store.
3. **See what's connected.** Call `analify_get_context` and list, per platform, how many accounts are connected and which are disconnected.
4. **Report in plain words:**
   - "Connected: …" (platforms and how many ad accounts).
   - "Missing: …" with what each gap means, for example "No store connected, so I can't see orders or real profit yet" or "Meta disconnected, reconnect it in Analify".
   - Two or three things Claude can do now with what is connected, such as yesterday's real profit or a Meta and TikTok spend check.
5. If anything is missing, give the link https://analify.scalyax.ai → Settings → Integrations, and suggest running `/analify:connect` again afterwards.
