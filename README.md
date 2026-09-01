# LinkedIn content

Graphics, copy workflow, and Notion review queue for Erik Leavell's LinkedIn posts.

Nothing in this repo publishes to LinkedIn. Drafts land in Notion at **Ready for Review**. Erik decides Post, Revise, or Kill.

## Notion

Hub: [LinkedIn Content OS](https://app.notion.com/p/3ce5e66946278105a0a4fc496a44df22)

| Piece | URL |
| --- | --- |
| Review queue (Social Media Planner) | https://app.notion.com/p/3ce5e6694627804792c0fedb8916f055 |
| Inspiration (screenshots, links, pastes) | https://app.notion.com/p/024d0c3975b344cf9328b3c8def35a70 |
| Skill: draft posts for review | https://app.notion.com/p/3ce5e6694627817c9debf68c4e304436 |
| Skill: save inspiration | https://app.notion.com/p/3ce5e669462781b79eb8d87f6fb3e5b2 |

## How to use it

1. In Cursor (or any assistant with Notion MCP), send screenshots, LinkedIn/other URLs, or pasted copy of posts you like. The save-inspiration skill files each one in Notion with hook pattern, why it works, and what to steal (structure, not wording). A link is enough; LinkedIn login walls still get saved.
2. Ask for a batch of LinkedIn drafts. The draft skill reads Inspiration plus `images/` / `specs/`, writes copy in the finance-operator voice, and creates Social Media Planner rows at Ready for Review.
3. Review in Notion. Set **Decision** to Post, Revise, or Kill.

## Repo layout

- `specs/` — 1200×1200 HTML graphic sources (Georgia titles, Helvetica body, `#EDF2F8` ground, navy punchline bar).
- `images/` — rendered JPEGs. GitHub Actions renders any spec that does not yet have a matching image (`.github/workflows/render-specs.yml`).
- `.cursor/skills/` — Cursor copies of the two Notion skills, with the same destinations.

## Voice

Startup finance operator, not a thought leader. Specific artifacts and failure modes. Short lines. Dry punchlines. Personal, not company-branded.
