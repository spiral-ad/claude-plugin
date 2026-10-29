---
name: creative-generation
description: Produce and edit ad creative with Spiral, and organize ads into collections. Use to adapt a reference ad to a product, remix an existing ad, write a brief for new ads, resize, translate, edit, or animate a generation, or save and track ads. Generation charges credits, so confirm scope before producing.
---

# Creative generation

Produce creative the user actually asked for, at the scope they authorized. Every generation tool charges per output, so the cost of a misread request is real. Research and performance analysis belong to the research and analytics skills; come here once a production or organization task is the request.

Use Spiral MCP for generation, editing, and collections. If it is unavailable, say so rather than describing output you cannot produce.

## Confirm authorization before producing

Generation is never implied. A user admiring a reference ad, picking a product, or asking what is possible has not authorized a paid batch. Produce only on an explicit production request.

Before the first paid call, the source asset, the target app, and the output scope must all be settled:

- **Source** — `adapt_to_target` and `remix_ad` each take one source image by uuid: a library Meta or TikTok ad, one of the user's own account ads, or an earlier generation. Use uuids returned by Spiral tools; never guess one. If several candidates match, show them and ask which.
- **Target** — resolve the user's app with `my_apps`. Do not infer the target from conversation context alone when more than one app exists.
- **Scope** — variation count and languages determine the charge. If either is unclear, ask before submitting. Do not pick a "reasonable" default on the user's behalf.

State what will be produced and that it charges before calling. Report charges only once confirmed by the tool result, never as an estimate presented as fact.

## Set scope through parameters, not prose

`aspect_ratio`, `languages`, and `number_of_variations` are dedicated parameters. Never put the aspect ratio, language list, or number of ads in `instructions` or `prompt` — the brief text is for creative direction only. A ratio buried in prose is silently ignored and the batch comes back wrong, already charged.

- `adapt_to_target` — rebuild an existing ad image as an ad for one of the user's apps.
- `remix_ad` — make variations of one source ad.
- `create_ad` — new ads from a written brief with no source image, up to 9 variations per language. Put only the brief in `prompt`.

All three return a `concept_uuid`. Poll `get_generation` with it to collect finished images; a returned uuid is a queued job, not a result.

## Editing an existing generation

`resize_generation`, `translate_generation`, and `ai_edit_generation` each charge per output image and act on one image in place. Confirm the specific edit and how many images it applies to before running them — an edit applied across a batch multiplies the charge.

`animate_generation` charges per generated second. Use the requested model and the shortest duration that satisfies the request. If the user has not said enough to choose a duration, ask. Poll `get_generation` or `get_animation` with the returned identifier.

## Diagnose failures before reassigning blame

For a failed job with an unspecified source-asset error, use available diagnostics before naming a failed asset or recommending a replacement. If the tool cannot identify which asset failed, explain the uncertainty — do not assume the reference was at fault. Keep paid retries inside the authorization the user already gave; a retry at a larger scope needs a fresh confirmation.

## Collections

Saving is free and uncapped, but it is still an action on the user's account.

- `create_collection` creates an empty collection. Call it only when asked.
- To save ads, first read the user's collections with `my_collections`, then call `save_ads_to_collection` with the chosen collection and the matching platform. Keep Meta and TikTok ad IDs and calls separate.
- Report which ads were newly saved and which were already present.

## Meta page tracking

`meta_page_submit` and `meta_page_track_request_create` enqueue asynchronous work and are capped per organization per hour. Use them only when the user asks to submit or track a page; `meta_pages_find_by_url` is the read-only lookup.

Acceptance is not ingestion, and REQUESTED is not approved or actively tracked. Distinguish suggested, requested, pending, and saved states when reporting. Reuse existing tracked identities to avoid duplicates, and never guess page IDs or brand associations. Neither tool is a generic competitor-list editor. Do not start research automatically after a tracking change.
