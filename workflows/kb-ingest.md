---
name: kb-ingest
description: Bring one source (book, video, article, notes, diagram) into the knowledge base
run-by: KB ingestion
---

# KB Ingest

Follows [specs/day-trading/kb-ingestion.md](../specs/day-trading/kb-ingestion.md).

## Steps

1. Identify the source type and create its source record.
2. Capture the raw content (text, transcript, or images) using the method the spec defines for that type.
3. Split large content into chunks (chapters, sections, or time segments).
4. Extract notes from each chunk in the format the spec defines. Chunks may be processed in parallel where the platform supports it.
5. Check new notes against existing ones for duplicates and conflicts.
6. **Checkpoint**: present a summary of new notes, possible duplicates, and conflicts for human review.
7. Update the index and glossary with the approved notes.

## Done When

- [ ] Source record exists
- [ ] Approved notes are written and indexed
- [ ] No spec was changed
