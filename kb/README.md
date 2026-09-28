# Knowledge Base

The knowledge base is evidence. It is non-normative, while the [specs](../specs/) are normative. Adding knowledge never changes a spec on its own.

## Layout

```
kb/
  domain/   # knowledge about the domain itself
  tech/     # knowledge about building agents, skills, and workflows (including tool and service APIs)
    sources/<slug>.md
    notes/<id>.md
```

Store each piece of knowledge by its subject, not by who uses it. Both halves follow the same format and the same [ingestion workflow](../workflows/kb-ingest.md).

## Source files: `sources/<slug>.md`

One file per source. The original file stays outside the repo.

```markdown
---
title: <title>
author: <author>
medium: <e.g. book, video, web>
original: <link or local path>
captured: <YYYY-MM-DD>
---

<converted content, with page or timestamp locators>
```

## Note files: `notes/<id>.md`

One claim per note.

```markdown
---
id: <id>
source: <source slug>
locator: <page, section, or timestamp>
concerns: [optional]
---

<the claim, in plain words; quotes are marked as quotes>
```

## Rules

- Extract only what the source says. Never invent claims.
- Ingesting the same source again must not create duplicate notes. Match on source and locator first, then on claim.
- Conflicting notes may both stay.
