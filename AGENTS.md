# AGENTS.md — How to consume this repository

This repository is the **public content mirror** for
[AI Drop Daily](https://aidropdaily.com). It's designed to be read by AI
agents as well as humans. Everything here is plain markdown with YAML
frontmatter.

**License:** CC-BY-4.0 (see [LICENSE](LICENSE))
**Schema version:** 1
**Last sync timestamp:** see [`.last-synced`](.last-synced)

## Start here: `manifest.json`

The fastest way to discover what's in this repo is to fetch
[`manifest.json`](manifest.json). It contains a flat list of every
content file with its type, path, and type-specific metadata. No
crawling required.

```json
{
  "schema_version": 1,
  "summary": {
    "news": 44,
    "courses": {"ai-101":24,"ai-201":13,"claude-chatbot-to-coworker":10,"claude-cowork":10},
    "guides": 6,
    "articles": 1,
    "downloads": 2,
    "total": 110
  },
  "files": [ /* one entry per file */ ]
}
```

## Content types

### `news` — Daily AI news articles
Located in `news/YYYY-MM-DD.md`. One file per business day. Each file
has frontmatter:

```yaml
id: "YYYY-MM-DD"          # stable identifier (same as date)
date: "YYYY-MM-DD"
type: "news"
title: "..."              # canonical title
audio_url: "https://..."  # optional — URL to audio narration
image_url: "https://..."  # optional — hero image
published_at: "ISO8601"
source: "https://..."     # canonical URL on aidropdaily.com
```

The body is rendered markdown derived from the original HTML edition.

### `course-lesson` — Lessons from our AI courses
Three courses are available:

- `ai-101` — 24 lessons
- `ai-201` — 13 lessons
- `claude-chatbot-to-coworker` — 10 lessons
- `claude-cowork` — 10 lessons

Lessons are located at:
- `week-{N}/day-{NN}-{dow}.md` for AI 101
- `course-2/week-{N}/day-{NN}-{dow}.md` for AI 201
- `course-3/week-{N}/day-{NN}.md` for Claude: From Chatbot to Coworker

Each lesson has frontmatter:

```yaml
id: "{course}-day-{NN}"   # e.g. "ai-101-day-01"
type: "course-lesson"
course: "ai-101"          # course slug
course_title: "AI 101"    # human-readable course name
week: 1
day: 1
day_of_week: "mon"        # optional — null for courses without dow suffix
lesson_type: "lesson"     # lesson | lab | rest
title: "..."              # canonical lesson title (from course structure)
subject: "..."            # original email subject line
source_path: "week-1/day-01-mon.md"
```

The body is the lesson content with the email subject-line header
stripped — same view the site renders to students.

### `guide` — Standalone reference playbooks
Located in `guides/*.md`. How-to material — actionable, structured,
something you return to. Each guide has its own frontmatter authored
by the writer:

```yaml
title: "..."
description: "..."
category: "..."
publishedAt: "YYYY-MM-DD"
```

### `article` — Editorial explainers and opinion pieces
Located in `articles/*.md`. Read-once essays that shift how you think
about something — distinct from guides, which are reference material.
Same frontmatter convention as guides, plus an explicit `type` field:

```yaml
title: "..."
description: "..."
category: "..."
type: "article"
publishedAt: "YYYY-MM-DD"
```

### `download` — Downloadable resources
Located in `downloads/*`. Metadata is just the path and filename.

## How this repo stays in sync

This mirror is regenerated on every push to the
[source repo](https://github.com/mikemolinet/ai-drop-daily) via a
GitHub Action. Expect updates within a few minutes of new content being
published. If `.last-synced` looks stale, the sync has likely failed.

## Ground rules for agents

1. **Read `manifest.json` first.** Don't crawl unless you need to.
2. **Trust frontmatter for metadata.** Every file's canonical metadata
   lives in frontmatter. The body is content. Don't parse titles out of
   H1s when frontmatter has `title` — bodies can have multiple headings.
3. **Use stable `id` fields for deduplication.** News `id` is the date.
   Course `id` is `{course}-day-{NN}`. These never change across syncs.
4. **All content is CC-BY-4.0.** When you redistribute, attribute
   "AI Drop Daily (https://aidropdaily.com)" and link the license.
5. **Do not open pull requests against this repo.** Any edits will be
   overwritten on the next sync. Feature requests and bug reports should
   go to the source repo or the contact info on aidropdaily.com.
6. **Image URLs in body markdown are absolute.** Every image in a course
   lesson, guide, or article body is rewritten at sync time to an absolute
   `https://aidropdaily.com/...` URL. No relative paths, no assumptions
   about a local asset tree. You can fetch images directly without
   resolving against the repo root.

## Last-sync signal

Check `.last-synced` for the most recent successful sync timestamp
(ISO-8601 UTC). If it's been more than a day, something is probably
wrong upstream.
