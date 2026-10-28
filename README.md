# Spiral for Claude Code

Connect Claude Code to [Spiral](https://spiral.ad)'s hosted MCP server and work with ad intelligence through conversation. The plugin adds four skills that guide competitor research, connected-account performance analysis, creative production, and onboarding, so you can ask for what you want in plain language instead of selecting tools by hand.

Spiral indexes Meta and TikTok ads, brands, and advertiser pages, and connects to your own Meta ad accounts for private performance data. This plugin layers workflow guidance on top: which tool answers which question, how to compare metrics without mixing attribution windows, and when a creative action costs credits.

## Install

```
/plugin marketplace add filipkny/spiral-claude-plugin
/plugin install spiral@spiral
```

On first use, Claude Code prompts you to sign in and authorize access to your Spiral account. The endpoint and connection flow follow the [Spiral MCP documentation](https://docs.spiral.ad/docs/public/api-reference/mcp).

## Skills

| Skill | Use it for |
| --- | --- |
| `spiral-onboarding` | Understanding what Spiral offers and how to ask for it. Start here if you are new. |
| `creative-research` | Competitor ads, category research, emerging creative patterns, and references worth testing. |
| `creative-analytics` | Diagnosing winners and weak ads in your connected Meta accounts, and choosing the next test. |
| `creative-generation` | Adapting, remixing, editing, and animating ad creative, plus collections and page tracking. |

Claude selects the right skill from your request; you do not need to name it.

## Example requests

- "What is Spiral and how do I get started?"
- "Find competitor ads for a fitness tracking app."
- "Which of my Meta ads underperformed last month, and what should I test next?"
- "Adapt this reference ad for my product."

## Costs

Research and analysis are read-only. Creative generation and editing charge credits per produced image, and animation charges per generated second. The `creative-generation` skill is written to confirm the source, target, variation count, and languages with you before submitting a paid batch — it will not start producing on an implied request.

## Privacy

Your requests are sent to Spiral's hosted MCP server. Connected ad-account data is private to your organization. See the [Spiral privacy policy](https://www.spiral.ad/privacy-policy).

## License

Proprietary. Copyright (c) 2026 Spiral. See [LICENSE](LICENSE).
