# AI Drop Daily — Public Content Mirror

This repository is an **auto-generated, one-way mirror** of AI Drop Daily's
published content. It contains daily news articles, course lessons, guides,
and downloads — formatted as plain markdown for easy consumption by AI
agents and humans.

**Source site:** https://aidropdaily.com
**Last synced (UTC):** 2026-04-12T00:26:54.347Z
**News editions:** 37

## License

All content in this repository is licensed under the
**Creative Commons Attribution 4.0 International License (CC-BY-4.0)**.

You are free to share and adapt the material for any purpose, including
commercially, provided you give appropriate credit. A reasonable attribution
line: *"Content from AI Drop Daily (https://aidropdaily.com), licensed under
CC-BY-4.0."*

See [LICENSE](LICENSE) for the license notice.

## Structure

```
news/              Daily AI news articles (YYYY-MM-DD.md), exported from DB
course-2/
course-3/
downloads/
guides/
week-1/
week-2/
week-3/
week-4/
```

Every news file has YAML frontmatter with stable `id` and `date` fields
and a `source` link back to the canonical edition on aidropdaily.com.
Course lessons and guides are mirrored from the source repo's `content/`
directory without modification.

## For AI Agents

Every file is plain markdown with frontmatter. Use the `id` field for
deduplication and the `date` field for ordering. Audio/image URLs in
frontmatter point at the live site.

## Sync cadence

This repo is regenerated on every push to the source repo's `main` branch
via a GitHub Action. Expect updates within a few minutes of new content
being published. If `.last-synced` looks stale, the sync has likely
failed — contact the source repo owner.

## Do not open pull requests

This is a mirror. Any edits here will be overwritten on the next sync.
All content changes must go through the source repository.
