![Analify](./icon.png)

# Analify

Ask Claude what your ecommerce store actually made. Analify connects your store, ads and shipping data to Claude, and answers from your own numbers and your own Business Brain: the costs, rules and decisions your business already set.

## What it does

- **Real profit, not just sales.** Answers with Blended Profit: revenue minus ad spend, shipping, product costs and returns.
- **Every platform in one place.** Shopify, Meta Ads, TikTok Ads, Google Ads, Snapchat Ads, GA4 and couriers, through one Analify connection.
- **It remembers your business.** Findings, decisions and rules you save go to your Analify Business Brain, so the next conversation starts from them.
- **You stay in control.** Claude reads by default. It changes an ad, budget or price only after you approve the exact action, and only if you allowed changes when connecting.

## Get started

1. Create an Analify account and connect your store and ad accounts: https://analify.scalyax.ai
2. Install this plugin in Claude.
3. Run `/analify:connect`. Claude asks you to sign in to Analify (run `/mcp` → **analify** → **Authenticate**), then shows what's connected and what's missing.

## Try asking

1. "What did we actually make yesterday after ads, shipping and returns?"
2. "Which Meta and TikTok ad sets lose money once returns are counted?"
3. "Compare this week's ad spend and ROAS with last week, per platform."
4. "Give me this morning's brief." (or `/analify:brief`)

## Commands

| Command | What it does |
| :- | :- |
| `/analify:connect` | Sign in and see which platforms are connected and what's missing |
| `/analify:brief` | Morning brief: yesterday's real profit, ads to act on, delivery problems |
| `/analify:save` | Save a finding, decision, business rule or report to your Business Brain |

One skill works in the background: it answers questions about your store's numbers whenever you ask.

## How it connects

The plugin adds one connection, the Analify MCP server at `https://analify-mcp.scalyax.ai/`, signed in with your Analify account (OAuth). Nothing runs on your computer. Learn more: https://analify-ai.readme.io/docs/mcp

## Data and permissions

- Claude sees only the Analify workspace you sign in to, and only what your role in it allows.
- Reads are on by default. Changes need **Allow changes** at sign-in and your approval of each action.
- Remove the connection any time in Analify (Settings → AI connections) or with `/mcp`.
- Privacy policy: https://analify.scalyax.ai/en/privacy · Terms: https://analify.scalyax.ai/en/terms

## Troubleshooting

- **"Authentication needed"**: run `/mcp`, choose **analify**, **Authenticate**, and sign in again.
- **A number is missing**: Claude says what's not connected or not set (for example product costs). Connect it in Analify, then ask again.
- **Wrong store**: sign in again and pick the right workspace on the Analify screen.

## Support

https://analify.scalyax.ai/en/contact · analify@scalyax.ai

## License

MIT
