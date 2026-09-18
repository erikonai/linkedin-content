---
name: draft-linkedin-posts
description: >-
  Draft LinkedIn posts in Erik's Campfire Applied AI voice and save them to
  Notion Social Media Planner at Post Idea. Use for LinkedIn content, a batch
  of drafts, a weekday 9AM refill, or to refill the review queue. Never publish
  to LinkedIn.
---

# Draft LinkedIn posts to Notion for review

Source of truth (fetch this page first and follow it):
https://app.notion.com/p/3ce5e6694627817c9debf68c4e304436

Scheduled weekday run prompt:
`.cursor/automations/weekday-linkedin-drafts.md`

If Notion is unreachable, draft in chat and say they were not saved.

## When this applies

Erik wants LinkedIn copy sitting in Notion so he can decide whether to post.
Also use on the weekday 9:00 AM ET automation tick.
Do not use this to file other people's posts — that is save-linkedin-inspiration.

## Destinations

- Hub: https://app.notion.com/p/3ce5e66946278105a0a4fc496a44df22
- Review DB: https://app.notion.com/p/3ce5e6694627804792c0fedb8916f055
- Review data source: `collection://3ce5e669-4627-8088-b23f-000b14485a78`
- Inspiration: https://app.notion.com/p/024d0c3975b344cf9328b3c8def35a70
  (`collection://d50dbad2-26ad-4349-b590-402ceaa3b662`)
- ICP: https://app.notion.com/p/3d85e6694627816ba717da51dfd45a78
- This repo: `images/` (rendered 1200×1200 JPEGs), `specs/` (HTML sources)

## Scheduled weekday run

Cron: `CRON_TZ=America/New_York 0 9 * * 1-5`

1. Delete leftover **Not approved** rows from a prior day.
2. If today's 9:00 AM ET slot already has 3 Post Ideas, stop (do not duplicate).
3. Otherwise create 3 Post Ideas for that slot. Never publish to LinkedIn.

## Form and voice (Erik 2026-09-14)

Steal specificity from inspiration, not the set piece.

## Graphics (do not ship three quote cards)

Fetch Inspiration screenshots and skim older `images/` maps before drawing. Steal **visual form**, not the set piece: tables, four-column driver maps, numbered stacks, bingo, two-column translators, workflow steps. Never clone a $20M waterfall, a 13-item permission list, or april-blue grids (`#EDF2F8` / `#16375A`).

Campfire palette only: paper `#F9F9F8`, forest `#142D25`, flame `#FF862F`, sage `#4E615B`, Denim titles, Inter body, 1200×1200. Flame mark top-right, wordmark in the footer.

A batch of 3 must use **three different layouts**. A quote-card (kicker + giant quote + one note) is a last resort for one scar/wit post, never the default, never all three. Density should match July/Aug maps (full canvas of cells), not a sparse sentence on cream.

- A timestamped log, a 3×3, or a two-character sketch reads as LinkedIn theater if Erik did not live that day.
- Write what would survive a Controller saying “that’s not how it works.”
- Realistic: one conversation, one close artifact, how the work actually moves (waiting on the firm, pasting into last quarter’s deck, doing the messy rec in the sheet).
- Erik is the person in the room asking questions, not the hero of a reconstructed Monday.
- No fake folder names, fake timestamps, or “craziest part of all of this.”
- Overheard lines a Controller would actually say beat reconstructed calendars.
- Ending required, form must vary. Leave a next thought that grew out of this scene: a specific operator question, a bar Erik would count, or one Ember-shaped sentence. Scan the last 6 Post Idea endings and do not reuse them. Banned as a formula: “How do you all solve for this?”, “What if this didn’t have to exist?”, “That’s the world Ember is for.” Name Ember at most once. If the scene already named Ember, the ending does not.
