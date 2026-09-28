---
name: kb-ingest
description: Bring one source (book, video, article, notes, diagram) into the knowledge base
run-by: kb-ingestion
---

# KB Ingest

Follows the contract in [kb/README.md](../kb/README.md).

## Steps

1. Decide whether the source belongs in `domain/` or `tech/`, by subject.
2. **Capture**: use the capture skill for the source's medium. It produces text with page or timestamp locators, plus images. Platform-specific shortcuts may be used, but the workflow never depends on them.
3. Write or update `sources/<slug>.md` with the metadata and the captured content.
4. Split the content into chunks (chapters, sections, or time segments).
5. Extract notes from each chunk. Chunks may be processed by parallel workers where the platform supports it.
6. Check new notes against existing ones for duplicates and conflicts.
7. **Checkpoint**: show the human the new notes, possible duplicates, and conflicts.
8. Write the approved notes.

## Done When

- [ ] The source file exists
- [ ] Approved notes are written, with no duplicates of existing notes
- [ ] No spec was changed
