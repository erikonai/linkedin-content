# Weekday LinkedIn drafts (9:00 AM America/New_York)

This is the prompt for the recurring Cursor Automation. Trigger: cron
`CRON_TZ=America/New_York 0 9 * * 1-5`. Repo: `erikonai/linkedin-content`.
Notion MCP required. Never publish to LinkedIn.

Follow the live skill first:
https://app.notion.com/p/3ce5e6694627817c9debf68c4e304436

Also read:
- ICP: https://app.notion.com/p/3d85e6694627816ba717da51dfd45a78
- Hub: https://app.notion.com/p/3ce5e66946278105a0a4fc496a44df22
- Planner: `collection://3ce5e669-4627-8088-b23f-000b14485a78`
- Inspiration: `collection://d50dbad2-26ad-4349-b590-402ceaa3b662`

## Run

1. Query Social Media Planner for Status `Not approved`. If those rows are from a prior day, delete them. Do not delete fresh Post Ideas.
2. Query Status `Post Idea` for Post date on **today's** 9:00 AM America/New_York slot. If three (or more) already exist for that slot, do **not** duplicate. Reply with the existing table and stop.
3. Otherwise write **3 different** LinkedIn posts for today's 9:00 AM ET slot.
   - Status `Post Idea`, Decision `Pending`, Platform `LinkedIn`.
   - Mix: 1 Trust, 1 Category, 1 Adoption.
   - Write to Controller / Head of Accounting and CFO / VP Finance.
   - Human thought leadership: first-person scene or a single thesis. No comparison-table carousels. No Review notes section.
   - Ending required, form must vary. Across the 3 posts use three different shapes: a specific operator question, a bar Erik would count, or one Ember-shaped sentence. Scan the last 6 Post Idea endings. Banned as a formula: “How do you all solve for this?”, “What if this didn’t have to exist?”, “That’s the world Ember is for.” Name Ember at most once per post. Not a demo CTA.
   - Steal specificity from Inspiration, not the set piece. No fake logs, 3×3s, or two-character sketches Erik did not live.
   - Graphics: look at Inspiration screenshots and older `images/` maps first. Steal visual form (tables, four-column maps, numbered stacks, bingo, two-column translators). **Do not ship three quote cards.** Three different layouts per batch. Campfire palette only (paper `#F9F9F8`, forest `#142D25`, flame `#FF862F`, sage `#4E615B`, Denim/Inter, flame mark, wordmark). No april blue. No cloned $20M waterfalls.
4. Commit specs/images on a `cursor/` branch, push, open or update a PR.
5. Reply with a table: Post name, Hook, Campfire benefit type, Inspired by, Notion URL, graphic yes/no. Stop.

Never post, schedule, or publish to LinkedIn.
