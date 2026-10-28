---
name: creative-research
description: Research competitor ads, emerging creative patterns, and transferable ideas with Spiral. Use for category research, competitor investigations, reference discovery, or deciding which new concepts to test for an app or game.
---

# Creative research

Use market evidence and relevant product context to explore categories, understand competitors, identify creative patterns, and inform decisions. Let the user’s objective determine the output, from exploratory findings to recommendations for what to test. Success is a clear answer to the user’s research question, grounded in inspectable references. Adapt depth to the request; finding one reference does not require a category report.

Use Spiral MCP as the primary source for ad discovery, advertiser signals, and creative analysis. If it is unavailable, explain the limitation before substituting another source.

## Establish context

Reuse the conversation, supplied product materials, previous tests, and saved references. Always discuss the researched brand in third person. Call the brand a competitor only when context supports it. Understand the audience's situation, functional or emotional problem, product-supported promise, differentiator, destination funnel, and relevant market. Distinguish known facts from proposed audience hypotheses. Ask only for missing information that would materially change the work; do not require a complete questionnaire to begin research.

## Choose the research route

Prioritize winning and trending ads from `brand_winners` and `trending_ads` when selecting creatives to analyze, expanding to the broader library when needed for coverage or context.

- Category or competitors: use `brands_search` for relevance and `brands_discover` for market-wide rankings. Use `brand_detail` selectively to resolve advertiser identities and context.
- A brand's strongest creative signals: use `brand_winners`. For emerging movement use `trending_ads`; for library inspection use `meta_page_ads`. These answer different questions.
- A specific idea, message, or visual format: use `ads_search`; follow a useful reference with `similar_ads`. Semantic search is Meta-specific. For TikTok, resolve `tiktok_pages` through brand detail and use `tiktok_page_ads` and TikTok detail tools.
- Funnel questions: use `brand_promoted_links` or `meta_page_promoted_links`. Promoted URLs and ad shares do not establish landing-page conversion performance.
- Existing research: use `my_collections` and `collection_ads` before repeating discovery when the user refers to saved material.

For growth or time-sensitive rankings, establish the metric, geography, actual observation dates, and comparable periods before ranking. Check current tool semantics: monthly store totals, rolling EU ad reach, and page-relative rank movement answer different questions. A level is not a growth rate; EU advertising reach is not Europe-wide app growth. If the required comparison is unavailable, give a clearly labeled alternative and identify the missing data. Keep creative-group longevity separate from the representative ad's dates.

Start with narrow searches and small result sets. Inspect a shortlist, then expand when the evidence is repetitive, insufficient, or misses the audience. Include direct competitors and adjacent categories when their audience need or persuasive mechanism transfers; explain that connection.

If a read fails, retry selectively or narrow the request when that can help; avoid repeated identical failures. A fallback to one page or a partial result set must retain that scope. For promoted links, report the window and share denominator when known; preserve meaningful flow and locale parameters when grouping URLs, and label incomplete family totals as partial.

## Extract mechanisms, not just appearances

Prefer Spiral `ad_creative_analysis` for video inspection and `transcribe_ads` for exact spoken wording. Do not open or play videos in the user's visible UI or trigger autoplay during research. Downloads, local media tools, and background inspection are allowed when useful. Provide reference links without launching playback. If analysis is inconsistent, cross-check details, transcripts, or the media; omit unresolved claims. Static images may be inspected through detail tools and creative analysis.

Identify the audience situation, problem, promise, emotional motivation, hook, proof, format, and CTA when observable. A static hook is a visual attention mechanism; a video hook has a temporal structure. Group related executions into concepts before counting diversity. Compare audience/problem, promise, persuasive mechanism, proof, and narrative structure; use media similarity to locate candidates, not decide concept identity by itself. Two meal-scan demos can share one concept despite different opening text; a comedy sketch may introduce a different mechanism. Distinguish a new asset, a new execution, and a new concept. Color changes, translations, and resized assets are not automatically new concepts.

For large duplicate-heavy collections, inspect a representative of each apparent family first, using media identity and available creative evidence. Expand inspection to resolve meaningful message differences or uncertain grouping; do not analyze every duplicate merely to count assets.

For each proposed test connect:

**Observed reference → persuasive mechanism → fit with this product → meaningful adaptation → learning objective.**

Separate proven-by-account-results, competitor signals, and creative hypotheses. A winning score, impression rank, reuse, or reach does not reveal competitor profitability. Missing EU data is unknown, not zero. Describe prevalence within the inspected sample; do not call something a market trend from one example or claim a chronological change without dated evidence.

## Write like a marketer

Write like a perceptive creative strategist: approachable, specific, and energized by useful discoveries.

- **Turn observations into meaning.** Explain what the creative invites someone to feel, believe, or want—and how the hook, story, or demonstration supports that interpretation.
- **Keep useful numbers visible.** Ground the main findings in available quantitative evidence, such as ad duration, longest run, reuse count, reach, or the share of inspected ads using an angle. A friendly tone should retain the numbers that make an insight concrete. Pair important metrics with their marketing significance; use readable rounding, clear units, relevant dates, and a denominator for sample shares. Do not invent metrics or compare incompatible measures to fill a table.
- **Use tables to make comparisons easy.** For competitor comparisons or several creative examples, default to a compact table when it helps the marketer scan differences. Choose columns for the question, such as brand or creative, hook or angle, relevant numerical evidence, and strategic takeaway. Follow the table with the interpretation and ideas worth acting on. Use numbered lists for ranked opportunities or sequential recommendations. Keep simple answers concise without forcing a table or a fixed report template.
- **Keep technical mechanics in the research process.** Avoid ad IDs, representative-ad terminology, tool names, and routine counting explanations in the report. Keep the distinction between creative-group longevity and individual ad dates internal; use a clear label such as "Longest run" when presenting that metric. Explain methodology only when it materially changes the conclusion or the user asks. Translate variations-versus-concepts observations into the marketing takeaway, such as "They keep returning to the same idea, refreshing the hook and meal to give it new life."
- **Make uncertainty natural and proportional.** Lead with discoveries. Keep routine methodology and generic metric caveats internal; surface limitations only when they change the interpretation or the user asks. Use brief language such as "This looks underused in the ads reviewed."
- **Use confident, grounded language.** Keep observations and hypotheses distinguishable. Avoid forced enthusiasm, invented psychology, and unsupported performance claims. Describe an idea as "winning" only when the evidence supports it, without implying competitor profitability.

## Deliver useful research

Answer the user’s central question first, then organize the evidence around the findings that matter. Choose a structure suited to the request. Avoid presenting a tool-by-tool recap or a list of ads without explaining what they reveal.

Make the actual creatives accessible in the final answer. Every specific ad discussed must have a clickable creative link beside its description; in tables, link the creative name or add a "View creative" column. For a grouped pattern, link at least one representative creative next to the insight. Links shown only in tool outputs do not satisfy this requirement.

Use an ad-view URL returned by Spiral when available; otherwise link directly to the returned image or video media URL. Never invent ad-view URLs. Landing pages, brand homepages, ad IDs, and text descriptions are not substitutes for creative links. Label landing-page links separately. If no usable creative URL is available, say so beside that example.

Show representative static creatives or video thumbnails inline when supported and useful, while retaining clickable links to the actual creatives. A video thumbnail must link to the video or ad view, not just the thumbnail image. Do not launch playback or autoplay. Before delivering, check that every ad example and creative table row lets the user inspect the creative without searching for it.

For exploratory research, explain the meaningful similarities, differences, and tensions in the inspected material. Group examples by audience need, message, persuasive mechanism, or another dimension that helps answer the question. Show representative references and relevant counterexamples. Distinguish a recurring pattern from an isolated observation, and a newly discovered execution from evidence of an emerging trend. Surface useful unanswered questions without forcing every finding into an action item.

Default to strategic interpretation and transferable lessons, not advice to improve the researched brand. Do not automatically end with tests or an optimization plan. When the user identifies a competitor, the brand is clearly tracked by the user, or the user asks what to apply, connect relevant lessons to their product or goals where known. Keep the researched brand in third person and make product fit explicit; tracking alone does not establish direct competition. When recommendations are requested, explain why they follow from the findings and prioritize them against the user’s objective. For creative tests, consider product fit, evidence strength, distinctness from known existing tests, and execution feasibility. Connect each concept to its source mechanism, intended audience, supported promise, proposed adaptation, and learning objective. Scale execution detail to the requested deliverable; do not manufacture numerical precision or imply that competitor signals predict the user’s results.

Close with the implication of the research: what the user can now understand or decide, and any next investigation that would materially change that conclusion. Carry references, product facts, hypotheses, and constraints into requested follow-on work. Research alone does not authorize saving collections, generating assets, or starting monitors.
