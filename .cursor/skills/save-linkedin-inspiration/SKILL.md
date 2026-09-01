---
name: save-linkedin-inspiration
description: >-
  Save LinkedIn posts Erik likes into the Notion Inspiration database from
  screenshots, links, pasted copy, or a mix. Capture craft plus a Campfire
  angle for his Applied AI / Ember-adoption voice. Use when he sends LinkedIn
  URLs, swipe-file images, pasted posts, or asks to capture content as a
  reference for future drafts.
---

# Save LinkedIn inspiration to Notion

Source of truth (fetch this page first and follow it):
https://app.notion.com/p/3ce5e669462781b79eb8d87f6fb3e5b2

If Notion is unreachable, follow the rest of this file.

## When this applies

Erik sends content he likes — screenshots, LinkedIn/other URLs, pasted post
text, or several of those in one message. Phrases like "save this," "add to
inspiration," "this is the vibe," or "swipe file" all count.

A URL is enough. Do not ask for a screenshot before saving a link.

Do not use this for drafts Erik wrote. Those go to Social Media Planner via
`.cursor/skills/draft-linkedin-posts`.

## Destinations

- Hub: https://app.notion.com/p/3ce5e66946278105a0a4fc496a44df22
- Database: https://app.notion.com/p/024d0c3975b344cf9328b3c8def35a70
- Data source: `collection://d50dbad2-26ad-4349-b590-402ceaa3b662`

Fetch the database before writing.

## Role context (for Campfire angle only)

Do not rewrite the original post into an Ember ad. Campfire angle answers:
if Erik stole this *form* tomorrow, how would a CFO reading it help Ember get
adopted or better-informed?

Valid types (same as drafts): Trust | Category | Adoption | Two-way.
"None — craft only" is allowed for pure writing-craft saves; say so.

Erik is Campfire's Applied AI voice: finance-leader-to-finance-leader, deep
with a few strategic accounts, playbooks CS can scale, two-way between
customer reality and Ember. LinkedIn is the external half.

## Split the batch into posts, not file types

- Several unrelated links or images = several rows.
- A link plus a screenshot (or paste) of the **same** post = one row,
  `Source` = Mixed.
- Carousel slides of one post = one row.

If there is no image, no URL, and no post text, ask for one of those. Do not
invent the post.

## Links

1. Dedup on **Link** first (strip `utm_*` and similar tracking params). If a
   row exists, update it instead of duplicating.
2. Fetch the URL. Public articles often work. **LinkedIn commonly returns a
   login wall** — still save the row with the URL in **Link**.
3. On a login wall or empty fetch: save anyway, note it in the page body, and
   ask once for a screenshot or paste. Do not block the save.
4. Store the canonical URL in **Link**.

## Screenshots

1. Read the image. Transcribe hook and enough body to judge structure.
2. Upload with Notion `create_file_upload` (`.png` / `.jpg` / `.webp`). POST
   to `upload_url` as multipart field `file` with the returned headers.
3. Attach to **Screenshot** and place at the top of the page body.

## Pasted text

Treat the paste as the original. Quote the hook. File the rest under
**Transcribed / pasted copy**. Steal this stays pattern-only.

## Create the row

In `collection://d50dbad2-26ad-4349-b590-402ceaa3b662`:

- **Name:** specific, e.g. `Contrarian cash-forecast hook — [Author]`
- **Author:** visible/fetched/provided, else `Unknown`
- **Why it works:** 1–3 sentences on craft, for a future assistant
- **Steal this:** structure / pacing / visual move — never the wording
- **Hook pattern:** Contrarian | Framework | Story | List | Confession | How-to | Hot take | Proof | Carousel
- **Topics:** Cash, FP&A, Headcount, Revenue, Systems, Tax & compliance, Leadership, AI in finance, Ember, Adoption, Close & billing, Career, Writing craft
- **Campfire angle:** one or two sentences (Trust / Category / Adoption / Two-way / craft-only)
- **Link:** URL string when one exists
- **Source:** `Screenshot` | `Link` | `Paste` | `Mixed`
- **Screenshot:** uploaded file ids when images exist
- **Captured:** today (`date:Captured:start` = YYYY-MM-DD, `is_datetime` = 0)
- **Reusable:** `__YES__` unless off-brand bait or a negative example

Page body: screenshot (if any), Link, Visible hook, Structure, What to copy /
what not to copy, **Campfire angle** (repeat), Transcribed / pasted copy (if any),
Fetch notes (if blocked), extra carousel slides.

## Rules

- Steal form, not content. Erik's voice is a startup finance operator with
  Applied AI as the throughline.
- Unreadable screenshot or blocked LinkedIn URL: still save, Reusable honest.
- Never publish, comment, or reshare on LinkedIn.
- Do not recreate a post from memory.

## Done

Reply with each new or updated Notion URL, Name, Source, Hook pattern,
Campfire angle type, and one sentence on what is now reusable. Then stop
unless Erik also asked for drafts.
