---
name: draft-linkedin-posts
description: >-
  Draft LinkedIn posts in Erik's finance-operator voice and save them to Notion
  Social Media Planner at Ready for Review. Use when he asks for LinkedIn
  content, a batch of drafts, or to refill the review queue. Never publish to
  LinkedIn.
---

# Draft LinkedIn posts to Notion for review

Source of truth (fetch this page first and follow it):
https://app.notion.com/p/3ce5e6694627817c9debf68c4e304436

If Notion is unreachable, draft in chat and say they were not saved.

## When this applies

Erik wants LinkedIn copy sitting in Notion so he can decide whether to post.
Do not use this to file screenshots of other people's posts — that is
`.cursor/skills/save-linkedin-inspiration`.

## Destinations

- Hub: https://app.notion.com/p/3ce5e66946278105a0a4fc496a44df22
- Review DB: https://app.notion.com/p/3ce5e6694627804792c0fedb8916f055
- Review data source: `collection://3ce5e669-4627-8088-b23f-000b14485a78`
- Inspiration: https://app.notion.com/p/024d0c3975b344cf9328b3c8def35a70
  (`collection://d50dbad2-26ad-4349-b590-402ceaa3b662`)
- This repo: `images/` (rendered 1200×1200 JPEGs), `specs/` (HTML sources)

Fetch both databases before writing.

## Voice

Startup finance operator, not a thought leader.

- Specific artifacts and failure modes (plan vs forecast vs budget, 13-week
  cash, fully loaded headcount, nexus, dilution, AR aging). Not "5 lessons."
- Short LinkedIn lines. White space. One idea per post.
- Dry punchlines. Contrast tables, staircases, before/after. Admit unsolved
  problems.
- Personal, not company-branded. No april footer, no hashtag dumps, no
  "I'm humbled," no emoji walls, no engagement-bait as the whole post.

Graphic language when pairing an image: ground `#EDF2F8`, navy `#12263A` /
`#16375A`, Georgia titles, Helvetica body, 1200×1200, small-caps kicker,
punchline in a navy bar. Render pipeline: `.github/workflows/render-specs.yml`.

## Before writing

1. Query Inspiration where Reusable is yes, newest first (~15). Fetch 3–6
   full pages including screenshots. Use hook patterns and "Steal this" —
   never wording.
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
| Topic | From the shared topic list |
| Target audiences | CFOs / finance leaders, Founders / operators, FP&A / controllers, GTM / RevOps |
| Inspired by | Inspiration row URLs actually used |
| Graphic | Uploaded file ids when a file exists |
| Post date | Omit unless Erik named a date |

Page body:

1. **LinkedIn post (copy-ready)** — the full post only
2. **Graphic** — preview or notes
3. **Why this draft**
4. **Review notes** — empty heading for Erik

Copy: 800–1,300 characters, line breaks as they should appear. End on a
punchline or a decision, not "What do you think?"

Do not apply the leftover "New post" request-intake template.

If a new graphic is warranted, add `specs/<slug>-YYYY-MM-DD.html` in this
repo using the house palette, or describe the spec in Graphic notes. Do not
fake a rendered image.

## After saving

Fetch each page and confirm Status is Ready for Review. Reply with a table:
Post name, Hook, Notion URL, graphic yes/no. Stop.

Never mark Published, never change Decision, never post to LinkedIn. If Erik
replies Post / Revise / Kill, update that row only (Kill → Cancelled,
Revise → Draft plus notes).
