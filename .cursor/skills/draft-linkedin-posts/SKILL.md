---
name: draft-linkedin-posts
description: >-
  Draft LinkedIn posts in Erik's Campfire Applied AI voice (finance-native
  bridge to Ember) and save them to Notion Social Media Planner at Ready for
  Review. Use when he asks for LinkedIn content, a batch of drafts, or to refill
  the review queue. Never publish to LinkedIn.
---

# Draft LinkedIn posts to Notion for review

Source of truth (fetch this page first and follow it):
https://app.notion.com/p/3ce5e6694627817c9debf68c4e304436

If Notion is unreachable, draft in chat and say they were not saved.

## When this applies

Erik wants LinkedIn copy sitting in Notion so he can decide whether to post.
Do not use this to file other people's posts (screenshots, links, or pastes)
— that is `.cursor/skills/save-linkedin-inspiration`.

## Destinations

- Hub: https://app.notion.com/p/3ce5e66946278105a0a4fc496a44df22
- Review DB: https://app.notion.com/p/3ce5e6694627804792c0fedb8916f055
- Review data source: `collection://3ce5e669-4627-8088-b23f-000b14485a78`
- Inspiration: https://app.notion.com/p/024d0c3975b344cf9328b3c8def35a70
  (`collection://d50dbad2-26ad-4349-b590-402ceaa3b662`)
- This repo: `images/` (rendered 1200×1200 JPEGs), `specs/` (HTML sources)

Fetch both databases before writing.

## Role (why the content exists)

Erik is Campfire's finance-native bridge between **Ember** (Campfire's applied
AI) and customers. Day to day that looks like strategy and operations: go where
the problem is, with AI as the throughline. LinkedIn is the **external** half of
a roughly even external/internal split.

- Not product owner. Informal, real input into Ember from customer reality.
- Not ticket-queue support. Drive **adoption of what Ember already does**, then
  turn that into playbooks CS can scale.
- Go **deep with a handful of strategic finance leaders**. Public posts are the
  scaled version of that motion. Do not name accounts.
- Close, billing, variance, OpEx, headcount, compliance, and internal process
  are all in-bounds as long as a CFO would trust this person on Ember afterward.
- Finance, operations, and compliance background is source material, not a
  second brand.
- East Coast events are presence, not a posting theme unless Erik asks.

Primary audience: CFOs, controllers, FP&A, heads of accounting.
Secondary: founders/operators buying Campfire, Campfire customers/prospects.
CS enablement is a *downstream use* of the post, not the LinkedIn audience.

## Campfire benefit (required)

Fill **Campfire benefit** with one sentence. If you cannot, rewrite the post.

1. **Trust** — a finance leader would take Erik's call about Ember after
   reading this, and Ember is not mentioned.
2. **Category** — names a real finance workflow AI should already do. Ember may
   be named once, as the system that should hold that workflow, never as a
   feature tour.
3. **Adoption** — a specific "this is how a team actually uses it" pattern CS
   could reuse. No demo CTA.
4. **Two-way** — a customer-shaped gap that should inform Ember, without
   dumping a product roadmap.

A batch of 3 should not all be Category. Default mix: 1 Trust, 1 Category or
Two-way, 1 optional Adoption.

Do not write join announcements, feature lists, april-company voice, demo CTAs,
or Ember as the hero of a story with no finance scar.

## Voice

Startup finance operator. Applied AI in the finance stack is the throughline,
not generic AI takes.

- Specific artifacts and failure modes (plan vs forecast vs budget, 13-week
  cash, fully loaded headcount, nexus, dilution, AR aging, revenue bridges,
  department-coded OpEx, close, billing, which version went to investors).
- Short LinkedIn lines. White space. One idea per post.
- Dry punchlines. Contrast tables, staircases, before/after. Admit unsolved
  problems.
- Personal byline, Campfire as context when earned. No april footer, no
  Campfire logo bar on graphics unless asked, no hashtag dumps, no "I'm
  humbled," no emoji walls, no engagement-bait as the whole post.

Graphic language when pairing an image: ground `#EDF2F8`, navy `#12263A` /
`#16375A`, Georgia titles, Helvetica body, 1200×1200, small-caps kicker,
punchline in a navy bar. Render pipeline: `.github/workflows/render-specs.yml`.

## Before writing

1. Query Inspiration where Reusable is yes, newest first (~15). Fetch 3–6
   full pages including screenshots. Use hook patterns, "Steal this", and
   **Campfire angle** — never wording.
2. Query Social Media Planner for recent Ready for Review / Draft / Published
   titles so you do not duplicate a live draft.
3. Skim `images/` filenames and matching `specs/*.html`.
4. If Inspiration is empty, still draft from voice + graphics, and say the
   library is thin.

Default to **3 posts** if unspecified (max 5 unless asked).

## Save each draft

Create in `collection://3ce5e669-4627-8088-b23f-000b14485a78`:

| Property | Value |
| --- | --- |
| Post name | Internal title, not the LinkedIn hook |
| Status | `Ready for Review` |
| Decision | `Pending` |
| Platform | `LinkedIn` |
| Hook | First line as it will appear |
| Content type | `Text`; add `Image / photo` or `Carousel` if needed |
| Topic | From the shared list (includes Ember, Adoption, Close & billing) |
| Target audiences | CFOs / finance leaders, Founders / operators, FP&A / controllers, Accounting / close, Campfire customers / prospects, GTM / RevOps |
| Campfire benefit | One sentence, typed Trust / Category / Adoption / Two-way |
| Inspired by | Inspiration row URLs actually used |
| Graphic | Uploaded file ids when a file exists |
| Post date | Omit unless Erik named a date |

Page body:

1. **LinkedIn post (copy-ready)** — the full post only
2. **Graphic** — preview or notes
3. **Why this draft** — Inspiration + Campfire benefit type
4. **Review notes** — empty heading for Erik

Copy: 800–1,300 characters, line breaks as they should appear. End on a
punchline or a decision, not "What do you think?"

Do not apply the leftover "New post" request-intake template.

If a new graphic is warranted, add `specs/<slug>-YYYY-MM-DD.html` in this
repo using the house palette, or describe the spec in Graphic notes. Do not
fake a rendered image.

## After saving

Fetch each page and confirm Status is Ready for Review. Reply with a table:
Post name, Hook, Campfire benefit type, Notion URL, graphic yes/no. Stop.

Never mark Published, never change Decision, never post to LinkedIn. If Erik
replies Post / Revise / Kill, update that row only (Kill → Cancelled,
Revise → Draft plus notes).
