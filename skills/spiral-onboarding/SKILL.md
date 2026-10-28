---
name: spiral-onboarding
description: Explain what Spiral MCP is, what its intelligence and creative tools make possible, and how to use it through conversation. Use for new-user onboarding, plugin setup, walkthroughs, and questions about getting started. Run research, analytics, or generation only when requested, using the corresponding specialist skill.
---

# Spiral onboarding

Help a new user understand Spiral and feel confident using it. Success means they understand what information is available, why it is useful, how their product context personalizes the work, and how to ask for what they need. Onboarding itself does not require a competitor report, ad ideas, a performance analysis, or a generated ad.

A request such as being new, asking what Spiral can do, or asking for a walkthrough calls for explanation and guidance. It is not a request to run a creative workflow. Do not choose research as a default, produce a fixed number of ideas, or treat selecting a product as permission to start researching its ads.

## Explain what Spiral is and how to use it

Start by explaining Spiral MCP in your own words: it connects the user’s AI assistant to Spiral’s app-market intelligence, competitor creatives, saved product context, and connected advertising data and creative tools. Show that the user can work through conversation. Mention tool names, commands, or API syntax only if the user asks about setup or how technical the experience is.

Keep the first onboarding response to 150–250 words in total, including any introductory commentary, usually in two or three short paragraphs. This word range applies only to the first onboarding response; later replies have no fixed word limit and should match the user’s question and requested depth. Explain what Spiral is, make its value tangible with one useful connection, show how to ask for help, and propose a next step. Mention research, static creation, and connected-account learning naturally; save detailed feature lists and prerequisites for follow-ups. Explain enough before asking the user to choose, without making them read a brochure.

Write like an insightful creative strategist: connect a capability to something the user can discover or decide. For example, market momentum helps choose whom to study, while creative analysis reveals the hook or demonstration worth learning from. Choose the connection that fits this conversation instead of explaining the whole research-to-results cycle every time. Make possibilities feel exciting through specific insights and active language. Present better ad win rate and ROAS as goals, without inventing results.

Show how the conversation moves the user toward something useful: they can name an app, ask about a competitor, or share an ad they like, then ask to explore an interesting pattern or adapt a reference for their product. Describe concrete actions in natural language rather than abstract instructions such as “refine the answer with follow-ups.” Choose an example that fits the conversation; do not turn these suggestions into a fixed script. Use one short example request suited to their interests or product when known; add more only if the user asks for examples. Make clear these are things they can ask for; do not execute examples as if the user requested them. Explain inputs when they matter to the question—for example, connected Meta accounts enable analysis of their own performance, and Adapt uses a static reference and a target product. Avoid repeating setup requirements before and after tool reads. Users do not need to know the names of the specialist skills.

Guide the conversation responsively. Answer follow-up questions, offer to explore relevant saved context, or help the user understand a capability in more detail. Ask only a focused question that advances their understanding or resolves necessary ambiguity. Avoid a fixed welcome script, prescribed final wording, mandatory sequence of questions, or an automatic handoff. The sections below are knowledge and guidance for the agent, not text to recite.

Use Spiral MCP as the primary source for workspace context. Inspect available tool descriptions before promising capabilities. Distinguish what Spiral can provide from data actually retrieved for this user. Tool names below describe routes, not guarantees that every deployment exposes them. If access is unavailable, explain the specific limitation when relevant. Do not switch to browser control unless requested.

## Explain the research intelligence

Help the user understand why this information is valuable, not just that it exists. Introduce the breadth in a digestible way, group related signals naturally, and expand on what interests them. Use this table as reference material; do not require a live research run to explain these capabilities or dump the whole table into every welcome.

| Signal | Value for the user |
| --- | --- |
| Estimated downloads and app revenue | Identify apps worth studying and compare their scale and growth. |
| Active ads, linked Meta pages, and TikTok | Understand advertising activity and discover creative approaches across pages and platforms. |
| EU reach | Understand advertising exposure and prioritize markets or creatives to investigate. |
| Trending and winning ads | Discover emerging opportunities and established creative patterns. |
| App Store rankings | Understand category and country relevance. |
| Creative analysis | Break down an ad’s hook, visual execution, story, product demonstration, and CTA to understand what makes the concept compelling and how to adapt it for your app. |
| Ad copy and transcripts | Examine exact wording, promises, objections, and proof to develop sharper messaging. |
| App reviews, when accessible | Find customer language, frustrations, desired outcomes, and messaging opportunities. |

Keep estimates labeled and preserve platform, market, and time scope when discussing actual figures. Mention reviews when accessible through a supported source. These are reasoning checks, not extra caveats to append to onboarding. Surface a limitation only when the user asks about it, it changes the proposed next step, or a specific statement would otherwise mislead them.

## Explain what Spiral knows about the user’s product

Saved context is part of onboarding, not a trigger for production. Use `my_apps` when exploring the user’s setup. An entry in “Your apps” is a saved promotion target. Reuse an unambiguous selection; ask which product when several are plausible and a profile review is relevant. Read `app_detail` only for the selected product. A general explanation of Spiral does not require choosing a product first.

Explain how saved positioning, audience, benefits, differentiators, and assets help tailor future research and creatives. Make it clear users can review and edit this context. If no saved product exists, explain that a product URL or short description can support a later research request; saving a profile is not a prerequisite for understanding or trying research.

When useful for the walkthrough, `get_ad_accounts` can establish whether connected analytics is available. Treat connection state and reporting coverage separately in your reasoning; do not fetch performance metrics merely to demonstrate onboarding or append a reporting-coverage notice to a simple connection summary. Review tracked brands with `brands_search` and `tracked: "only"` when explaining the user’s saved competitor setup, preserving query scope and pagination. Retrieve collections or past concepts only when the user refers to them.

Present a concise summary grounded in the records actually returned. Describe missing fields as unavailable in that response, not nonexistent. Reuse prior conversation context; do not assume a new chat means a new user or invent a persisted onboarding-completion state.

| Context | What the available records may establish |
| --- | --- |
| Product positioning | Saved summary, main benefits, features, audience descriptions, use cases, reasons to choose the product, additional notes, and destination URL from `app_detail`. |
| Brand and offers | Saved colors, logos, reference assets, and promotional offers. Describe the assets returned for this product. |
| Advertising setup | Connected Meta accounts, associated app, campaign platform, configured conversion event, currency, and sync status. Use actual reporting metrics for later performance questions. |
| Competitive context | Tracked brands that can inform later competitor selection and ad research. |
| Previous creative work | Saved collections and generated concepts when retrieved, with their returned status. |

Use precise labels such as saved audience, connected account, and tracked brand. Ground claims about customers or performance in the corresponding records; do not imply access to information that was not provided. Keep routine evidence checks internal during a profile walkthrough.

Explain how the saved context can personalize future work. Mention gaps only when they matter to what the user is exploring.

## Review and improve product context

When reviewing the selected product, show its saved positioning in a few lines: who the product serves, the outcome it promises, why someone would choose it, and the features or proof supporting that promise. Lead with the outcome rather than a feature inventory. Invite correction of the main promise or audience when not already confirmed. Do not turn the review into a questionnaire about campaign goals or performance targets.

If the user requests saving a correction, use an available `app_update` tool after inspecting its schema and current record. Show the concrete changes; existing authorization to save those changes is sufficient. Read the record back when supported to verify persistence. Never invent an update tool or overwrite a complete structured profile with a short summary.

If a requested edit cannot be saved, provide paste-ready replacement text and explain the limitation briefly. Mention unsaved context only when the user requested an update or could reasonably believe one was saved; ordinary positioning summaries do not need a persistence notice. Continue the walkthrough. Profile editing is optional; it is not a prerequisite for using Spiral.

## Explain competitor tracking and support requested setup changes

Explain that users can review their tracked brands and add relevant competitors to make future monitoring and research more useful. Do not automatically expand the competitor set or inspect ads during a walkthrough. If the user asks to discover competitors or research a category, use the creative-research skill. If they ask to add named or selected competitors, inspect the supported tracking tools and perform the authorized setup change without another generic permission question.

Reuse existing tracked identities to avoid duplicates. Use an existing-brand tracking tool when available. `meta_page_submit` submits a verified Meta page for asynchronous tracking; acceptance does not mean ingestion is finished. `meta_page_track_request_create` requests a verified page under an existing brand; REQUESTED does not mean approved or actively tracked. Neither is a generic product competitor-list editor. Never guess page IDs or brand associations. If the required write is unavailable, explain the specific limitation and distinguish suggested, requested, pending, and saved states. Do not automatically start research after a tracking change.

## Use specialist skills when the user asks to do the work

A user request to research, analyze, or generate is the handoff point. Selecting a product for a walkthrough or acknowledging the explanation is not such a request. If the user already made a concrete task request, skip redundant onboarding and use the relevant skill immediately.

| Requested work | Skill to load and follow |
| --- | --- |
| Competitor discovery, category or ad research, creative inspiration, or ideas to test | `creative-research` |
| Analysis of the user’s connected Meta ad performance | `creative-analytics` |
| Static ad adaptation or supported static creative production | `static-ad-generation`, including an available plugin-prefixed equivalent |

Load only the relevant available specialist skill. Carry the user’s request, selected product, confirmed positioning, constraints, and relevant references into it. Let that skill govern the workflow and deliverable; onboarding must not substitute its own mini research, analytics, or generation routine. If the required skill is unavailable, briefly explain the blocker and propose a concrete recovery step. Check supported skill discovery or setup guidance when available; otherwise offer to help locate or add the required skill and preserve the user’s request for resuming. Do not invent installation commands, UI steps, or capabilities, claim the skill ran, or substitute your own workflow. Avoid ending with only a vague promise to continue once it is available.

Present Adapt as the static production route. Do not offer video briefs or video generation as an onboarding option or automatic next step. Follow creative-generation’s parameters and charging requirements when a generation task is requested; onboarding alone never authorizes generation credits. For a failed Adapt job with an unspecified source-asset error, use available diagnostics before identifying a failed asset or recommending a replacement. If the tool cannot identify it, explain the uncertainty rather than assuming the reference failed. Report charges only when confirmed, and keep paid retries within existing authorization.

## Keep the walkthrough conversational

Keep each turn focused on the user’s question. Use short, connected prose and a useful example rather than repeated feature lists. Explain the opportunity, then leave room for a reply. Do not repeat the overview after reading a profile; share only what the retrieved context adds. Keep internal IDs and routine tool mechanics out of the explanation.

Remove boilerplate caveats from welcomes, profile reviews, and capability explanations, including general warnings about competitor profitability, guaranteed uplift, or saved audiences not being measured demographics. When explaining why research signals are useful, describe what each reveals and which decision it informs; do not append a limitation to each signal. A question about usefulness does not by itself call for a warning about profitability or causality. Preserve accuracy with labels and grounded claims. Explain limitations when the user asks about inference or reliability, or when a limitation changes an actual recommendation or next step, such as an unavailable skill, a failed save, or missing data needed for a requested analysis.

End with one concrete, relevant next-step proposal. It might be reviewing the selected app’s saved promise, asking which saved product to explore, requesting a product URL when no context is available, or offering a deeper explanation of the capability the user is curious about. Give the user an easy way to respond; avoid a generic “whenever you’re ready” or a menu of every feature. If the context already resolves a question, do not ask it again.

A proposed next step is not permission to execute research, analytics, or generation. Wait for the user’s request or acceptance of that specific action. If they already requested the work, proceed through its specialist skill without another approval question. For a blocker, make the next step a supported way to resolve it. Report persistence status when a change was requested or attempted, and do not claim scheduling, publication, saved changes, or onboarding-completion state without supported success.
