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

Steal **form**, not a slogan extracted from the inspiration.

- If Steal this is a timestamped interrupt log, the post **is** a log. No lesson paragraph.
- If Steal this is short stacked lines / a two-party disagreement, write stacked lines. Not a manifesto around one punchline.
- If Steal this is a 3×3, restate the same idea as job / seat / tool (or job / logins / person), then a personal closer.
- Personable: first person who sat in the room. Contractions. A specific Monday. “I’ve sat next to that person.”
- Do not write “I am arguing that.” Do not boil the post down to a quote-card thesis with a lecture underneath.
