---
name: save-linkedin-inspiration
description: >-
  Save screenshots of LinkedIn posts Erik likes into the Notion Inspiration
  database. Use when the user attaches LinkedIn screenshots, swipe-file images,
  or asks to capture posts they like as a reference for future drafts.
---

# Save LinkedIn inspiration screenshots

Source of truth (fetch this page first and follow it):
https://app.notion.com/p/3ce5e669462781b79eb8d87f6fb3e5b2

If Notion is unreachable, follow the rest of this file.

## When this applies

Erik sends one or more screenshots / images / PDFs of LinkedIn posts (or
carousels) and wants them stored as a reference library. Phrases like "save
this," "add to inspiration," "this is the vibe," or "swipe file" all count.

Do not use this for drafts Erik wrote. Those go to Social Media Planner via
`.cursor/skills/draft-linkedin-posts`.

## Destinations

- Hub: https://app.notion.com/p/3ce5e66946278105a0a4fc496a44df22
- Database: https://app.notion.com/p/024d0c3975b344cf9328b3c8def35a70
- Data source: `collection://d50dbad2-26ad-4349-b590-402ceaa3b662`

Fetch the database before writing.

## Procedure

Work one screenshot at a time. Several images in one message = several rows,
unless they are slides of the same carousel (one row, all slides on the page).

1. Read the image. Transcribe the hook and enough body to judge structure.
   Note author, line breaks, CTA, and format (text / graphic / carousel).
2. Upload with Notion `create_file_upload` (filename must include `.png`,
   `.jpg`, or `.webp`). POST the local file to `upload_url` as multipart
   field `file`, including every returned header. Use `create_attachment`
   with a public `source_url` only if file upload is unavailable.
3. Create a row in `collection://d50dbad2-26ad-4349-b590-402ceaa3b662`:
   - **Name:** specific, e.g. `Contrarian cash-forecast hook — [Author]`
   - **Author:** visible/provided name, else `Unknown`
   - **Why it works:** 1–3 sentences on craft, for a future assistant
   - **Steal this:** structure / pacing / visual move only — never the wording
   - **Hook pattern:** Contrarian | Framework | Story | List | Confession | How-to | Hot take | Proof | Carousel
   - **Topics:** Cash, FP&A, Headcount, Revenue, Systems, Tax & compliance, Leadership, AI in finance, Career, Writing craft
   - **Screenshot:** uploaded file id
   - **Captured:** today (`date:Captured:start` = YYYY-MM-DD, `is_datetime` = 0)
   - **Reusable:** `__YES__` unless it is off-brand bait or a negative example
4. Page body: screenshot at the top, then Visible hook, Structure, What to
   copy / what not to copy. Extra carousel slides below.

## Rules

- Steal form, not content. Erik's voice is a startup finance operator.
- Unreadable screenshot: still save the file, Reusable = no, say what is missing.
- Never publish, comment, or reshare on LinkedIn.
- Search Name + Author before creating; skip duplicates of the same post.
- If there is no image, ask for the screenshot. Do not recreate from memory.

## Done

Reply with each new Notion URL, Name, Hook pattern, and one sentence on what
is now reusable. Then stop unless Erik also asked for new drafts.
