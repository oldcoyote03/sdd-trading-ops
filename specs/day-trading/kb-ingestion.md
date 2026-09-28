# Day Trading KB Ingestion Specification

This draft is intentionally neutral and should be specialized with explicit human input before use. It governs how source material enters the knowledge base in [kb/](kb/). Ingestion never changes any spec.

## Objectives

**Primary Objective**: [what the knowledge base should make available to spec authors and agents]

**Success Criteria**:
- [coverage or completeness criterion]
- [traceability criterion, e.g. every note points to its source]
- [quality criterion]

## Sources

### Source Types

| Type | Capture Method | Trust Level |
|---|---|---|
| Book | [OCR or text extraction approach] | [trust level] |
| Video | [transcript approach] | [trust level] |
| Web article / PDF | [fetch or conversion approach] | [trust level] |
| Personal notes / journals | [copy in as-is] | [trust level] |
| Diagrams / charts | [image plus text description] | [trust level] |

### Topics in Scope

- [topic area 1]
- [topic area 2]
- [topics explicitly out of scope]

## Knowledge Structure

### Source Record

- [where the raw material and source metadata are stored]
- [required metadata: title, author, type, link or identifier, capture date]

### Note Format

- [one claim or rule per note, or other granularity]
- [required fields: id, source location, related features, note type, confidence]
- [how quotes vs. paraphrases are handled]

### Index & Glossary

- [how notes are indexed for lookup]
- [how glossary terms are added]

## Rules

- Extract what the source says; never invent claims.
- [how duplicates and conflicting notes are handled]
- [what requires human confirmation before a note is kept]

## Completion

An ingestion is complete when:
- [source record exists]
- [notes are written and indexed]
- [human has reviewed the summary of new notes, duplicates, and conflicts]

## Audit Trail

Every ingestion should be logged with:
- Timestamp
- Source ingested
- Notes added, merged, or rejected
- Reviewer
